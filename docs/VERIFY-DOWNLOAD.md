# Verify a Nulx Linux download

An ISO is trusted only when its checksum and detached signature match the files in the same official GitHub Release.

## 1. Confirm the source

Begin only from:

`https://github.com/Alhasan100/Nulx-Linux-Releases/releases`

Open the selected Release and verify the signature of its manifest. If the ISO is too large for a GitHub Release asset, use only the exact HTTPS URL recorded inside that signed manifest. Do not boot a file from an issue attachment, pull request, chat message, search result, or unofficial mirror.

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

The release notes will identify the approved signing key and fingerprint. Confirm that fingerprint through both this repository and the official Nulx Linux website before trusting a newly downloaded key.

After importing the verified public key:

```bash
gpg --verify Nulx-Linux-<version>-amd64.iso.sig Nulx-Linux-<version>-amd64.iso
```

The signature must be valid and made by the fingerprint named in the release notes. A valid signature from an unknown key is not sufficient.

## 4. Check the manifest

Confirm that the ISO filename, official HTTPS URL, byte size, SHA-256, architecture, signature filename, SBOM, license bundle, and release notes agree with `MANIFEST.json`, and that `MANIFEST.json.asc` is valid.

If any value is missing or inconsistent, do not boot the ISO. Report a possible release-integrity problem privately through [SECURITY.md](../SECURITY.md).
