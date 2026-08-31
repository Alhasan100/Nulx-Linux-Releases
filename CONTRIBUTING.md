# Contributing to the public beta

This repository accepts high-quality beta reports and documentation improvements. Nulx Linux product development remains in a separate private engineering repository.

## Beta reports

Use the structured issue form that best matches the result. A useful report identifies the exact release, verifies the ISO checksum, explains the environment, and provides deterministic reproduction steps. Read [Privacy and redaction](docs/PRIVACY-AND-REDACTION.md) before sharing diagnostics.

## Pull requests

Pull requests are limited to corrections and improvements to the allowlisted public documentation and issue forms. They must not contain:

- Nulx Linux product source or build files;
- executable or binary files, archives, ISO images, Git LFS objects, or submodules;
- generated logs, VM images, screenshots containing sensitive information, or test data from third parties;
- credentials, tokens, private keys, internal paths, or private repository information.

`CODEOWNERS`, the public-boundary workflow, and the release public key are maintainer-controlled security files and are not accepted through external pull requests.

Release binaries are published only by maintainers through GitHub Releases. Binary pull requests are never accepted.

By contributing, you agree that your repository contribution is available under the repository's MIT License and that you have the right to submit it.

## Responsible testing

Only test systems you own or are explicitly authorized to assess. Keep offensive testing isolated, document the rules of engagement, and prefer minimal safe reproduction over destructive proof.

## Security reports

Do not disclose vulnerabilities in issues or pull requests. Follow [SECURITY.md](SECURITY.md).
