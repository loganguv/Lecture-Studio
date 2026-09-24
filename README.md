# Lecture Studio

Lecture Studio is a private, local-first macOS app that turns lecture recordings into searchable, timestamped transcripts.

- Record from your Mac or import existing audio and video
- Transcribe locally using MLX Whisper
- Search transcripts across your library
- Follow transcripts during audio playback
- Save bookmarks, notes, questions, and important moments
- Organize lectures by course
- Export and back up your library
- No subscription or API key required

## System Requirements

- Apple Silicon Mac — M1 or newer
- macOS 14.6 or later
- Several gigabytes of available storage
- Internet access for initial setup, model downloads, and app updates

Lecture Studio does not currently support Intel Macs.

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
- Transcripts
- Course settings
- Highlights, bookmarks, notes, and questions
- Playback and app preferences

Transcription runs locally on supported Apple Silicon Macs. Lecture Studio does not upload recordings or transcripts to a Lecture Studio server.

### When Lecture Studio connects to the internet

Lecture Studio may access the internet to:

- Download its private Python and transcription runtime
- Download required packages from package repositories
- Download speech-recognition models
- Check for and install app updates
- Open links or an email client when you request support

These downloads may involve services operated by GitHub, Astral, PyPI, Hugging Face, and the Sparkle update system. Those services may receive ordinary connection information such as your IP address.

Lecture Studio currently does not include advertising, user accounts, or default-on analytics.

Read the full [Privacy Policy](PRIVACY_POLICY_URL).

## Permissions

Lecture Studio may request:

- **Microphone access** when you choose to record a lecture
- **Notification access** if you enable transcription-completion notifications
- **File access** when you choose recordings, backups, or export destinations

Notifications are optional and disabled by default.

## Recording Consent

Recording laws and school policies vary by location and institution.

You are responsible for obtaining permission from your instructor and anyone else being recorded. Do not use Lecture Studio to record a class, meeting, or conversation when recording is prohibited.

## Data Storage

Lecture Studio stores its library and private runtime under:

```text
~/Library/Application Support/Lecture Studio/
