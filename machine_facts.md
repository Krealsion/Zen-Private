- **WSL**: Ubuntu 22.04, GCC 11.4.0, cmake 3.22 (the floor a CMake feature must clear; CLion's
  bundled cmake is 4.0). Ninja and ccache are not installed system-wide; they sit under
  `~/opt/zoom/bin-ninja` and `~/opt/zoom/bin-ccache` (the ccache wrapper needs `LD_LIBRARY_PATH`).
  `sudo` needs a password. WSL sees 48 GB of the host's 63 (`.wslconfig`, 2026-10-27: 30, then
  44; `MemTotal` reads 47 GB).
- **Night Lab's distribution, `Zen-Night-Lab`** (the wall, built and checked 2026-10-16): Ubuntu
  24.04 under WSL 2.6.2, with users of its own: `labagent`, the default, with no sudo and no
  privileged group, and `labadmin`, with sudo, the founder's, its password never in the lab.
  `/etc/wsl.conf`: systemd on; drive automount and fstab off; Windows interop and the Windows PATH
  off; the GPU off. WSLg off for every distribution (`guiApplications=false` in the founder's
  `.wslconfig`, 2026-10-16), since it shared the Windows clipboard. Networking mirrored, as every
  distribution's: the said limit, it reaches Windows' localhost and the home network. Installed: g++
  13.3, cmake 3.28.3, ninja 1.11.1, ccache, `gh` 2.45, bubblewrap and socat (Claude Code's sandbox),
  and Claude Code 2.1.301 by its native installer in `~/.local` (auto-updating). Both logged in by
  the founder: `gh` with a fine-grained token reaching only `zen-night-lab` (Contents read and
  write), and Claude Code. Root is reached only from Windows, `wsl -d Zen-Night-Lab -u root`; a
  script goes in on standard input, since the lab sees no Windows drive: `cmd /c "wsl -d
  Zen-Night-Lab -- bash -s < <script> > <output> 2>&1"`. The scripts and the check:
  `Zen/night-lab/wall/` (`verify.sh`, 23 checks passed, 0 failed, 2026-10-16).
- **CPU**: Ryzen 9 7900X, 12 physical cores / 24 threads. `-j24` is the best measured build
  parallelism; `-j32` is slower. In WSL, when it saw 30 GB, Zengine's official lane at `-j24`
  had compilers killed for memory (2026-09-30); `-j8` built. The founder's limits (2026-10-04):
  a Windows build (MinGW-w64, MSVC, the SDL tree) runs at up to `-j16`; a WSL build stays at
  `-j8`, since more can run the host out of memory. Measured 2026-10-04: a clean MinGW-w64
  build of 358 edges took 545 s at `-j8` and 326 s at `-j16`.
- **The executor's primary folder** (constitution § c; `Zen/pass-tools/executor-kit/`, its
  README), kept between phases, as build-speed laid it out (2026-10-10): on G:, `Zen/primary/`
  holds the Zengine and Loom clones; under the kit's Windows root `C:/Users/Joshua/zen-build/`,
  `primary/` holds `zengine-msys` (the MinGW-w64 lane), `zengine-sdl`, `loom-msys`,
  `loom-msys-install` and the Windows ccache store, and a phase's own Windows trees sit in
  `<PHASE>/`; in WSL, `~/zen-build/primary/` holds `src/zengine` (an ext4 copy of the Zengine
  clone, which a lane refuses to run from unless its files are the clone's byte for byte),
  `zengine-primary-ext4` and `zengine-primary-ext4-san` built from it, `loom`, `loom-install` and
  its own ccache store `ccache` (24 GB cap, launcher `bin/ccache`). Its trees are the executor's,
  not the founder's below. The trees the move left unused are the founder's to delete:
  `Zen/primary/win/` on G: and WSL's `~/zen-build/primary/zengine-primary{,-san}` with their fetch
  caches `~/.cache/zen-fetch/zengine-zengine-primary{,-san}` (counted 2026-10-04 at 15.7 GB on G:
  with the clones, and 16 GB in WSL).
- **ccache on Windows**: MSYS2's `mingw-w64-x86_64-ccache` 4.11.3-1 is installed in
  `C:\msys64x\mingw64` with eight dependencies, from the existing sync database and with nothing
  upgraded (2026-10-04; `g++` still 15.2.0). The kit's store is
  `C:\Users\Joshua\zen-build\primary\ccache` (NTFS, 24 GB cap). A hit skips the compile but not
  `ar` and `ld`, which dominated a rebuild while the trees were on G:: returning both Windows trees
  across one PR's delta took 380 s with ccache against 604 s without (2026-10-04).
- **The kit's stores since executor-kit-speed** (Zen `ee2d32fb`, 2026-10-12): one store per side
  serves every executor tree of that side, `base_dir` `/home/joshua/zen-build` in WSL and
  `C:/Users/Joshua/zen-build` on Windows, `hash_dir = false`; the first build through the landed kit
  writes both settings, gives a tree a C launcher and changes every compile's key once. A second
  copy's WSL trees read their own copy of the Loom prefix (`<copy>/loom-install`), and Loom installs
  by content, so a same-bytes reinstall writes nothing. A second copy is cloned under the Windows
  root beside its trees (`<root>/<PHASE>/<name>/zengine`, since Zen `f20dd0c9`, 2026-10-12), so the
  store serves it: 231 of 291 hits against 98 when its clone lay on G:. SDL3's own C files compile
  with SDL's precompiled header, which ccache 4.5.1 does not cache (218 calls a WSL build). A
  test-only edit runs its own suites through `case-wsl.sh affected`; the slot queues builds in the
  order asked, a Windows build holding it through a 10 s quiet window (20 s until `f20dd0c9`); the
  kit is edited in a staged copy and landed by `kit.sh land` once nothing reads it; `run-end.sh`
  reads a hosted run's end for a report's table.
- **Windows' short sleeps last a scheduler tick**: `Sleep(1)` and a 1 ms `sleep_for` each took about
  15.5 ms on this machine, a high-resolution waitable timer 1.5 ms for 1 and 10.2 for 10, and
  `GetTickCount64` steps 15 or 16 ms (fast forward S1, 2026-10-12).
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
- **MSVC**: VS 2026 Community 18.1 at `C:\Program Files\Microsoft Visual Studio\18\Community` (cl
  19.50.35720). It refuses `editor/neovim/lua.hpp`'s 20.6 KB `kModule` literal (C2026), which the
  hosted cl 19.51 accepts, so no local MSVC build of Zengine `main` completed until Visual Studio
  was updated (the founder updated it, 2026-10-11; the next local MSVC build says whether it now
  compiles); the Windows lanes phase split the literal in its trees, uncommitted (2026-10-11). The
  kit builds Zengine with MSVC (`build-win.sh msvc`, and `msvc-bare` with nothing added). Zengine's
  MSVC lane needs `VsDevCmd.bat -arch=x64` loaded into the shell (its
  `INCLUDE`/`LIB`/`LIBPATH`/`PATH`); `Enter-VsDevShell` is not a substitute (it needs `vswhere` on
  `PATH` and fails while appearing to continue). Zengine's MSVC tree is `build-msvc-p1` and its
  MinGW tree is `build-win-msys` (below; `build-win-jx` is the CLion-toolchain predecessor,
  unconfigurable since its prefix vanished); the working MSVC Loom prefix is Loom
  `build-msvc-p1/_install` — Debug AND `LOOM_ENABLE_WINDOWS_KERNEL=ON` (a Release install links as
  `LNK2038` mismatches; a kernel-less install makes configure silently skip every weave).
- **Git remote operations run from the Windows Bash tool, never WSL**; the Actions API is readable
  unauthenticated for job conclusions, not for logs. Two GitHub logins live here (2026-10-10):
  - **the founder's, `Krealsion`**: `gh`'s default login (it opens the pull requests; on 2026-10-11
    `gh`'s active login read `UnknownWorkers` instead, so a session pinned `GH_TOKEN` from `gh auth
    token --user Krealsion` per command, and `issue-say.sh` posted as the machine account), and Git
    Credential Manager's for HTTPS remotes. His SSH key, `~/.ssh/id_ed25519` (rotated 2026-10-10),
    asks a passphrase: Git Bash's `ssh` cannot ask it (`read_passphrase: can't open /dev/tty`), and
    the Windows OpenSSH agent holds it, so a session reaches an SSH remote with
    `GIT_SSH_COMMAND=C:/Windows/System32/OpenSSH/ssh.exe`, or uses HTTPS;
  - **the restricted agents', `UnknownWorkers`** (a GitHub machine account): its own `gh` login,
    `GH_CONFIG_DIR="$HOME/.config/gh-unknownworkers" gh ...`, a classic token with `repo` and
    `read:org`. No collaborator access to Zengine or Loom: it files issues, comments, and opens pull
    requests from its own fork, and never merges, pushes to the founder's repositories or sets
    labels. Git's own credentials are untouched by it; pushing to its fork as it, through `gh auth
    git-credential` under that `GH_CONFIG_DIR`, is untried. A restricted agent uses this login and
    no other.
- **The Bash tool** is Git Bash: its `python` is Windows Python, its `/tmp` is not WSL's, and WSL's
  `/tmp` does not survive between tool calls; `perl -0pi` cannot rename its work file on `/mnt/g`;
  a heredoc of ~190 lines or more fails with `unexpected EOF`; `wsl -e bash <script>` has its
  `/mnt` paths mangled by MSYS — go through `bash -lc`. WSL kills `nohup`/`disown` when the last
  client exits, so a long harness needs a detached `wsl.exe` client. The Bash tool has no
  `python3`: a `python3 - <<EOF` heredoc falls through to `python` and opens a REPL that never
  exits, so a script is written to a file and run, in WSL; its `grep -P` is not UTF-8 clean.
  A heredoc's backslashes do not survive it either (`\\` became `\` three times in G2's stage 2,
  2026-10-20): a patch script holding one is written with the file tool.
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
- **Seven more MinGW-w64 toolchains** (five MinGW-Builds GCC from 12.2, llvm-mingw Clang 18.1.8 and
  23.1.2) sit in their home beside the kit's primary, `C:/Users/Joshua/zen-build/toolchains/`
  (2026-11-02), their archives in the weave-runtime-windows phase's `dl/` (2026-10-11). CLion 2025.2's GCC 13.1 builds Loom's libraries but, once Loom
  #53 merges, no weave: its libstdc++ lacks `__cxa_thread_atexit`, which the contract refuses.
- **The harness collapses `\\` to `\` in a command before the shell sees it**, so a `\b`
  written as `\\b` reaches Python or printf as a backspace (measured 2026-09-03: a
  single-quoted `'x\\b'` arrived in Python as one backslash). Text that must carry a
  backslash goes through a file written by a tool, never through the command line: a batch file
  written through `printf` lost a backslash and a digit (`Visual Studio\18` became `Studio8`,
  2026-10-11).
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
- **D: is gone**: the Dev Drive (ReFS, a VHDX) measured level with plain C: (a cold build 258 s
  against 262, warm 25.4 against 26.0; build-speed, 2026-10-10), so the founder chose plain C: for
  the Windows root and deleted the Dev Drive's partition and its file (2026-10-10). Tutorial and
  demo pictures are taken from a root under `C:/Zen-pictures` (the founder's choice after D: went,
  2026-10-10, as B2's picture script records it).
- **WSL as the founder reaches every Windows file he can** (an agent's powers, researched,
  2026-10-10): kernel 6.6.87.2, unprivileged user namespaces allowed, Yama `ptrace_scope` 1;
  `/etc/wsl.conf` holds only `[boot] systemd=true`; no `bwrap`; drvfs mounts the Windows drives 777
  with no `metadata`, so `C:\Users\Joshua\.ssh` reads through `/mnt/c`; G: and H: are exFAT, with no
  ACLs; `memory` and `pids` are delegated to the user's slice; WSLg's X sockets are `/tmp/.X11-unix`
  and `/mnt/wslg/.X11-unix`.
- **Python's `write_text` on Windows writes CRLF**: a helper that edits a product file writes bytes,
  as the kit's `replace.py` does (the Weaver's decisions, 2026-10-11).
- **Under Git Bash's `PATH`, a MinGW-w64 program loads Git for Windows' `libstdc++-6.dll`**
  (`C:\Program Files\Git\mingw64\bin`, ahead of MSYS2's) unless the toolchain's `bin` comes first,
  as the kit puts it (runtime-gcc16, 2026-10-10).
- **A second MinGW-w64 toolchain sits in scratch**: MSYS2's GCC 16.2.0 Rev5 with binutils 2.47 in
  `Zen/scratch/runtime-gcc16/toolchains/msys2-gcc16/` (its `fetch-msys2.sh` remakes it from signed
  packages), beside the verified archives in `dl/`; `C:\msys64x` stays at 15.2.0 Rev8, the kit's
  (runtime-gcc16, 2026-10-10).
