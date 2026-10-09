# Lecture Studio Privacy Policy

**Effective date: October 9, 2026**

Lecture Studio is a local-first macOS application created by Logan Guvenel. This policy explains how Lecture Studio handles recordings, transcripts, study material, app settings, licenses, and network connections.

## Summary

- Lecture transcription runs locally on your Mac.
- Lecture Studio does not operate a server that receives your recordings or transcripts.
- Lecture Studio does not include advertising or sell personal information.
- Lecture Studio does not currently include default-on analytics or crash reporting.
- The optional AI study features send text and files to OpenAI or Anthropic only if you add your own API key and confirm each request.
- Lecture Studio Plus licenses are checked with Freemius, our payment and licensing provider.
- Other internet access is used for setup downloads, speech-model downloads, updates, and links you choose to open.

## Information stored on your Mac

Lecture Studio may store the following locally:

- imported audio or video;
- microphone recordings;
- transcripts, timestamps, transcript edits, speaker labels, and saved transcript snapshots;
- course names, colors, language choices, vocabulary, and model preferences;
- Highlights, bookmarks, notes, and questions;
- files you attach to a lecture, such as slides, documents, and photos;
- study packs (summaries, key terms, study questions, and flashcards), quizzes, your quiz answers and scores, and study streak activity;
- app settings, appearance, and notification preferences;
- transcription progress, errors, and diagnostic logs;
- the private transcription runtime and downloaded speech models.

The main storage location is:

```text
~/Library/Application Support/Lecture Studio/
```

Deleting `Lecture Studio.app` does not automatically delete this folder.

### Information stored in your Mac's Keychain

- If you add an AI provider API key, it is stored in your Keychain.
- If you activate Lecture Studio Plus, your license key, license activation details, and a device ID are stored in your Keychain.

Keychain items are not part of library backups. They are not removed when you delete the app. See "Data retention and deletion" below.

## Microphone and file permissions

Lecture Studio requests microphone access only when you choose to record. It accesses files that you explicitly choose for transcription, import, attachment, export, or restoration. Notification permission is optional and notifications are disabled by default.

## Optional AI study features

Study packs, quizzes, and short-answer grading use a third-party AI provider. These features are off until you add your own API key for OpenAI or Anthropic in Settings.

What may be sent:

- When you generate a study pack or quiz: the lecture transcript (including your edits), plus any notes or attached files you choose to include. Attached PDFs and images are sent to the provider if you select them.
- When short answers are graded: your short-answer responses and the saved answer key for those questions only.

How consent works:

- Lecture Studio asks you to acknowledge each AI request before anything is sent, and asks again separately before including notes or attached files.
- Requests go from your Mac directly to the provider you chose, using your own API key. Lecture Studio does not receive or relay this content.
- The provider's handling of that content, and any charges, are governed by your agreement with the provider. Review their terms and privacy policy:
  - OpenAI: https://openai.com/policies
  - Anthropic: https://www.anthropic.com/legal

Study material returned by the provider is saved on your Mac. You can remove your API key at any time in Settings.

## Lecture Studio Plus and licensing

Lecture Studio Plus is sold and licensed through Freemius (https://freemius.com). When you purchase, activate, check, or deactivate a license, Lecture Studio connects to Freemius and may send:

- your license key;
- an identifier for this Mac (a hashed device ID derived from your Mac's hardware identifier);
- a name for this installation, which includes your Mac's name (for example, "Lecture Studio on Logan's MacBook");
- the Lecture Studio version.

Payments are handled by Freemius and its payment processors. Lecture Studio does not receive your payment card details. Freemius's handling of this information is governed by its own privacy policy.

Lecture Studio does not send your recordings, transcripts, or study material to Freemius.

## Network connections

Lecture Studio may connect to third-party services to:

- download setup tools and Python packages from GitHub, Astral, PyPI, or their delivery networks;
- download speech-recognition models from Hugging Face or associated delivery networks;
- check for and install updates through Sparkle and the Lecture Studio GitHub Pages update feed;
- check or manage a Lecture Studio Plus license with Freemius;
- send AI study requests to OpenAI or Anthropic, only as described above;
- open GitHub, support, purchase, license, or email links that you select.

These services may receive ordinary connection data such as your IP address, device/network information, request time, and the requested file. Their handling of that information is governed by their own privacy policies.

Lecture Studio does not send your recordings or transcript contents to any service as part of local transcription.

## Support and diagnostics

If you request support, you choose what information to send. Diagnostic text may include app and macOS versions, technical errors, filenames, or local file paths. Review diagnostic information before sharing it. Do not send private recordings or transcripts unless you intentionally choose to do so.

## Data retention and deletion

Lecture data remains on your Mac until you delete it. Lectures moved to Recently Deleted may remain recoverable for up to 30 days before permanent removal while Lecture Studio is running.

To remove all Lecture Studio data:

1. Export anything you want to keep.
2. If you have an active Plus license, deactivate it in Settings first.
3. Quit Lecture Studio.
4. Delete `Lecture Studio.app`.
5. Delete `~/Library/Application Support/Lecture Studio/`.
6. Optionally open Keychain Access and remove the items named "Lecture Studio.AIStudy" and "Lecture Studio.Plus".

Current versions may retain recovery copies of microphone recordings in the `Recordings` subfolder. Review that folder when deleting sensitive material.

Content you sent to an AI provider, and license records held by Freemius, are kept by those companies under their own policies. Contact them directly to ask about deletion.

## Backups

Exports are created only when you request them and are saved to a location you choose. A library backup can include your lectures, transcripts, notes, attachments, study packs, quizzes, and study streak history. It does not include your API key or license, which stay in your Keychain.

Anyone with access to an exported ZIP may be able to read its contents. Store backups securely.

Backups may not include every app preference. Review the release notes and backup description for the installed version.

## Children and student use

Lecture Studio is a general-purpose study tool and is not directed specifically to children. Users are responsible for following school policies and applicable recording-consent laws.

## Security

No software can guarantee absolute security. Keep macOS updated, download Lecture Studio only from its official GitHub repository, keep your API key and license key private, and maintain backups of important data.

## Changes to this policy

This policy may change as Lecture Studio evolves. Material changes will be reflected by updating the effective date and publishing the revised policy in this repository. If a future feature sends content to a new third-party service, this policy will be updated before that feature is released.

## Contact

For privacy questions, use the support options listed in [SUPPORT.md](SUPPORT.md). Do not post private recordings, transcripts, or sensitive personal information in a public GitHub issue.
