# Nulx Linux

Nulx Linux is a Debian 13-based desktop in development for cybersecurity students and lab users with basic Linux knowledge. It brings organized security tools, local learning guidance and native Nulx applications into a KDE Plasma 6 desktop.

The project is designed for learning network analysis, security testing and digital investigation in your own lab or on systems you are authorized to test.

> No public beta or approved ISO is available yet. A release date has not been announced.

## Explore Nulx

- [Official website](https://nulxlinux.com/) — the project, its goals and current progress.
- [Tool catalog](https://nulxlinux.com/tools/) — browse the security tools by area of study.
- [Nulx AI](https://nulxlinux.com/nulx-ai/) — local guidance and optional online chat.
- [Documentation](https://nulxlinux.com/docs/) — getting started, lab preparation and project guides.
- [Development updates](https://nulxlinux.com/updates/) and [roadmap](https://nulxlinux.com/roadmap/) — what has been tested and what comes next.

## What is being built?

Nulx Launcher helps you find tools. Command Center brings together local system information, projects and settings. Nulx Terminal provides a workspace for command-line study, while Nulx AI offers curated offline guidance and optional chat through your own OpenAI account.

Online chat requires your consent before sending a message. Provider access and usage limits apply. No shared account or developer key is included. Approval-based actions remain under development, and Nulx AI is not an autonomous scanner or unrestricted terminal agent.

## Development status

These results describe the development installation. They do not establish the behavior or compatibility of a future release.

- All 64 catalog tools are installed and have passed executable startup checks. Complete tool workflows still need wider testing.
- Native Launcher, Command Center, Terminal and Nulx AI applications are under active development.
- Tested Nulx app package upgrades retained existing user data without reinstalling the operating system.
- Selected wordlists are installed. Full SecLists and original RockYou coverage remain under review.

Before an ISO can be released, the project still needs final-image installation and reboot testing, hardware and VM validation, accessibility checks, licensing and source-delivery review, and approved signing. The public signed update channel is not configured.

## Downloads and verification

Future approved downloads will be recorded on the official [GitHub Releases page](https://github.com/Alhasan100/Nulx-Linux-Releases/releases). GitHub's automatic source archives contain this public repository's documentation and configuration, not a bootable Nulx image.

Before booting a future ISO, follow [Verify a download](docs/VERIFY-DOWNLOAD.md). Check its SHA-256, detached signature and signed manifest from the same official release. The guide also describes the required release files and signing process. Do not use ISO files from issue attachments or unofficial mirrors.

Releases are prepared as drafts. Only a successful manual run publishes the prepared draft. Public release signing is still awaiting approval.

## Feedback and support

Documentation corrections are welcome now. Read [Contributing](CONTRIBUTING.md) for the public contribution process. Once an approved beta is available, use the [beta testing guide](docs/BETA-TESTING.md) and [support guide](SUPPORT.md) to submit a useful installation, compatibility or bug report.

Read [Privacy and redaction](docs/PRIVACY-AND-REDACTION.md) before sharing logs or screenshots. Report suspected vulnerabilities through [GitHub private vulnerability reporting](https://github.com/Alhasan100/Nulx-Linux-Releases/security/advisories/new), following [SECURITY.md](SECURITY.md).

## Repository and licensing

This repository is intentionally separated from the private engineering repository. It contains public release information, verification guidance and feedback channels. Product source, private build files and internal test records are not stored here.

The repository documentation and configuration use the [MIT License](LICENSE). Software in a future ISO keeps its own licenses, notices and corresponding-source obligations.

Nulx Linux was created by [Alhasan Al-Hmondi](https://nulxlinux.com/about/#creator). Learn more about the project on the [About page](https://nulxlinux.com/about/).
