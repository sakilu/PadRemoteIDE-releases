# PadRemote downloads

[Download PadRemote Host 0.13.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.13.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing/removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**Update behavior:** Host 0.12.0 and newer check for a release and display Update. Download and installation start only after you press Update and confirm. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation/uninstall integration.

0.13.0 is available on the stable update channel at the publisher's request. Windows EXE/installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Linux x64 DEB/RPM lifecycle tests passed in local Ubuntu/Fedora containers. macOS package structure and uninstall shell behavior were checked; native Apple testing and ARM64 runtime testing were skipped. See the release notes for exact validation limits. Do not interpret cross-compilation as native platform acceptance.

Only download artifacts from this repository's Releases. Never upload AI credentials, private projects, Host settings or signing keys here.
