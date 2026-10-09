# Lecture Studio

Lecture Studio is a private, local-first macOS app that turns lecture recordings into searchable, timestamped transcripts, with optional study tools.

- Record from your Mac or import existing audio and video
- Transcribe locally using MLX Whisper
- Search transcripts across your library
- Follow transcripts during audio playback
- Edit transcripts: fix text, add speakers, find and replace, and revert to the original
- Save bookmarks, notes, questions, and important moments
- Attach slides, documents, and photos to a lecture
- Organize lectures by course
- Export and back up your library
- Core recording, transcription, notes, and attachments are free, with no account required

### Lecture Studio Plus (optional)

Plus adds study tools and extras:

- Study packs: summaries, key terms, study questions, and flashcards
- Quizzes with instant scoring and AI grading of short answers
- Study streaks
- Silence detection for skipping quiet stretches in recordings
- Transcript editing and batch export

AI study features use your own OpenAI or Anthropic API key and only send content after you confirm. An API key is not needed for anything else.

## System Requirements

- Apple Silicon Mac, M1 or newer
- macOS 14.6 or later
- Several gigabytes of available storage
- Internet access for initial setup, model downloads, and app updates

Lecture Studio does not support Intel Macs.

## Download and Install

1. Download the latest `Lecture-Studio-[version].zip` from the [Releases page](https://github.com/loganguv/Lecture-Studio/releases).
2. Open the ZIP.
3. Move **Lecture Studio.app** into your Applications folder.
4. Open Lecture Studio.

### If macOS blocks the app

Lecture Studio is currently distributed independently with ad-hoc signing and is not notarized by Apple. Because of this, macOS may block the first launch.

To approve it:

1. Try to open Lecture Studio once.
2. Open **System Settings**.
3. Select **Privacy & Security**.
4. Scroll down to the Security section.
5. Find the message about Lecture Studio and click **Open Anyway**.
6. Confirm that you want to open the app.

Do not disable Gatekeeper globally. Lecture Studio should only require this approval for the downloaded app.

After opening the app, follow the setup screen to install the private transcription runtime. Setup does not require Terminal, Homebrew, an administrator password, or an API key.

## Privacy

Lecture Studio is designed as a local-first application.

### What stays on your Mac

- Imported recordings
- Microphone recordings
- Transcripts and transcript edits
- Course settings
- Highlights, bookmarks, notes, and questions
- Attached files
- Study packs, quizzes, scores, and study streaks
- Playback and app preferences

Transcription runs locally on supported Apple Silicon Macs. Lecture Studio does not upload recordings or transcripts to a Lecture Studio server.

Your AI provider API key and Plus license are stored in your Mac's Keychain.

### When Lecture Studio connects to the internet

Lecture Studio may access the internet to:

- Download its private Python and transcription runtime
- Download required packages from package repositories
- Download speech-recognition models
- Check for and install app updates
- Purchase, activate, or check a Lecture Studio Plus license
- Send AI study requests, only if you add your own API key and confirm each request
- Open links or an email client when you request support

These connections may involve services operated by GitHub, Astral, PyPI, Hugging Face, Freemius, OpenAI, Anthropic, and the Sparkle update system. Those services may receive ordinary connection information such as your IP address.

When you use AI study features, the content you choose to include (such as the transcript, notes, or attached files) is sent directly from your Mac to the provider you selected.

Lecture Studio does not include advertising, user accounts, or default-on analytics.

Read the full [Privacy Policy](PRIVACY.md).

## Permissions

Lecture Studio may request:

- **Microphone access** when you choose to record a lecture
- **Notification access** if you enable notifications
- **File access** when you choose recordings, attachments, backups, or export destinations

Notifications are optional and disabled by default.

## Recording Consent

Recording laws and school policies vary by location and institution.

You are responsible for obtaining permission from your instructor and anyone else being recorded. Do not use Lecture Studio to record a class, meeting, or conversation when recording is prohibited.

## Data Storage

Lecture Studio stores its library and private runtime under:

```text
~/Library/Application Support/Lecture Studio/
```

## Important Links

- [Privacy Policy](PRIVACY.md)
- [Terms of Use](TERMS.md)
- [Support](SUPPORT.md)
- [Security Policy](SECURITY.md)
- [Open-Source Notices](OPEN_SOURCE_NOTICES.md)
- [Lecture Studio License](LICENSE)
