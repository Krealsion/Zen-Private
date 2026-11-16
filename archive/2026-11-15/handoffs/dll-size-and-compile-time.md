# What fills a DLL, and where the compile time goes (Vision, 2026-10-20)

Measured for the founder's question: why the files are so big, and which pieces tied together a
split would speed up. Nothing was changed.

## Where it was measured

- **The DLLs**: the primary's MinGW-w64 lane tree, `C:/Users/Joshua/zen-build/primary/zengine-msys`
  (Debug, `-g`, tests on, configured as CI's MinGW-w64 job): its 35 product weave DLLs, leaving out
  the staged copies under `workshop/` and `examples/snake/` and the test weaves. Sections from the
  PE headers; functions from the COFF symbol table (`nm`, a function's size by address).
- **The compile times**: that tree's `.ninja_log` (the last build of each object, 2026-10-19, at 16
  jobs, so each object is slower than alone) and `.ninja_deps` (the headers each object read).
- **Inside one object**: `tests/test_workshop_panes_builder.cpp` (205 s in that log), compiled alone
  in Vision's cloud workspace against Zengine `main` `75e335b3` and Loom `3afe9e3`, with GCC 13.3
  (`-ftime-report`) and clang 18.1 (`-ftime-trace`), the tree's flags and its generated manuals.

## The DLLs

- The 35 weigh 739 MB: debug information 394 MB (53 %), symbol tables 277 MB (37 %, most of it
  mangled names), machine code 50 MB (7 %), the rest 18 MB.
- Of the 46.5 MB of functions, 37.9 MB (82 %) are copies of a function another of the 35 holds;
  5.0 MB lie in one DLL only, about 140 KB a weave.
- The largest, `zengine-info-pane.dll`, 37.2 MB: debug 18.8, symbols 14.9 (names 11.6), code 2.6.
  Of its code, the standard library's templates and runtime are 60 %, Loom 13 %, Zengine 10 %
  (`zengine::info_pane` itself 118 KB), the file's own anonymous namespace 2 %.
- A near-empty provider (`tests/zengine-provider-min.dll`) is 6.8 MB, 0.5 MB of it code: the floor
  every weave carries.
- Why each carries more than its own code: a weave links Loom's core and switchboard statically
  (Loom `CMakeLists.txt:125`) and, on MinGW-w64, its own C++ runtime, `-static`
  (`cmake/loom-weave.cmake:166-167`), both by the weave build contract (KERN-05); and every
  template it uses is compiled into it.

## The compile time

- 7,690 s over 343 objects: test objects 5,691 s (74 %), product weaves and libraries 1,077 s
  (14 %), the Workshop host 922 s (12 %). The panes suite alone is 3,030 s (39 %). The slowest 30
  objects are 49 % of it, the slowest 60 are 73 %.
- 47 objects took 60 s or more. Each reads about 120 to 150 Zengine headers, 1.9 to 2.6 MB of
  them, about 45 Loom headers and about 470 of the compiler's. 35 of the 47 include
  `tests/workshop_support.hpp` (233 KB); 39 include `workshop/weave.hpp` (134 KB) and
  `workshop/screen.hpp` (94 KB).
- Inside the panes suite's builder object (alone: GCC 59 s, clang 48 s): parsing 24 %, template
  instantiation 30 %, code generation 44 % (GCC's phases). Of clang's 17.7 s of parsing, 16.5 s
  comes through `tests/workshop_support.hpp`; Zengine's own headers are 14.3 s of it.
- Templates there by clang's summed time, which counts a template again at every level it nests
  in itself: the facet lists' merge, `zengine::detail::MergeLists`
  (`activation/activation.hpp:103-125`), summed 21.8 s over 263 instances, but costs 0.14 s counted
  once (corrected by the lighter-builds phase, 2026-10-21): not where the time is. The time is code
  generation, parsing what `tests/workshop_support.hpp` includes, Loom's shape templates and the
  `std::tuple` machinery a shape's fields are declared in (`std::make_tuple`, Loom
  `zen/weave/shape.hpp:398`), and on MinGW-w64 the GNU assembler: about 40 s of that object's 71 s,
  on about 97,000 sections, four for each function, the debug level barely moving it.
- Debug information in that object: `-g1` 12 % faster and 31 % smaller than `-g`; `-g0` 16 % faster
  and 57 % smaller.

## What it means

- The size is mostly debug information and names; a weave's own code is already small.
- The time is mostly the tests, and in them the same world parsed and instantiated again: about 40
  heavy objects each read most of Zengine's headers and instantiate the same facets and shapes, so
  every pane, shape or facet added grows all of them at once.
- The pieces tied together: `tests/workshop_support.hpp` (the rigs, in one header), Workshop's
  `weave.hpp` and `screen.hpp`, and the shape schemas and functions every object rebuilds.

## Not measured

- The whole build attributed by header and template (one object was traced); what any split
  saves; MSVC; the Linux trees; the hosted runners.
