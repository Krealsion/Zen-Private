- **WSL**: Ubuntu 22.04, GCC 11.4.0, cmake 3.22 (the floor a CMake feature must clear; CLion's
  bundled cmake is 4.0). Ninja and ccache are not installed system-wide; they sit under
  `~/opt/zoom/bin-ninja` and `~/opt/zoom/bin-ccache` (the ccache wrapper needs `LD_LIBRARY_PATH`).
  `sudo` needs a password. WSL sees 30 GB of the host's 63.
- **CPU**: Ryzen 9 7900X, 12 physical cores / 24 threads. `-j24` is the best measured build
  parallelism; `-j32` is slower. In WSL, which sees 30 GB, Zengine's official lane at `-j24`
  had compilers killed for memory (2026-09-30); `-j8` built. The founder's limits (2026-10-04):
  a Windows build (MinGW-w64, MSVC, the SDL tree) runs at up to `-j16`; a WSL build stays at
  `-j8`, since more can run the host out of memory. Measured 2026-10-04: a clean MinGW-w64
  build of 358 edges took 545 s at `-j8` and 326 s at `-j16`.
- **The executor's primary folder** (constitution § c; `Zen/pass-tools/executor-kit/`, its
  README), kept between phases: on G:, `Zen/primary/` holds the Zengine and Loom clones and, in
  `win/`, `zengine-msys` (the MinGW-w64 lane), `zengine-sdl`, `loom-msys` and
  `loom-msys-install`; in WSL, `~/zen-build/primary/` holds `zengine-primary`,
  `zengine-primary-san`, `loom`, `loom-install` and its own ccache store `ccache` (24 GB cap,
  launcher `bin/ccache`). About 15.7 GB on G: and 16 GB in WSL (2026-10-04). Its trees are the
  executor's, not the founder's below.
- **ccache on Windows**: MSYS2's `mingw-w64-x86_64-ccache` 4.11.3-1 is installed in
  `C:\msys64x\mingw64` with eight dependencies, from the existing sync database and with nothing
  upgraded (2026-10-04; `g++` still 15.2.0). The kit's store is
  `C:\Users\Joshua\zen-build\primary\ccache` (NTFS, 24 GB cap). A hit skips the compile but not
  `ar` and `ld`, which write to G: and now dominate a rebuild: returning both Windows trees across
  one PR's delta took 380 s with ccache against 604 s without.
- **Fetch caches** in `~/.cache/zen-fetch/`: only `zengine-zengine-p1{,-san}` and
  `zengine-zengine-primary{,-san}` remain (2026-10-04).
- **Build trees on ext4** under `~/zen-build/`: `loom`, `loom-install`, `zengine-p1`,
  `zengine-p1-san` (the Ninja-configured Zengine trees) and `CS3-head`, whose `prefix` (Loom
  `b47c7d6`) is the Loom both Zengine trees build against (`CMAKE_PREFIX_PATH` and `loom_DIR`,
  measured 2026-09-30), so it stays with them. A tree's
  generator is baked in, and Zengine's FetchContent cache `~/.cache/zen-fetch/zengine-<basename>`
  is keyed by build-directory basename with no eviction (13 GB measured) — reuse names. Both
  Zengine trees carry the ccache launcher, so a timed clean build sets `CCACHE_DISABLE=1` or it
  measures the cache.
- **G: is exFAT with 256 KB clusters**: a file takes at least 256 KB of disk, so many small files
  cost far more than their bytes (104,259 run-package files of 0.9 GB held about 25 GB), and
  junctions and symlinks cannot exist there.
- **G: shows WSL whole-second file times** (exFAT through drvfs): a source rewritten in the second
  its object was compiled looks older than the object, so Ninja keeps the stale object. A tool that
  rewrites sources under WSL and rebuilds at once (a mutation driver) waits past a second boundary
  before each write (measured 2026-10-01).
- **`Zengine/.git/worktrees` can stick delete-pending** when the last worktree is removed: Git,
  `ls` and PowerShell then answer Access/Permission denied and `git worktree add` fails. Seen
  2026-09-30 and 2026-10-01, both times with CLion open; a restart cleared it. A phase that meets
  it works in a clone in its `trees/`.
