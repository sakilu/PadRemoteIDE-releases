# PadRemote downloads

[Download PadRemote Host 0.18.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.18.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing/removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**What is new in 0.18.0:** resident desktop controls on Windows, macOS and supported Linux desktops. The menu shows live service status and offers Start service, Stop service, Open management page, Settings and Quit. Closing the browser keeps Host running; reopen the page from the icon without remembering its port. Stopping service keeps the resident app available for restarting. Windows includes the branded icon in portable and updated builds, macOS uses a PR menu-bar item, and Linux uses StatusNotifierItem/DBusMenu with desktop shortcut actions as a fallback. On desktops without a compatible tray, reopening PadRemote Host from the application menu always returns to the current management page. Menu labels follow the management page's Traditional Chinese, Simplified Chinese, English or Japanese language setting.

**Update behavior:** Host 0.12.0 and newer check for a release and display Update. Download and installation start only after you press Update and confirm. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation/uninstall integration.

0.18.0 is available on the stable update channel at the publisher's request. Windows EXE/installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Validation for 0.18.0: shared service lifecycle and single-instance tests, Windows native tray lifecycle/action dispatch, Linux isolated D-Bus registration/actions/status updates/panel re-registration, and four-language management-page checks passed. All six platform/CPU builds and archive integrity checks passed; Unix installer payloads, permissions, licenses and Linux desktop entries passed structural checks. All 16 GitHub asset digests match the verified local files; the anonymous latest manifest and Windows package download passed signature, hash and extraction checks. Native macOS/ARM64 runs, real Linux desktop appearance, extra Windows visual inspection and full installer lifecycle reruns were skipped. No new mobile builds were published. See the release notes for exact limits; cross-compilation is not native platform acceptance.

Only download artifacts from this repository's Releases. Never upload AI credentials, private projects, Host settings or signing keys here.
