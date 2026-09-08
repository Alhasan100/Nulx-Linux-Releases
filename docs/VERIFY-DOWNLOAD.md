# Verify a Nulx Linux download

No approved public ISO is available yet. These instructions apply only after an official release is published. The planned `downloads.nulxlinux.com` service is not currently an approved download channel.

An ISO must match the checksum, detached signature and signed manifest from the same official GitHub Release.

## 1. Confirm the source

Begin only from:

`https://github.com/Alhasan100/Nulx-Linux-Releases/releases`

Read the selected Release's notes for the approved public key and fingerprint. Confirm the fingerprint through both this repository and the official Nulx Linux website before importing or trusting that key.

Download the manifest and its signature from the Release. After importing the verified public key, check the manifest signature:

```bash
gpg --verify Nulx-Linux-<version>-MANIFEST.json.asc Nulx-Linux-<version>-MANIFEST.json
```

Replace `<version>` with the actual release version in every example on this page. The signature must be valid and identify the approved fingerprint. Use only the exact HTTPS ISO URL in that signed manifest, even when the file is hosted outside GitHub. Do not boot files from issue attachments, pull requests, chat messages, search results or unofficial mirrors.

## 2. Verify SHA-256

On Linux:

```bash
sha256sum Nulx-Linux-<version>-amd64.iso
cat Nulx-Linux-<version>-amd64.iso.sha256
```

On Windows PowerShell:

```powershell
Get-FileHash -Algorithm SHA256 .\Nulx-Linux-<version>-amd64.iso
Get-Content .\Nulx-Linux-<version>-amd64.iso.sha256
```

The hexadecimal values must match exactly. Stop if they differ.

## 3. Verify the detached signature

Use the same verified public key to check the ISO signature. Use the exact signature filename supplied by the Release, which may end in `.sig` or `.asc`:

```bash
gpg --verify Nulx-Linux-<version>-amd64.iso.sig Nulx-Linux-<version>-amd64.iso
```

The signature must be valid and made by the fingerprint named in the release notes. A valid signature from an unknown key is not sufficient.

## 4. Check the manifest

Confirm that the ISO filename, official HTTPS URL, byte size, SHA-256, architecture, signature filename, SBOM, license bundle, and release notes agree with `MANIFEST.json`, and that `MANIFEST.json.asc` is valid.

If any value is missing or inconsistent, do not boot the ISO. Report a possible release-integrity problem privately through [SECURITY.md](../SECURITY.md).
