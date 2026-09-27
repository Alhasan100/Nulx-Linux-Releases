# Nulx Linux Releases

The official release information, download verification and beta-feedback repository for **Nulx Linux**.

> **Not released:** no public beta or approved ISO is available. Downloads will be announced here only after release validation and signing are complete.

## What is Nulx Linux?

Nulx Linux is a Debian 13-based desktop built around KDE Plasma 6 for cybersecurity students and lab users with basic Linux knowledge. It brings together organized security tools, learning guidance, and a consistent Nulx interface. Use it for study and practice on systems you own or have permission to test.

Development includes Nulx Launcher, Terminal, Command Center, and Nulx AI with local guidance and optional online chat. A tool's catalog entry does not mean it is installed. Release notes will describe the features and platforms tested with that specific image.

## Development status

Updated September 27, 2026. These results come from a development installation, not a released ISO.

**All 64 catalog tools are installed and have passed executable startup checks.** Launcher identifies all 64 as installed. The public beta remains unreleased.

| Area | Verified on the development system | Before public release |
| --- | --- | --- |
| Tools | 64/64 installed, with help or version startup checks for every executable | Complete workflow coverage, redistribution review and fresh-ISO retention |
| Functional tests | Owned-data tests for Ghidra, Radare2, Zeek, Nmap and mitmproxy. Ordinary-user Firejail isolation and AppArmor checks | Broader tool, runtime-data and hardware testing |
| Desktop | One top panel with the categorized menu, app shortcuts and virtual desktops. It survives a desktop-shell restart | Final-image reboot, keyboard, accessibility and multi-display checks |
| Themes | All five themes passed installed KDE visual smoke checks, including Spectrum neon borders and translucent Terminal | Chooser layout and complete visual acceptance. Obsidian remains the product default |
| Nulx apps | Launcher and Command Center are separately packaged. Menu routes start actual tools | Complete click-through testing and final-image integration |
| Nulx AI | Single-window guidance and online chat. Earlier real sign-in, learning reply and reconnection checks. In-place app and runtime upgrades | Account expiry, revocation, secure storage and end-to-end reviewed-action acceptance |
| Package safety | Dependency and package-state checks passed. Existing service safeguards are intact, with no new running services or listening endpoints | Current license inventory, signed updates and recovery coverage |
| Boot and platforms | Earlier Hyper-V installation and direct-disk boot checks. Secure Boot enabled on the tested installation | Final candidate in Hyper-V and VirtualBox, kernel updates and physical hardware |
| Public beta | No approved ISO or release date | Remaining stability, licensing, source-delivery, signing and publication gates |

Startup checks confirm that executables run. They do not mean every feature has been exercised, every service is enabled, or every tool needs no configuration. The functional tests used owned data and isolated local fixtures, not public targets.

### What happens next

1. Complete third-party notices and required source documentation. The current Zeek packages lack the Debian license records required by the inventory check. The older inventory is not current.
2. Integrate accepted packages and organized wordlists into reproducible ISO inputs.
3. Test fresh installations, tool retention, app workflows, updates, reboot, accessibility and supported hardware.
4. Publish known limitations, signed verification material and an approved ISO only after the release gates pass.

No ISO was built or published for this milestone. Older development updates retain their original dates and test scope.

Online chat uses the user's own account and requires consent before sending messages. Provider access and usage limits apply. Nulx AI is not an unrestricted vulnerability scanner or autonomous desktop agent. No shared account or developer key is included.

