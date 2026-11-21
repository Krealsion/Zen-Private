The founder's PC, as the restore round measured it on 2026-11-21 (`reportbacks/machine-restore-RB.md`
once filed): its old system drive died on 2026-11-15, and a new one carries a fresh Windows 11.
What holds from before is kept here with its date; what went with the old drive is in that
report's "What was lost".

- **CPU**: Ryzen 9 7900X, 12 physical cores / 24 threads. On the old drive `-j24` was the best
  measured build parallelism and `-j32` slower (2026-09-30); the job counts the kit runs at are its
  README's ("The build slots"), measured here 2026-11-21.
- **Memory**: 63.1 GB visible to Windows. WSL is given 48 GB by `C:\Users\Joshua\.wslconfig`
  (`memory=48GB`, `guiApplications=false`, `networkingMode=mirrored`) and reads `MemTotal`
  49,331,128 kB (47.0 GB) with a 12 GB swap file, so a build on Windows has what WSL's VM leaves
  of the host. WSL's VM keeps what its builds used for minutes after they end (38.4 GB of the
  host's 59.7 GB used, after slot-1's sanitizer build, 2026-11-21), so a Windows build asked then
  waits for the host's memory (two did, 233 and 239 s): `autoMemoryReclaim` in `.wslconfig`'s
  `[experimental]` section is the founder's switch for that.
- **Disks**: C: is the new system drive, a 6.4 TB NVMe (HUSMR7664BHP301, 5,961 GB NTFS, 4 KB
  clusters), and holds both of the kit's roots: the Windows root `C:\Users\Joshua\zen-build` and
  WSL's ext4 disk (1007 GB, `/dev/sdd`). G: ("Gargandos", an SSK 1 TB SSD on USB) is exFAT with
  256 KB clusters and holds Zen at `G:\programming\cpp\Zen`; no slot, tree, prefix, cache or session
  root is on it. F: is a letter with no medium. H: is gone.
- **G: (exFAT on USB) costs**: a file takes at least 256 KB of disk (104,259 small files of 0.9 GB
  held about 25 GB, 2026-10-04); junctions and symlinks cannot exist there; Windows programs see
  2-second file times and WSL whole seconds, so a source rewritten in the second its object compiled
  looks older than the object (a tool that rewrites sources and rebuilds at once waits past a second
  boundary); a served Loom session refuses a root there (no permissions). A Windows tree's disk
  decides its build: on the old C: a warm MinGW-w64 build took 23.9 s against 328.3 s with the tree
  on G:, a cold one 264.8 s against 532.0 s (`reportbacks/c-drive-builds-RB.md`, 2026-10-10).
- **Windows**: Windows 11 Pro 24H2, build 26100, user `Joshua`; Windows PowerShell 5.1; Defender's
  real-time protection on (its exclusions need an administrator to read); no Microsoft Store and no
  winget, so every tool comes from its own site. One display measured, 1920x1080 at (0,0). Not
  installed: Visual Studio (no local MSVC), CLion, .NET, AutoHotkey, DisplayFusion.
