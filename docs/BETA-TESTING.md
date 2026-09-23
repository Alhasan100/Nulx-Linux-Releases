# Nulx Linux beta testing

## Before a public beta exists

No public beta ISO is available until an approved release appears on the official [Releases page](https://github.com/Alhasan100/Nulx-Linux-Releases/releases). If the ISO is hosted at the dedicated download endpoint, follow only the URL recorded in that Release's signed manifest. Do not trust issue attachments, pull-request artifacts, unofficial mirrors, or files that lack the published checksum and signature.

## Prepare a safe test environment

1. Read the release notes and known limitations.
2. Download every artifact from the same official release.
3. Verify the ISO SHA-256 and detached signature.
4. Back up important data before testing on physical hardware.
5. Prefer a new VM or an unused test disk for installation tests.
6. Do not expose an untrusted beta system directly to sensitive networks or production credentials.
7. Use security tools only on systems you own or are explicitly authorized to test.

The current beta validation focuses on Hyper-V and VirtualBox, alongside physical hardware testing. Other environments are not confirmed supported. Always check the release notes for the exact image and platform before testing.

The September 23 development checkpoint includes real-account chat, saved-account reconnection, a single-window AI interface, and an in-place AI package upgrade. Those checks were performed on a development installation. Newer package, guarded-command, private-history, updater and Spectrum checks used isolated test environments. They do not make a public ISO available or establish complete account, action, hardware, or upgrade acceptance. See the [current status](../README.md#development-status).

## Record the environment

Include the following details in your report:

- Release tag, exact ISO filename, and SHA-256
- Physical hardware or hypervisor and version
- CPU architecture, memory, GPU, network, and storage controller
- UEFI or legacy boot, Secure Boot state, and encryption choices
- Whether you used a live or installed session
- Wayland or X11, when relevant
- Exact reproduction steps, expected behavior, and actual behavior

## Suggested test areas

- ISO boot in UEFI and supported legacy modes
- Live desktop startup and display scaling
- Installer partitioning, locale, keyboard, user creation, and first boot
- Suspend, resume, shutdown, restart, lock, and login
- Wired networking, Wi-Fi, audio, Bluetooth, GPU acceleration, and external displays
- Nulx Launcher, Terminal, Command Center, Offline Guide, and tool registry
- Nulx AI mode switching, unsent drafts, keyboard navigation, and clean closure
- Optional online sign-in, cancellation, reconnect, explicit sharing consent, and clear usage-limit errors when authorized by the release notes
- Reviewed command proposals, one-use approval, cancellation and separate result sharing only when the tested release explicitly supports them
- Virtual desktops, keyboard navigation, accessibility, and multiple displays
- Upgrades and package installation only when the release notes authorize them

## Submit a report

Use the matching issue form. Attach the smallest sanitized diagnostic excerpt that demonstrates the problem. Never upload a complete home directory, VM disk, credentials, or a raw support bundle.
