# PrivacyNotes Scoop bucket

[Scoop](https://scoop.sh) bucket for [PrivacyNotes](https://privacynotes.app), an end-to-end
encrypted app for notes, tasks, files and a vault.

## Install

```powershell
scoop bucket add lifetimelabs https://github.com/LifetimeLabsDev/scoop-bucket
scoop install lifetimelabs/privacynotes
```

## What you get

The same signed Windows build we publish everywhere else, taken from the GitHub release and
verified against the checksum in the manifest. The installer is Authenticode-signed by
Lifetime Labs LLC.

Scoop unpacks it rather than running it, so the app lives under your Scoop directory and no
file associations are registered. Use the installer from
[privacynotes.app](https://privacynotes.app) if you want PrivacyNotes offered in the Windows
"Open with" list for Markdown files.

## Updates

The manifest carries `checkver` and `autoupdate`, both pointed at the Windows release feed, and
an Excavator workflow runs every four hours. New versions land here on their own.

Your notes are not touched by an update. They live in `%LOCALAPPDATA%\app.privacynotes`,
outside the Scoop directory.
