# Nulx Linux beta testing

No public beta ISO is available yet. This guide is for a future approved release. You can explore the [tool catalog](https://nulxlinux.com/tools/), read the [documentation](https://nulxlinux.com/docs/) or suggest a documentation correction now.

The [development status](../README.md#development-status) describes work tested on the development installation. It does not establish support for a released image, physical computer or hypervisor. Check the release notes for the exact version and platform when a beta becomes available.

## Prepare a test environment

1. Start from the official [Releases page](https://github.com/Alhasan100/Nulx-Linux-Releases/releases) and read its known limitations.
2. Follow [Verify a download](VERIFY-DOWNLOAD.md) to check the signed manifest, ISO checksum and detached signature.
3. Prefer a disposable VM or unused test disk. Back up important data before using physical hardware.
4. Keep the beta away from production credentials and sensitive networks.
5. Use security tools only on systems you own or are explicitly authorized to test.

Do not use issue attachments, pull-request artifacts, unofficial mirrors or files without the official verification material.

## Useful things to test

Choose a small, repeatable task and record what happened. Suggested areas include:

- Boot, live desktop, installation and first reboot.
- Display scaling, keyboard navigation and accessibility.
- Networking, audio, external displays, suspend and shutdown.
- Finding and starting tools through Launcher and Command Center.
- Tool prerequisites and wordlists needed for an authorized lab exercise.
- Nulx Terminal and the local Offline Guide.
- Optional online chat, sharing consent, cancellation and usage-limit messages when supported by that release.
- Approval-based actions and package upgrades only when the release notes explicitly authorize testing them.

Startup checks alone do not confirm complete tool workflows. A listed shortcut does not establish that every prerequisite is ready.

## Submit a useful report

Use the matching form in [Support](../SUPPORT.md). Include the release tag, ISO filename and verified SHA-256, hardware or hypervisor version, live or installed session, and the shortest steps that reproduce the result. State what you expected and what happened.

Firmware mode, Secure Boot state, display session and relevant hardware details help with boot, desktop and compatibility reports. Include them when they affect the problem.

Follow [Privacy and redaction](PRIVACY-AND-REDACTION.md) before attaching the smallest relevant diagnostic excerpt. Never upload credentials, personal data, a VM disk or a raw support bundle. Report suspected vulnerabilities privately through [SECURITY.md](../SECURITY.md).
