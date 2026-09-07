# Security Policy

## System and scope

This repository is the public distribution, verification, documentation, and beta-feedback surface for Nulx Linux. It does not contain the private Nulx Linux engineering repository or build environment.

Security coverage includes:

- Official GitHub Releases and downloadable Nulx Linux artifacts
- Checksums, signatures, public signing keys, SBOMs, manifests, license bundles, and release notes
- Repository settings, issue forms, and public-boundary validation
- Security defects that affect a currently supported, official Nulx Linux ISO

No public beta has been released yet, so no Nulx Linux version is currently supported through this repository.

## Report a vulnerability privately

Do not create a public issue for a suspected vulnerability. Use [GitHub private vulnerability reporting](https://github.com/Alhasan100/Nulx-Linux-Releases/security/advisories/new).

Include only the information needed to assess the problem:

- Affected release tag and the ISO SHA-256 you verified
- Realistic impact and required attacker access
- Minimal, safe reproduction steps
- Sanitized logs or screenshots
- Whether any details are already public

Never submit passwords, API tokens, cookies, private keys, personal data, client information, live third-party target data, or weaponized proof-of-concept material. Do not test against systems or people without explicit authorization.

No response-time or disclosure-time commitment is promised until a formal security response process is published.

## Reportable security findings

Examples include:

- An official artifact that does not match its checksum, signature, or manifest
- Release-channel, tag, workflow, or download-link takeover
- Accidentally published credentials, private source, internal artifacts, or sensitive diagnostics
- Verification instructions that accept a substituted or invalid artifact
- Unsafe repository automation that exposes privileged credentials to untrusted contributions
- Installer, boot, update, authentication, privilege-boundary, or insecure-default defects in a supported official ISO
- A Nulx-specific integration that materially increases the impact of an upstream vulnerability

Compromise of signing or release authority, embedded credentials, reliable default-install remote code execution, or reliable root compromise is treated as potentially critical or high severity.

## Publication invariants

The following rules are mandatory:

1. This repository has a new, unrelated Git history. It must never fork, mirror, submodule, or add the private engineering repository as a remote.
2. Only explicitly allowlisted public documentation, issue forms, and boundary configuration may enter Git.
3. ISO images are immutable official release artifacts referenced by the signed manifest, never Git blobs or Git LFS objects. When an ISO exceeds GitHub's per-file limit, its approved HTTPS URL, byte size, SHA-256, and detached signature must still be recorded in the canonical GitHub Release.
4. No ISO may be published before release approval, exact-hash verification, secret scanning, checksum generation, signing, SBOM review, and license review are complete.
5. Every release fails closed if its filename, size, checksum, signature, SBOM, license bundle, release notes, or manifest disagree.
6. Public issues, pull requests, attachments, links, logs, and screenshots are untrusted input and must never be executed automatically.
7. Feature, compatibility, security, and support claims must reflect verified evidence from the exact released artifact.

The supported publication path is: prepare a draft, upload every companion artifact, run the manual release-validation workflow, and let that successful workflow publish the draft. Directly publishing a draft through the GitHub interface bypasses the supported gate and is prohibited. Published releases are configured as immutable.

The following material is prohibited:

- Product source code, private patches, build recipes, internal CI, package caches, or Git bundles
- Passwords, password hashes, QA credentials, tokens, cookies, recovery material, private keys, or `.env` files
- Developer home paths, internal repository identifiers, private URLs, internal IP addresses, shell history, or raw build logs
- VM disks, snapshots, checkpoints, installer answer files, crash dumps, packet captures, databases, or support bundles that have not been sanitized
- Authentication automation, private malware samples, or data from unauthorized targets

## Out of scope

- Modified, unofficial, unsupported, or unverifiable images
- Upstream-only Debian, KDE, or third-party tool defects without Nulx-specific impact
- Ordinary UI defects, compatibility requests, feature requests, and documentation errors
- Scanner output without reproducible reachability or credible impact
- Attacks against GitHub itself, spam, social engineering, and third-party availability
- Requests for access to the private engineering repository

Report ordinary defects through the appropriate public issue form instead.

## Known limitations

A source-free public release repository cannot provide source-level assurance of the private build pipeline. GitHub availability and account security remain external dependencies. GitHub's Release update API does not provide an atomic compare-and-publish operation. The supported workflow rechecks the complete asset snapshot immediately before publication, while owner or interface bypass remains an administrative trust boundary. Issue attachments and external links are untrusted. Third-party binary redistribution still requires compliance with each upstream license and corresponding-source obligation. The absence of product source from this repository does not remove those duties.
