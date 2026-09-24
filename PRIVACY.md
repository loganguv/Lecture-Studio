# Lecture Studio Privacy Policy

**Effective date: September 24, 2026**

Lecture Studio is a local-first macOS application created by Logan Guvenel. This policy explains how Lecture Studio handles recordings, transcripts, app settings, and network connections.

## Summary

- Lecture transcription runs locally on your Mac.
- Lecture Studio does not operate a server that receives your recordings or transcripts.
- Lecture Studio does not include advertising or sell personal information.
- Lecture Studio does not currently include default-on analytics or crash reporting.
- Internet access is used for setup downloads, speech-model downloads, updates, and links you choose to open.

## Information stored on your Mac

Lecture Studio may store the following locally:

- imported audio or video;
- microphone recordings;
- transcripts and timestamps;
- course names, colors, language choices, vocabulary, and model preferences;
- Highlights, bookmarks, notes, and questions;
- app settings and notification preferences;
- transcription progress, errors, and diagnostic logs;
- the private transcription runtime and downloaded speech models.

The main storage location is:

```text
~/Library/Application Support/Lecture Studio/
```

Deleting `Lecture Studio.app` does not automatically delete this folder.

## Microphone and file permissions

Lecture Studio requests microphone access only when you choose to record. It accesses files that you explicitly choose for transcription, import, export, or restoration. Notification permission is optional and notifications are disabled by default.

## Network connections

Lecture Studio may connect to third-party services to:

- download setup tools and Python packages from GitHub, Astral, PyPI, or their delivery networks;
- download speech-recognition models from Hugging Face or associated delivery networks;
- check for and install updates through Sparkle and the Lecture Studio GitHub Pages update feed;
- open GitHub, support, license, or email links that you select.

These services may receive ordinary connection data such as your IP address, device/network information, request time, and the requested file. Their handling of that information is governed by their own privacy policies.

Lecture Studio does not intentionally send your recordings or transcript contents to these services as part of local transcription.

## Support and diagnostics

If you request support, you choose what information to send. Diagnostic text may include app and macOS versions, technical errors, filenames, or local file paths. Review diagnostic information before sharing it. Do not send private recordings or transcripts unless you intentionally choose to do so.

## Data retention and deletion

Lecture data remains on your Mac until you delete it. Lectures moved to Recently Deleted may remain recoverable for up to 30 days before permanent removal while Lecture Studio is running.

To remove all Lecture Studio data:

1. Export anything you want to keep.
2. Quit Lecture Studio.
3. Delete `Lecture Studio.app`.
4. Delete `~/Library/Application Support/Lecture Studio/`.

Current versions may retain recovery copies of microphone recordings in the `Recordings` subfolder. Review that folder when deleting sensitive material.

## Backups

Exports are created only when you request them and are saved to a location you choose. Anyone with access to an exported ZIP may be able to read its contents. Store backups securely.

Current backup formats may not include every app preference or Highlight. Review the release notes and backup description for the installed version.

## Children and student use

Lecture Studio is a general-purpose study tool and is not directed specifically to children. Users are responsible for following school policies and applicable recording-consent laws.

## Future AI features

The current local transcription workflow does not send transcripts to a cloud AI provider. If a future feature can send content to a third-party AI provider, Lecture Studio will identify the provider and request the user's action or consent before transmission. This policy will be updated before such a feature is released.

## Security

No software can guarantee absolute security. Keep macOS updated, download Lecture Studio only from its official GitHub repository, and maintain backups of important data.

## Changes to this policy

This policy may change as Lecture Studio evolves. Material changes will be reflected by updating the effective date and publishing the revised policy in this repository.

## Contact

For privacy questions, use the support options listed in [SUPPORT.md](SUPPORT.md). Do not post private recordings, transcripts, or sensitive personal information in a public GitHub issue.
