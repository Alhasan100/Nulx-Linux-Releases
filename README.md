# Nulx Linux Releases

The official release information, download verification and beta-feedback repository for **Nulx Linux**.

> **Not released:** no public beta or approved ISO is available. Downloads will be announced here only after release validation and signing are complete.

## What is Nulx Linux?

Nulx Linux is an independent Debian 13-based desktop distribution built around KDE Plasma 6 and a coherent Nulx visual identity. It is designed for cybersecurity learning, authorized offensive and defensive workflows, system administration, development, and everyday desktop use. It is not a Kali Linux derivative or reskin.

Development includes Nulx Launcher, Terminal, Command Center and Nulx AI with a local Offline Guide. The tool registry describes planned capabilities, not proof that every tool is installed. Only features verified in the signed ISO will appear as supported in its release notes.

Seven tool routes remain under review. Installed-system Secure Boot, signed updates and live-account features also require acceptance testing before the beta is ready.

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

Nulx Linux was created by **Alhasan Al-Hmondi** and is being developed with a security-first, release-gated process.
