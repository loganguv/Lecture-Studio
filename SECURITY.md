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

Never send passwords, Apple certificates, Keychain exports, Sparkle private keys, AI provider API keys, Lecture Studio Plus license keys, or verification codes.

Reports are reviewed on a best-effort basis. Please give a reasonable amount of time to investigate and release a fix before sharing details publicly.

## What is in scope

Examples of issues we want to hear about:

- another website, app, or local process being able to read or control Lecture Studio's local server;
- access to recordings, transcripts, notes, attachments, or study material by anyone other than the user;
- exposure of a stored AI provider API key or Lecture Studio Plus license;
- a malicious backup, attachment, or imported file that escapes its folder, overwrites other files, or exhausts disk space or memory;
- a way to bypass the confirmation Lecture Studio asks for before sending content to an AI provider;
- a way to bypass Lecture Studio Plus licensing checks through a flaw in the app's security;
- tampering with update delivery or the setup download.

Out of scope:

- vulnerabilities in third-party services (GitHub, Hugging Face, Freemius, OpenAI, Anthropic), which should be reported to those providers;
- issues that require physical access to an unlocked Mac or an already compromised macOS account;
- the app being ad-hoc signed and not notarized (this is documented below);
- social-engineering, spam, or denial-of-service attacks against project infrastructure.

## How Lecture Studio protects your data

- Lecture data is stored locally on your Mac. Lecture Studio does not operate a server that receives recordings or transcripts.
- The app runs a local-only server that listens on your Mac's loopback address. Requests must pass a private per-launch access token and origin checks, so other websites and apps cannot use it.
- AI provider API keys and Lecture Studio Plus license details are stored in your macOS Keychain, not in library files or backups.
- Backups and attachments are validated on import, including checks for unsafe file paths, symbolic links, malformed data, and size limits.

No software can guarantee absolute security. Keep macOS updated, keep your API keys and license key private, and store exported backups securely.

## Update authenticity

Official releases are published at:

https://github.com/loganguv/Lecture-Studio/releases

Lecture Studio uses Sparkle EdDSA signatures to verify update archives. The setup tool download is verified against a pinned checksum. The initial application is currently ad-hoc signed and not notarized, so users may need to approve its first launch in macOS Privacy & Security.

Download Lecture Studio only from the official Releases page. If you receive a copy from anywhere else, do not trust it.
