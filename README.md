# PadRemote downloads

[Download PadRemote Host 0.17.0](https://github.com/sakilu/PadRemoteIDE-releases/releases/tag/v0.17.0). No GitHub account is required. This repository contains downloads and release information only; source code is maintained separately.

| Platform | Installer | Default program location | Uninstall |
| --- | --- | --- | --- |
| Windows Intel/AMD or ARM64 | matching Setup `.exe` | `%LOCALAPPDATA%\Programs\PadRemote Host` | Windows Installed Apps or Start Menu |
| macOS Intel or Apple Silicon | matching Setup `.pkg` | `~/Applications/PadRemote Host.app` | open `~/Applications/Uninstall PadRemote Host.app` |
| Debian/Ubuntu amd64 or arm64 | matching Setup `.deb` | `/opt/padremote-host` | `sudo apt remove padremote-host` |
| Fedora/RHEL-compatible x86_64 or aarch64 | matching Setup `.rpm` | `/opt/padremote-host` | `sudo dnf remove padremote-host` |

On Linux, open the package with your software installer or run `sudo apt install ./PACKAGE.deb` / `sudo dnf install ./PACKAGE.rpm`. Launch from the application menu or run `padremote-host` as your normal user. macOS PKG installs for the current user. Save your work before installing/removing: the flow stops Host and its terminals. Settings and projects are preserved. Custom settings locations remain user-managed; exit those Host instances before removing the package.

**What is new in 0.17.0:** a language model running on your own computer can proofread what whisper heard. Speech recognition mishears project names and homophones ("佛拉特" for flutter, "speech input button 點 dart" for `speech_input_button.dart`); the Host can now hand each transcript, with the project's file names, to a small instruction model in llama.cpp's `llama-server`, which fixes only recognition mistakes, punctuation and spellings of names, never the wording or meaning, and neither answers nor carries out what was said. The transcript stays on your computer unless you point the Host at a server elsewhere. The management page's new Voice proofreading section finds `llama-server` where it is installed, offers Gemma 4 E4B-it (recommended), Qwen3.5-4B and Gemma 4 E2B-it for download from fixed Hugging Face revisions verified with SHA256, and takes the path of a server, model or an OpenAI-compatible server you already run (llama-server, LM Studio, Ollama). The app's settings gain a per-tablet switch, on by default but locked while the Host has no model; every proofread transcript is marked in the review and can be switched back to whisper's own text with one tap. Proofreading adds about 0.2–0.3 s on a GPU or 1–3 s on a four-core CPU; the first run of a CUDA build may take a minute while the driver compiles kernels. Hosts without a model, and clients before 0.17.0, behave exactly as before.

**Update behavior:** Host 0.12.0 and newer check for a release and display Update. Download and installation start only after you press Update and confirm. Older 0.11.x previews automatically update when idle. Versions 0.10.1 and earlier need an initial manual installation. Portable archives remain portable after an update; run Setup once to obtain OS installation/uninstall integration.

0.17.0 is available on the stable update channel at the publisher's request. Windows EXE/installers are still unsigned, and macOS packages are not Developer ID signed or notarized. The Ed25519-signed update manifest and SHA256 sums verify update integrity but do not remove OS publisher warnings.

Linux x64 DEB/RPM lifecycle tests passed in local Ubuntu/Fedora containers. macOS package structure and uninstall shell behavior were checked; native Apple testing and ARM64 runtime testing were skipped. Real 0.16.0 (prompt) and 0.11.1 (automatic) Hosts updated to 0.17.0 through this channel on Windows x64; the 0.16.0-to-0.17.0 handoff also passed on Linux x64. Voice proofreading was exercised on Windows against a real llama-server (CUDA build) with Gemma 4 E4B-it and on the Host's management API; real recordings through a tablet, macOS native runs and the native Android/iPad flows were not tested for this release. See the release notes for exact validation limits. Do not interpret cross-compilation as native platform acceptance.

Only download artifacts from this repository's Releases. Never upload AI credentials, private projects, Host settings or signing keys here.
