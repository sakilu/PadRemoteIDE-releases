# PadRemote downloads

[Download PadRemote Host 0.16.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.16.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing/removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**What is new in 0.16.0:** the Host finds `whisper-cli` where it is installed, not only on PATH: the unzipped Windows release under `%LOCALAPPDATA%\Programs\whisper.cpp` or `%ProgramFiles%\whisper.cpp`, Homebrew on macOS, `/usr/local/bin` and source builds under `~/whisper.cpp/build/bin`, or the `whisper/` folder of the Host settings directory. The management page's Voice input section shows what it found or the folders it searched with install steps, and gains two fields to name a `whisper-cli` and a model file kept elsewhere (no need to copy a 1.6 GB model). Adding whisper-cli to PATH still needs a Host restart; the other ways do not. In the app, saved commands no longer take a row of their own: a ☆ key beside the attachment button opens a panel over the terminal, a tap runs a command and closes it, a long press on ☆ saves the line being typed. "Back to the latest output" now also brings a full-screen program such as Claude Code back to its last line. Voice input (0.15.0) is unchanged otherwise.

**Update behavior:** Host 0.12.0 and newer check for a release and display Update. Download and installation start only after you press Update and confirm. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation/uninstall integration.

0.16.0 is available on the stable update channel at the publisher's request. Windows EXE/installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Linux x64 DEB/RPM lifecycle tests passed in local Ubuntu/Fedora containers. macOS package structure and uninstall shell behavior were checked; native Apple testing and ARM64 runtime testing were skipped. Real 0.15.0 (prompt) and 0.11.1 (automatic) Hosts updated to 0.16.0 through this channel on Windows x64; the 0.15.0-to-0.16.0 handoff also passed on Linux x64. The whisper-cli search and path fields were exercised on Windows against a real whisper.cpp build; the macOS and Linux search folders have unit tests only. See the release notes for exact validation limits. Do not interpret cross-compilation as native platform acceptance.

Only download artifacts from this repository's Releases. Never upload AI credentials, private projects, Host settings or signing keys here.
