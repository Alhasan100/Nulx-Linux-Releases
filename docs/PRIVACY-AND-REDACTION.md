# Privacy and diagnostic redaction

Public GitHub issues, comments, and attachments are visible to everyone. Treat them as permanent public records.

## Remove before posting

- passwords, API tokens, cookies, private keys, recovery codes, and authentication databases;
- full names, email addresses, phone numbers, account identifiers, and client information;
- home-directory names and local file paths that identify a person or organization;
- public or private IP addresses when they are not essential, MAC addresses, serial numbers, UUIDs, and device identifiers;
- Wi-Fi SSIDs, VPN endpoints, browser profiles, shell history, clipboard contents, and recent-document lists;
- proprietary source, target data, packet payloads, malware samples, or information from systems you were not authorized to test;
- EXIF metadata and unrelated screen content in screenshots.

## Safer diagnostic process

1. Reproduce the issue in a disposable test account or isolated VM when possible.
2. Copy only the few relevant log lines rather than uploading a whole log or support archive.
3. Replace sensitive values consistently, for example `<user>`, `<host>`, `<ip>`, and `<token-redacted>`.
4. Review the final text and attachment visually before posting.
5. If the report may reveal a security vulnerability, stop and use private vulnerability reporting.

Maintainers may remove public content that appears to contain sensitive information, but removal cannot guarantee that earlier copies no longer exist.
