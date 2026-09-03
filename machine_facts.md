- **WSL**: Ubuntu 22.04, GCC 11.4.0, cmake 3.22 (the floor a CMake feature must clear; CLion's
  bundled cmake is 4.0). Ninja and ccache are not installed system-wide; they sit under
  `~/opt/zoom/bin-ninja` and `~/opt/zoom/bin-ccache` (the ccache wrapper needs `LD_LIBRARY_PATH`).
  `sudo` needs a password. WSL sees 30 GB of the host's 63.
- **CPU**: Ryzen 9 7900X, 12 physical cores / 24 threads. `-j24` is the best measured build
  parallelism; `-j32` is slower.
- **Build trees on ext4** under `~/zen-build/`: `loom`, `loom-install`, `zengine-p1`,
  `zengine-p1-san` (the Ninja-configured Zengine trees against the ext4 Loom install). A tree's
  generator is baked in, and Zengine's FetchContent cache `~/.cache/zen-fetch/zengine-<basename>`
  is keyed by build-directory basename with no eviction (13 GB measured) — reuse names.
- **CLion 2025.2's bundled MinGW** at `C:\Program Files\JetBrains\CLion 2025.2\bin\mingw\bin`
  (g++ 13.1, binutils 2.40), ninja under `bin\ninja\win\x64`, cmake under `bin\cmake\win\x64\bin`.
  That `mingw\bin` must be on `PATH` in EVERY tool call: without it `cc1plus.exe` dies
  `0xC0000135` and g++ prints nothing, and a built `.exe` dies `0xc0000139` before any test runs.
- **MSVC**: VS 2026 Community 18.1 at `C:\Program Files\Microsoft Visual Studio\18\Community`
  (cl 19.50). Zengine's MSVC lane needs `VsDevCmd.bat -arch=x64` loaded into the shell (its
  `INCLUDE`/`LIB`/`LIBPATH`/`PATH`); `Enter-VsDevShell` is not a substitute (it needs `vswhere` on
  `PATH` and fails while appearing to continue). The Windows trees in Zengine are `build-win-jx`
  (MinGW) and `build-msvc-p1` (MSVC); the working MSVC Loom prefix is Loom `build-msvc-p1/_install`
  — Debug AND `LOOM_ENABLE_WINDOWS_KERNEL=ON` (a Release install links as `LNK2038` mismatches; a
  kernel-less install makes configure silently skip every weave).
- **Git remote operations run from the Windows Bash tool, never WSL**: the SSH key exists only at
  Windows `~/.ssh/id_ed25519`. `gh` is not installed; the Actions API is readable unauthenticated
  for job conclusions, not for logs.
- **The Bash tool** is Git Bash: its `python` is Windows Python, its `/tmp` is not WSL's, and WSL's
  `/tmp` does not survive between tool calls; `perl -0pi` cannot rename its work file on `/mnt/g`;
  a heredoc of ~190 lines or more fails with `unexpected EOF`; `wsl -e bash <script>` has its
  `/mnt` paths mangled by MSYS — go through `bash -lc`. WSL kills `nohup`/`disown` when the last
  client exits, so a long harness needs a detached `wsl.exe` client.
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
- **The MSYS2 toolchain at `C:\msys64x\mingw64`** (g++ 15.2, binutils 2.45) is the local road to a
  full MinGW lane: its binutils clear the 2.40 ceiling that stops CLion's bundled MinGW from
  assembling `workshop.cpp`; a Loom built by it and a fresh Zengine tree are still owed.
- **The harness collapses `\\` to `\` in a command before the shell sees it**, so a `\b`
  written as `\\b` reaches Python or printf as a backspace (measured 2026-09-03: a
  single-quoted `'x\\b'` arrived in Python as one backslash). Text that must carry a
  backslash goes through a file written by a tool, never through the command line.
