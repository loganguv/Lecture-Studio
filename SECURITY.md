# Security Policy

## Supported versions

Security fixes are provided for the latest publicly released version of Lecture Studio. Users should update through **Lecture Studio → Check for Updates…** or the official GitHub Releases page.

## Reporting a vulnerability

Do not disclose an unpatched vulnerability in a public GitHub issue.

Until a dedicated private security email is verified, use GitHub's private vulnerability reporting feature for this repository, if enabled. Repository owners should enable it under:

**Settings → Security → Code security and analysis → Private vulnerability reporting**

Include:

- the affected Lecture Studio version and build;
- the macOS version and Mac architecture;
- clear reproduction steps;
- the expected and actual result;
- the potential impact;
- a minimal proof of concept that does not contain private user data.

Never send passwords, Apple certificates, Keychain exports, Sparkle private keys, API keys, or verification codes.

## Update authenticity

Official releases are published at:

https://github.com/loganguv/Lecture-Studio/releases

Lecture Studio uses Sparkle EdDSA signatures to verify update archives. The initial application is currently ad-hoc signed and not notarized, so users may need to approve its first launch in macOS Privacy & Security.