- **CLion 2025.2's bundled MinGW** at `C:\Program Files\JetBrains\CLion 2025.2\bin\mingw\bin`
  (g++ 13.1, binutils 2.40), ninja under `bin\ninja\win\x64`, cmake under `bin\cmake\win\x64\bin`.
  That `mingw\bin` must be on `PATH` in EVERY tool call: without it `cc1plus.exe` dies
  `0xC0000135` and g++ prints nothing, and a built `.exe` dies `0xc0000139` before any test runs.
- **MSVC**: VS 2026 Community 18.1 at `C:\Program Files\Microsoft Visual Studio\18\Community`
  (cl 19.50). Zengine's MSVC lane needs `VsDevCmd.bat -arch=x64` loaded into the shell (its
  `INCLUDE`/`LIB`/`LIBPATH`/`PATH`); `Enter-VsDevShell` is not a substitute (it needs `vswhere` on
  `PATH` and fails while appearing to continue). Zengine's MSVC tree is `build-msvc-p1` and its
  MinGW tree is `build-win-msys` (below; `build-win-jx` is the CLion-toolchain predecessor,
  unconfigurable since its prefix vanished); the working MSVC Loom prefix is Loom
  `build-msvc-p1/_install` — Debug AND `LOOM_ENABLE_WINDOWS_KERNEL=ON` (a Release install links
  as `LNK2038` mismatches; a kernel-less install makes configure silently skip every weave).
- **Git remote operations run from the Windows Bash tool, never WSL**: the SSH key exists only at
  Windows `~/.ssh/id_ed25519`. `gh` is installed and logged in (it opens the pull requests); the
  Actions API is readable unauthenticated for job conclusions, not for logs.
- **The Bash tool** is Git Bash: its `python` is Windows Python, its `/tmp` is not WSL's, and WSL's
  `/tmp` does not survive between tool calls; `perl -0pi` cannot rename its work file on `/mnt/g`;
  a heredoc of ~190 lines or more fails with `unexpected EOF`; `wsl -e bash <script>` has its
  `/mnt` paths mangled by MSYS — go through `bash -lc`. WSL kills `nohup`/`disown` when the last
  client exits, so a long harness needs a detached `wsl.exe` client. The Bash tool has no
  `python3`: a `python3 - <<EOF` heredoc falls through to `python` and opens a REPL that never
  exits, so a script is written to a file and run, in WSL; its `grep -P` is not UTF-8 clean.
  `bc` is not in Git Bash — timing arithmetic uses `$(( ))` over `date +%s%N`.
  `wsl.exe bash -lc '…'` expands `$?` and `$(…)` before the inner bash runs, so an exit captured
  in a chained command there is a launch-time value (2026-09-27): put the chain in a script.
- **SDL**: the WSL-fetched SDL3 has only the `dummy`/`offscreen` video drivers (no X11/Wayland
  dev headers at configure), so WSLg is irrelevant and a live SDL witness runs on a Windows tree
  with `ZENGINE_SDL_SKIN=ON`.
- **The desktop**: a 5760x3240 virtual desktop spanning (-1920,-1080)–(3840,2160) with a
  negative-coordinate monitor; Night Light / f.lux shifts every screen capture (red exact, green
  about half, blue about a sixth — diff with a tolerance, ±8 worked); no image library on the
  machine (no PIL, numpy or ImageMagick) and .NET 10's `System.Drawing` is unusable from
  `Add-Type`, so witness harnesses run under `powershell.exe` 5.1 and diff uncompressed BMPs with
  stdlib Python; Win11 Notepad is a packaged app and not a control target.
- **An AutoHotkey startup script `ctrljk-updown.ahk` maps `^k` to Down machine-wide** (KEY-0a).
  Enumerate remappers (AutoHotkey, PowerToys KBM) before diagnosing a dead chord.
- **Windows console hosts**: conhost and Windows Terminal both deliver right-click to a
  mouse-enabled console app; a console client cannot resize its own window under Win11's default
  terminal; a `PROC_THREAD_ATTRIBUTE_PSEUDOCONSOLE` child still inherited the parent's handles
  (unresolved).
- **tmux works as a TUI witness harness in WSL** (`send-keys -H` with raw SGR mouse bytes;
  `resize-window` drives a real resize).
