# PadRemote downloads

[Download PadRemote Host 0.20.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.20.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing or removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**New in 0.20.0:** conversation file references with text, Markdown, image and PDF previews; read-only approval for files outside projects; bounded file replay and downloads; diagnostic logs and retention controls; file-diff navigation; voice submission acknowledgement; Claude Code/Codex task completion notifications and notification settings recovery. This release fixes duplicate notifications, notification opt-out retries, notification launch routing, password-change revocation and compact JSON settings. Client-side features require a compatible updated App. Host installation does not update Android or iPad Apps.

**Update behavior:** Host 0.12.0 and newer display an update notice. Download and installation start only after you press Update and confirm. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation and uninstall integration.

Windows executables and installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Validation includes six platform/CPU builds and archive checks; Unix installer payload and structure checks; Linux amd64 DEB/RPM installation, reinstallation and removal; four-language management-page update checks; and native Windows/Linux amd64 update handoffs using anonymous downloads. macOS/iPad and ARM64 runtime checks were skipped. Real APNs/FCM delivery and mobile notification cold-launch taps remain unverified. Android QA APKs are separate test builds, not store releases; no Android or iPad store release is included. Cross-compilation and package structure checks do not establish native platform acceptance.

Only download artifacts from this repository's Releases. No GitHub account or access token is needed to download public releases. Never provide AI credentials, project contents or Host configuration files to this repository.