See the [September 27 test summary](https://nulxlinux.com/updates/#all-64-tools-installed), [complete tool catalog](https://nulxlinux.com/tools/), [real app captures](https://nulxlinux.com/screenshots/), and [remaining roadmap](https://nulxlinux.com/roadmap/).

## Purpose of this repository

This repository is intentionally separated from the private engineering repository. It is limited to:

- The canonical release record, official ISO download location, and verification material
- Public beta documentation
- Installation, hardware-compatibility, and defect reports
- Coordinated private reporting of security vulnerabilities

It does **not** publish the Nulx Linux product source tree, private build pipeline, internal CI, raw test evidence, VM images, credentials, or developer logs. GitHub's automatic source archives contain only the public documentation and repository configuration stored here.

## Downloads

Start at the [Releases page](https://github.com/Alhasan100/Nulx-Linux-Releases/releases). It will provide the official version record, verification files and approved ISO link. Large ISOs may be hosted separately from GitHub's release assets.

Cloudflare R2 Standard and `downloads.nulxlinux.com` are the planned download service, not an active or approved release channel. A hostname alone does not establish authenticity. Use only the exact ISO URL, byte size and SHA-256 recorded in the official Release's signed manifest.

Each approved release must include:

| Artifact | Purpose |
| --- | --- |
| `Nulx-Linux-<version>-amd64.iso` | Bootable image, hosted directly when eligible or at the signed official download URL |
| `.iso.sha256` | SHA-256 integrity checksum |
| `.iso.sig` or `.iso.asc` | Detached release signature |
| `Nulx-Linux-<version>-SBOM.spdx.json` | Sanitized software bill of materials |
| `Nulx-Linux-<version>-THIRD-PARTY-LICENSES.txt` | Third-party licensing and source-offer information |
| `Nulx-Linux-<version>-RELEASE-NOTES.md` | Verified changes, limitations, and test coverage |
| `Nulx-Linux-<version>-MANIFEST.json` | Sanitized filename, URL, size, architecture, and artifact hashes |
| `Nulx-Linux-<version>-MANIFEST.json.asc` | Detached signature for the release manifest |

Never download a Nulx Linux ISO from an issue attachment, pull request, unofficial mirror, or link posted by another user. Start from the official Release, follow only the ISO URL recorded in its signed manifest, and complete [Verify a download](docs/VERIFY-DOWNLOAD.md) before booting it.

### Release safety process

Releases are prepared as drafts. After all required assets are attached to the draft, the owner runs the repository's manual **Public repository boundary** workflow. The workflow refuses to continue unless it can verify the public release key, manifest signature, companion hashes and contents, complete ISO byte size and SHA-256, and detached ISO signature. Only a successful manual run publishes the prepared draft. GitHub release immutability is enabled so future published assets and their tag cannot be replaced silently.

The public signing key has not been generated and approved yet. Until it is added at `keys/nulx-release-public-key.asc` and its fingerprint is published through an independent official channel, release validation intentionally fails.

## Test and report

- Read the [Beta testing guide](docs/BETA-TESTING.md).
- [Report a general bug](https://github.com/Alhasan100/Nulx-Linux-Releases/issues/new?template=bug-report.yml).
- [Report an installation problem](https://github.com/Alhasan100/Nulx-Linux-Releases/issues/new?template=installation-report.yml).
- [Submit a hardware or VM compatibility result](https://github.com/Alhasan100/Nulx-Linux-Releases/issues/new?template=hardware-compatibility.yml).
- Read [Privacy and redaction](docs/PRIVACY-AND-REDACTION.md) before attaching diagnostics.

Security vulnerabilities must not be posted publicly. Use [GitHub private vulnerability reporting](https://github.com/Alhasan100/Nulx-Linux-Releases/security/advisories/new) as described in [SECURITY.md](SECURITY.md).

## Responsible use

Nulx Linux security functionality is intended only for systems you own or are explicitly authorized to test. Users are responsible for complying with applicable laws, contracts, and rules of engagement.

## Licensing

The repository documentation and configuration are licensed under the [MIT License](LICENSE). That license does not replace the individual licenses of software distributed inside a future ISO. Every upstream component keeps its own license, notices, and corresponding-source obligations.

## Credit

Nulx Linux was created by **[Alhasan Al-Hmondi](https://nulxlinux.com/about/#creator)**. Read about the project and its goals on the official website.
