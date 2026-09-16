# PadRemote downloads

Official PadRemote Host release downloads. This repository contains release artifacts and download information only; application source code is maintained separately.

[Download Host 0.12.0 engineering preview](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.12.0). Windows users can select the Setup installer for Intel/AMD (amd64) or Windows on ARM (arm64). Setup offers a directory choice, Start Menu shortcuts and removal through Windows Installed Apps. Uninstall stops Host and removes program files and update caches while preserving settings and project files. Portable archives remain available for Windows, macOS and Linux.

Host 0.12.0 checks for new stable versions and displays an Update button. It downloads and installs only after you select Update and confirm. Cancel leaves Host unchanged. Updating restarts Host and stops current connections and terminals, so save your work first. Failed updates are not automatically retried. A failed startup restores the previous version.

Pre-releases are not offered by the stable update channel. Older 0.11.x previews used background downloads and idle installation; install 0.12.0 to use the confirmation-based behavior. Versions 0.10.1 and earlier need a first manual installation.

The updater verifies an Ed25519-signed manifest and SHA256 digests. This signature is separate from Windows Authenticode and Apple Developer ID/notarization. The 0.12.0 engineering preview is not OS publisher-signed; release notes describe platform testing limits. Windows x64 installation and removal were tested locally; Apple native checks were skipped.

Only download artifacts from this repository's Releases. No GitHub account or access token is needed. Never provide AI credentials, project contents or Host configuration files to this repository.