- **Windows tools** (the founder's installs, 2026-11-21): Git for Windows 2.56.1 (Git Bash, bash
  5.3.15; its `git` is `/ucrt64/bin/git`); the GitHub CLI 2.105.0 in `C:\Program Files\GitHub CLI`;
  CMake 4.5.1 in `C:\Program Files\CMake`; Python 3.15.2 at `C:\Python315` (`python` and `py`; there
  is no `python3` on Git Bash's `PATH`); Node.js 26.13.1 LTS; MSYS2 at `C:\msys64x`, whose
  `mingw64` holds g++ 16.2.0 Rev7, binutils 2.47, ccache 4.14.3 and Ninja 1.13.2 (`pacman -Q`).
  That Ninja is the only one on Windows: the kit puts `C:\msys64x\mingw64\bin` first on `PATH` for
  every Windows build, which also keeps a MinGW-w64 program from loading Git for Windows'
  `libstdc++-6.dll`, and its programs need that `bin` on `PATH` to run at all (without it a built
  `.exe` dies `0xc0000139` before any test runs).
- **WSL**: Ubuntu 22.04.5 on kernel 6.18.58.1, user `joshua` (`/etc/wsl.conf`: systemd on, default
  user `joshua`); `sudo` needs a password. The build set is the distribution's: GCC 11.4.0, CMake
  3.22.1 (the floor a CMake feature must clear), Ninja 1.10.1, ccache 4.5.1, Python 3.10.12 as
  `python3` only (no `python`), tmux 3.2a, Git 2.34.1 and `/usr/bin/time`, with Zengine's Linux
  build set (`package.yml`'s `BUILD_SET`). No `gh`, Node or gdb (`hang-wsl.sh` needs gdb). `~/opt/`
  is WSL's home for tools apart: the Neovim 0.11.6 Zengine's `ci.yml` pins, by its checksum, in
  `~/opt/nvim-0.11.6/` (2026-11-21). drvfs mounts C: and G: as 9p with no `metadata`; `/mnt/wsl`
  is a 24 GB tmpfs every distribution shares, where the kit's build-slot lock lives. Yama
  `ptrace_scope` is 1.
- **The kit's slots** (constitution § c; `Zen/pass-tools/executor-kit/`, its README): `slot-1`,
  `slot-2` and `slot-3` under `C:\Users\Joshua\zen-build` (each slot's Zengine and Loom clones and
  its Windows trees) and under WSL's `~/zen-build` (the clones' ext4 copies and the WSL trees), with
  one compile cache a side beside them (`ccache`, 24 GB cap each). Made 2026-11-21: each clone came
  from GitHub over HTTPS (Zengine in 7 to 8 s, Loom in 2 to 3 s), with every local branch of the old
  primary's clones in `Zen/primary/` carried (13 in Zengine, `main` among them, and 1 in Loom) and
  the relicense guard as its `pre-push` hook. Built 2026-11-21 at Zengine `fadd33f4` and Loom
  `beb74e2`: slot-1 cold (Loom's prefixes 29 s on Windows, 25 s in WSL; the official WSL tree 797 s
  and the sanitizer's 1749 s in a work build slot at 8 jobs under the compile gate, WSL's used
  memory peaking at 13.2 and 13.3 GB; the MinGW-w64 tree 493 s at 8 jobs, its build processes
  peaking at 21.1 GB of the host's, its largest a 7.3 GB link; the SDL tree 124 s), then slot-2 and
  slot-3 at once, warm from the stores (official 106 s each, sanitizer 138 and 149 s, MinGW-w64 90
  and 81 s, SDL 102 s each; WSL's used memory peaked at 12.0 GB), then slot-2 moved to `main`
  again with nothing changed, 28 s whole. A slot holds about 30 GB in WSL and 9 to 11 GB on
  Windows.
- **Zen's checkout** is kept by Git for Windows' own `core.autocrlf=true` (its system gitconfig):
  13,048 tracked files have CRLF in the working tree and LF in the index, 3,859 LF in both, 283 CRLF
  in both, and the status is clean; a commit from Git Bash writes LF. So Git runs on Zen and
  `Zen/private` from Git Bash only, never from WSL, whose Git sets no `autocrlf` and would read
  every converted file as changed. `~/.gitconfig` holds the founder's identity and `safe.directory`
  `G:/*` (exFAT records no owner, and Git refused Zen without it). The slots' clones are LF on
  disk: Zengine's and Loom's `.gitattributes` set their line ends.
- **GitHub from this machine**: every Git remote operation runs from Git Bash over HTTPS, under
  `gh`'s login, `Krealsion` (keyring; scopes `gist`, `read:org`, `repo`, `workflow`). No SSH key
  is on this drive. The restricted agents' account, `UnknownWorkers`, has no login here yet; its
  own is to live under `GH_CONFIG_DIR="$HOME/.config/gh-unknownworkers"`, apart from the founder's.
  The Actions API answers job conclusions without a token, not logs.
- **The old MPL-2.0 histories**: besides the private `Krealsion/Loom-history` and
  `Krealsion/Zengine-history`, their only copies are the bundles in `Zen/private/relicense/` (its
  `README.md` says what each holds), on G: and ignored by `Zen/private`'s Git, so no remote holds
  them.
- **The Bash tool is Git Bash** (2026-11-21, as before): its `python` is Windows Python and it has
  no `python3`; its `/tmp` is not WSL's, and WSL's `/tmp` does not survive between tool calls; the
  harness collapses `\\` to `\` in a command before the shell sees it (measured again 2026-11-21:
  `printf '%s' 'x\\b'` printed one backslash), so text that must carry a backslash goes through a
  file written by a tool; a long heredoc fails with `unexpected EOF` (one of about 110 lines did,
  2026-11-21); Git Bash rewrites `/c` and `/J` arguments to drive paths, so `cmd.exe /c` is written
  `//c`; `wsl.exe -e bash <script>` from Git Bash needs `MSYS_NO_PATHCONV=1` or its `/mnt` paths
  are mangled; `wsl.exe bash -lc '…'` expands `$?` and `$(…)` before the inner bash runs, so a
  chain whose exit matters goes in a script; WSL ends `nohup`'d work when its last client exits, so
  a long harness keeps a `wsl.exe` client open; `bc` is not there (timing uses `$(( ))` over
  `date +%s%N`). Python's `write_text` on Windows writes CRLF, so a helper that edits a product file
  writes bytes. This harness keys its memory folder to the launch folder `G:\programming\cpp\Zen`;
  Zen keeps nothing there (`Zen/AGENTS.md`).
- **Windows' short sleeps last a scheduler tick** (measured on this hardware under the old Windows,
  2026-10-12, not again): `Sleep(1)` and a 1 ms `sleep_for` each took about 15.5 ms, a
  high-resolution waitable timer 1.5 ms for 1 and 10.2 for 10, and `GetTickCount64` steps 15 or 16
  ms.
- **tmux works as a TUI witness harness in WSL** (`send-keys -H` with raw SGR mouse bytes;
  `resize-window` drives a real resize), as before; tmux 3.2a is installed.
- **Windows console hosts** (as before, not measured again): conhost and Windows Terminal both
  deliver right-click to a mouse-enabled console app; a console client cannot resize its own window
  under Win11's default terminal.
- **SDL in WSL**: with the build set's X11 and Wayland headers, a WSL tree's SDL3 configures its
  `x11` and `wayland` video drivers beside `dummy` and `offscreen` (`SDL_X11` and `SDL_WAYLAND` ON
  in `zengine-slot-1-ext4`, 2026-11-21; before, only the last two). WSLg is off
  (`guiApplications=false`), so no window shows there: a live SDL witness runs on a Windows tree
  (each slot's `zengine-sdl`).
- **No MinGW-w64 toolchain but MSYS2's**: the toolchains' home `C:\Users\Joshua\zen-build\toolchains`
  is not made yet. The downloads of seven of the nine the old drive held survive on G:, in
  `Zen/scratch/weave-runtime-windows/dl/` (MinGW-Builds GCC 12.2.0 to 14.2.0, llvm-mingw Clang 18.1.8
  and 23.1.2), and MSYS2's GCC 16.2.0 packages in `Zen/scratch/runtime-gcc16/dl/`; MinGW-Builds
  15.2.0 and 16.2.0 are not there.
