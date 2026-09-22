# PadRemote downloads

[Download PadRemote Host 0.26.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.26.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing or removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**New in 0.26.0:** Fixes the tablet's Settings > Check for updates causing an endless disconnect/reconnect loop. Host 0.25.0 and earlier did not accept the update-status request over the peer connection and closed the connection instead; 0.26.0 answers it, replies 404 to unknown routes without dropping the connection, and advertises `host-update-v1` so newer Apps only ask Hosts that support it. Update Host on the computer first; existing iPad/Android Apps then check for updates without disconnecting. No App release is included in this version.

**New in 0.25.0:** Long voice proofreading uses a larger input-dependent output budget and rejects unfinished or truncated results, retaining the original transcription. Local release-binary tests preserved all 468 characters from two minutes and 704 from three minutes with proofreading enabled. The HTTP upload budget accommodates Base64-encoded three-minute audio. Codex standalone report links rendered as caption (file path) are recognized. The Android QA App now checks conversation files automatically, removes confirmed missing entries, and opens previews by tapping redesigned cards.

**Update behavior:** Host 0.12.0 and newer display an update notice. Download and installation start only after you press Update and confirm; from 0.21.0 you may also turn on auto-update in the status bar menu or management page, in which case a release installs while the Host is idle. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation and uninstall integration.

Windows executables and installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Validation for 0.26.0 includes six platform/CPU builds and archive checks; final Windows EXE/ZIP/Setup Defender scans with security intelligence 1.459.328.0 (real-time protection enabled, no exclusions); Linux amd64 DEB/RPM installation, reinstallation and removal against 0.25.0; ARM64 package structure and macOS PKG structure/simulated shell lifecycle checks; Go and Flutter regression suites including a new peer-route test that reproduces the disconnect loop; anonymous public-download handover from 0.25.0 on Windows and Linux amd64; and the public update channel from 0.12.0 (prompt) and 0.11.1 (automatic). Disposable Windows installer lifecycle QA, macOS/iPad and ARM64 runtime checks, and tablet re-verification were skipped. No Android or iPad store release is included. Cross-compilation and structure checks do not establish native acceptance.

**Android QA download:** [0.25.0+35 test APKs](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/android-qa-v0.25.0-build35), for armeabi-v7a, arm64-v8a and x86_64. These use a separate `.qa` package ID and debug signing. They are not Google Play releases. iPhone/iPad builds are not included; updating Host does not update the mobile App.

Only download artifacts from this repository's Releases. No GitHub account or access token is needed to download public releases. Never provide AI credentials, project contents or Host configuration files to this repository.

