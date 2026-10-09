# Lecture Studio Support

## Get help

- Check the latest [release notes](https://github.com/loganguv/Lecture-Studio/releases).
- Search existing [GitHub issues](https://github.com/loganguv/Lecture-Studio/issues).
- If your problem hasn’t been reported, open a new issue without attaching private recordings, transcripts, notes, or files.
- For private support or licensing questions, email [lecturestudio.support@gmail.com](mailto:lecturestudio.support@gmail.com).

## Requirements and setup

Lecture Studio requires an **Apple Silicon Mac (M1 or newer) running macOS 14.6 or later**.

First-time setup needs an internet connection and several GB of free space. The speech model downloads when first used. After setup and model downloads, transcription runs locally on your Mac without an account, subscription, or API key.

If setup fails, check your internet connection and available storage, then choose **Try again**.

## Include in a problem report

- Lecture Studio version and build, shown in **Settings → About**
- macOS version and Apple chip
- What you expected and what happened
- Steps to reproduce the problem
- Whether it affects recording, transcription, playback, study tools, or another feature
- Diagnostic text shown by Lecture Studio, after reviewing it for private paths, filenames, or content

For AI study problems, include the provider name and exact error message. **Never include your API key or license key.**

## Recording and transcription

If microphone recording doesn’t work, check **System Settings → Privacy & Security → Microphone** and allow Lecture Studio access.

If transcription fails, review the error message and use the available retry option. Keep Lecture Studio open while transcribing.

Interrupted recordings may appear as recovery recordings in **Settings → Storage**. Review or save them before deleting anything.

Silence prompts are controlled in **Settings → Notifications**. During recording, **Pause** pauses the recording; **×** dismisses the reminder and keeps recording. The reminder detects quiet microphone input, not recognized words.

## AI study tools

Lecture Studio+ includes AI study packs, quizzes, study streaks and progress, advanced transcript editing, playback silence skipping, and batch export.

To use AI study tools:

1. Open **Settings → AI Study Generation**.
2. Choose OpenAI or Anthropic.
3. Save your own API key, then select **Test connection**.

Provider usage charges are separate from Lecture Studio+. A connection test sends no lecture content.

Study generation sends the transcript and any selected notes or files to your chosen provider after acknowledgment. Short-answer quiz grading sends the relevant questions, model answers, and your responses. Multiple-choice and true/false answers are scored locally.

If short-answer grading fails, use **Retry short-answer grading**. Your submitted answers remain saved.

## Lecture Studio+ licenses

Activate your license in **Settings → Lecture Studio+**.

To move your license to another Mac, expand **Manage license** and deactivate it on the current Mac first. Deactivation keeps your lectures and saved study packs.

For activation problems, email support with the error message. Do not post your license key publicly.

## Installation blocked by macOS

Download Lecture Studio only from the official [GitHub releases](https://github.com/loganguv/Lecture-Studio/releases).

If macOS says the developer cannot be verified or Apple cannot check the app, and you trust the download:

1. Try opening Lecture Studio once.
2. Open **System Settings → Privacy & Security**.
3. Scroll to Security and choose **Open Anyway**, if available.
4. Confirm **Open** when prompted.

See Apple’s [instructions for opening apps safely](https://support.apple.com/en-us/102445). Do not disable Gatekeeper globally.

If macOS reports that the app will damage your computer, do not bypass that warning. Contact support.

## Backups and deleted lectures

Use **Settings → Storage** to export a restorable library backup. Library backup export requires Lecture Studio+.

Backups can include transcripts, notes, attachments, study packs, quiz history, study progress, and optional lecture audio. Select **Include audio** if you want recordings in the backup.

Transcript-only exports are not restorable library backups. Library backups exclude app preferences, API keys, Recently Deleted items, and recovery recordings. Save recovery recordings separately.

Deleted lectures can be restored from **Settings → Recently Deleted** for 30 days, unless permanently deleted sooner.

## Data location

Lecture Studio normally stores its data at:

```text
~/Library/Application Support/Lecture Studio/
```

This includes:

- `Transcripts/` — lecture data and saved study materials
- `Recordings/` — microphone recordings and recovery files
- `runtime-v1/` — the private transcription runtime

API keys are stored in macOS Keychain; some preferences are stored separately by macOS. Copying this folder alone is not a complete backup of every app setting.

Export important data before deleting or repairing anything in this folder. Contact support before manually moving files if your library is missing or migration fails.

## Never post publicly

Do not post:

- Private recordings, transcripts, notes, attachments, or quiz responses
- Passwords, verification codes, API keys, or license keys
- Signing keys, certificates, or Keychain exports
- Private student, instructor, medical, employment, or financial information

Review screenshots and diagnostic text before sharing them.
