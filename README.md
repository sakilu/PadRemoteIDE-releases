# PadRemote AI downloads

[Download the latest PadRemote AI Host](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately. Each release lists its own changes.

User guide (English, 日本語, 正體中文, 简体中文): <https://pad-remote-ai.sakilu.com/>

| Platform | Installer (latest stable) | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows x64 | [PadRemote-Host-Setup-windows-amd64.exe](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-windows-amd64.exe) | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| Windows ARM64 | [PadRemote-Host-Setup-windows-arm64.exe](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-windows-arm64.exe) | same as above | same as above |
| macOS Intel | [PadRemote-Host-Setup-darwin-amd64.pkg](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-darwin-amd64.pkg) | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| macOS Apple Silicon | [PadRemote-Host-Setup-darwin-arm64.pkg](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-darwin-arm64.pkg) | same as above | same as above |
| Debian/Ubuntu amd64 / arm64 | [amd64 .deb](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-linux-amd64.deb) · [arm64 .deb](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-linux-arm64.deb) | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 / aarch64 | [x86_64 .rpm](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-linux-amd64.rpm) · [aarch64 .rpm](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/PadRemote-Host-Setup-linux-arm64.rpm) | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

Checksums: [SHA256SUMS.txt](https://github.com/sakilu/PadRemoteIDE-releases/releases/latest/download/SHA256SUMS.txt). Portable archives are also attached to each release.

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. The macOS package installs for the current user and requires macOS 13 or later. Save your work before installing or removing: the flow stops Host and its terminals. Settings and projects are preserved.

**Before you start:** install Git and the AI CLI you want to use (Claude Code, Codex CLI, Grok Build, Antigravity CLI or GitHub Copilot CLI) and sign in on that computer as the same user who runs Host. On the phone or tablet, sign in to the PadRemote AI App, then enter the connection code and password shown on the Host management page, or scan its QR code. Connections are encrypted; the App connects directly when possible and otherwise falls back automatically to an encrypted relay.

**Updates:** Host checks for a newer stable release once after it starts, and again when a connected App asks it to. It only shows a notice; nothing downloads or installs until you press Update and confirm. Updates are verified with an Ed25519-signed manifest and SHA256; if the new version fails to start, the previous one is restored. Updating Host does not update the mobile App.

Windows executables and installers are still unsigned, and macOS packages are not Developer ID signed or notarized, so the operating system may show publisher warnings.

Only download artifacts from this repository's Releases. Never provide AI credentials, project contents or Host configuration files to this repository.
