# PadRemote downloads

[Download PadRemote Host 0.23.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.23.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing or removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**New in 0.23.0:** Voice input's recording cutoff is widened from 60 seconds to 3 minutes. The tablet Settings screen can also show when a newer Host is available and, once you opt in, trigger the update directly from the tablet using the same confirmed-install path as the desktop; the Host restarts and every connected device briefly disconnects and reconnects automatically. This is a Host-only release: the mobile App is unchanged.

**Update behavior:** Host 0.12.0 and newer display an update notice. Download and installation start only after you press Update and confirm; from 0.21.0 you may also turn on auto-update in the status bar menu or management page, in which case a release installs while the Host is idle. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation and uninstall integration.

Windows executables and installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Validation includes six platform/CPU builds and archive checks; Unix installer payload and structure checks with a stubbed macOS shell lifecycle; Linux amd64 DEB/RPM installation, reinstallation and removal against a running 0.22.0 Host; native Windows/Linux amd64 0.22.0 → 0.23.0 update handoffs using anonymous downloads; the stable channel from 0.12.0 (prompt) and 0.11.1 (automatic); Go tests, `flutter analyze` and 205 Flutter tests; and four-language catalog checks. Windows installer lifecycle QA, macOS menu bar rendering, and macOS/iPad and ARM64 runtime checks were skipped. Real APNs/FCM delivery remains unverified. No new Android QA build accompanies this release; the Android QA download below remains 0.21.0+31. No Android or iPad store release is included. Cross-compilation and package structure checks do not establish native platform acceptance.

**Android QA download:** [0.21.0+31 test APKs](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/android-qa-v0.21.0-build31), for armeabi-v7a, arm64-v8a and x86_64. These use a separate `.qa` package ID and debug signing. They are not Google Play releases. iPhone/iPad builds are not included.

Only download artifacts from this repository's Releases. No GitHub account or access token is needed to download public releases. Never provide AI credentials, project contents or Host configuration files to this repository.