- **A stale `Zen/install/loom`** (the prefix CLion's `cmake-build-debug` consumes) fails that lane's
  regeneration with a message that blames Zengine.
- **This harness keys its memory directory to the launch cwd** `G:\programming\cpp\Zen`; launching
  from a sub-repository opens a different, empty store.
- **`build-win-jx`'s Loom prefix lives in a harness session's scratchpad** (its `CMakeCache.txt`
  names it), so it vanishes with that session's temp sweep and the tree then cannot configure;
  rebuild the MinGW Loom prefix somewhere durable before trusting that tree again.
- **Git Bash rewrites `/c` and `/J` to drive paths** (MSYS argument conversion), so `cmd.exe /c …`
  and `mklink /J …` silently misfire from the Bash tool: write `//c` and `//J`, or put the
  command in a batch file.
- **`VsDevCmd.bat` changes the working directory** when it loads unless `VSCMD_START_DIR` is set;
  set it to the tree first, or every relative path after the call points at the VS install.
- **The MSYS2 toolchain at `C:\msys64x\mingw64`** (g++ 15.2, binutils 2.45) built the local MinGW
  lane below. Its binutils clear the 2.40 ceiling that stopped CLion's bundled MinGW from
  assembling `workshop.cpp` until the Workshop split (2026-09-03); since the split every Workshop
  object assembles under binutils 2.40 too (`workshop-split-RB.md` §11), so no MinGW toolchain on
  this machine is ruled out. Its `bin` must be on `PATH` in EVERY tool call for the same reason
  CLion's `mingw\bin` must — the built `.exe`s load `libstdc++-6.dll`, `libgcc_s_seh-1.dll` and
  `libwinpthread-1.dll` from there. Since 2026-09-03 the lane is built rather than owed:
- **The MSYS2 Loom prefix is `Loom\build-win-msys\_install`** — durable, named after the tree that
  made it, deliberately NOT `Zen\install\loom` (which CLion's `cmake-build-debug` consumes, and a
  stale one there breaks that lane) and not a harness scratchpad (which is what left
  `build-win-jx` unconfigurable). Debug, Ninja, `LOOM_ENABLE_WINDOWS_KERNEL=ON` (a kernel-less
  install makes Zengine's configure skip every weave), tests and examples off:

  ```text
  cmake -S Loom -B Loom/build-win-msys -G Ninja -DCMAKE_BUILD_TYPE=Debug \
        -DCMAKE_CXX_COMPILER=C:/msys64x/mingw64/bin/g++.exe \
        -DLOOM_ENABLE_WINDOWS_KERNEL=ON -DZEN_BUILD_TESTS=OFF -DZEN_BUILD_EXAMPLES=OFF
  cmake --build Loom/build-win-msys --parallel 24
  cmake --install Loom/build-win-msys --prefix Loom/build-win-msys/_install
  ```

  Measured 2026-09-03 at Loom `2eb6827`: 34 objects, 7 s at `-j24`; the prefix is 33,597,878
  bytes in 57 files and exports `loom::kernel`. It was not rebuilt since: on 2026-09-27 it was
  behind Loom `0839bfc`, so rebuild it before a MinGW lane or mutant that must match Loom main.
- **The Zengine MinGW tree is `Zengine\build-win-msys`**, configured exactly as `ci.yml`'s
  `Zengine / Windows / MinGW-w64 Loom stranger` job configures its own:

  ```text
  cmake -S Zengine -B Zengine/build-win-msys -G Ninja -DCMAKE_BUILD_TYPE=Debug \
        -DCMAKE_CXX_COMPILER=C:/msys64x/mingw64/bin/g++.exe \
        -DCMAKE_PREFIX_PATH=G:/programming/cpp/Zen/Loom/build-win-msys/_install \
        -DZEN_LOOM_DEV=OFF -DBUILD_TESTING=ON -DZENGINE_SDL_SKIN=OFF
  ```

  `CMAKE_C_COMPILER` is accepted and unused by both projects — CMake warns; C is never enabled.
- **The three commands that run the lane**, from the Zengine checkout, and it stays serial:

  ```text
  export PATH="/c/msys64x/mingw64/bin:$PATH"
  cmake --build build-win-msys --parallel 24
  cmake -DZEN_BUILD_DIR=build-win-msys -P tests/verify.cmake
  ```

  Measured 2026-09-03 at Zengine `8ceee9d`: 148 edges in 80 s; `workshop.cpp.obj` 47,226,532
  bytes and `zengine-workshop.exe` 48,612,545 bytes — the object binutils 2.40 refused before the
  split; the lane PASSED 30 of 30, `gates active: always`, 89.9 s; the tree is 2.0 GB.
  Beside heavy compiles, MinGW's `ar` ran out of memory at `--parallel 24` (2026-09-27);
  `--parallel 8` passed.
  `ctest --test-dir build-win-msys -R '^(workshop_files|workshop_panes)$' -V` is where the
  junction witnesses print: the sweep case in `workshop_files` and, since #70, the
  linked-directory case in `workshop_panes`. On this machine both say "made as a junction".
- **The CLion tree `Zengine\cmake-build-debug`, now on the MSYS2 toolchain, builds the app.**
  Rebuilt 2026-09-03: exit 0 in 52 s, `workshop.cpp` assembled and `zengine-workshop.exe` linked,
  and a second build says `ninja: no work to do`. Its prefix `Zen\install\loom` was installed
  from `Loom\build-clion`, whose cache names the same MSYS2 compiler and the Windows kernel on.
- **The harness collapses `\\` to `\` in a command before the shell sees it**, so a `\b`
  written as `\\b` reaches Python or printf as a backspace (measured 2026-09-03: a
  single-quoted `'x\\b'` arrived in Python as one backslash). Text that must carry a
  backslash goes through a file written by a tool, never through the command line.
- **DisplayFusion injects `AppHook64_....dll` into every windowed process** (the release
  research, 2026-10-10): a loaded-module judgment of a graphical program on this machine names it,
  and it is not the package's.
- **The build trees' disk decides Windows builds** (the C: drive test, 2026-10-10, one run each,
  `reportbacks/c-drive-builds-RB.md`): with the tree on C: (internal NVMe, NTFS) a warm build took
  23.9 s against 328.3 s on G:, a cold one 264.8 s against 532.0 s, a Loom source's rebuild 24 s
  against 272 s; one pane's change costs the same on both. Sources on G: with the tree on C: matched
  everything on C:. In WSL `/mnt/c` reads as `/mnt/g`; an ext4 source copy took the official lane
  from 247.7 s to 208.8 s and its text checks from 110 s to 19 s.
- **G: (exFAT on USB) gives Windows programs 2-second file times and WSL whole seconds**; C: gives
  both sub-microsecond ones. Twice a G: build rebuilt what the build before had just made; none with
  its tree on C: did. G:'s 256 KB clusters hold Zengine's primary `.git` in 1.3 GB against 63 MB.
- **`C:/Zen` is a copy of Zen**, a snapshot of 2026-10-09 22:05; its primary trees were configured
  on G: and cannot be used where they are. The indexer excludes both Zens and includes
  `C:\Users\Joshua\zen-build\`.
- **D: is a Dev Drive (ReFS)**, made for the build-speed phase (2026-10-10); `D:/zen-build/` holds
  that phase's trees and caches. Tutorial and demo pictures are taken from a root under `D:/Zen`
  from now on (the founder, 2026-10-10).
- **WSL as the founder reaches every Windows file he can** (an agent's powers, researched,
  2026-10-10): kernel 6.6.87.2, unprivileged user namespaces allowed, Yama `ptrace_scope` 1;
  `/etc/wsl.conf` holds only `[boot] systemd=true`; no `bwrap`; drvfs mounts the Windows drives 777
  with no `metadata`, so `C:\Users\Joshua\.ssh` reads through `/mnt/c`; G: and H: are exFAT, with no
  ACLs; `memory` and `pids` are delegated to the user's slice; WSLg's X sockets are `/tmp/.X11-unix`
  and `/mnt/wslg/.X11-unix`.
- **The founder's SSH key asks a passphrase** (rotated 2026-10-10), so no session can push over SSH
  unattended; sessions push over HTTPS, where Git Credential Manager already holds the founder's
  login (the overhaul's B1 continuation, 2026-10-11).
