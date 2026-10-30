# PrivacyNotes Scoop bucket

[Scoop](https://scoop.sh) bucket for [PrivacyNotes](https://privacynotes.app), an end-to-end
encrypted app for notes, tasks, files and a vault.

## We recommend winget

winget is the Windows install we support. It runs our installer, so the app then updates
itself, and it registers the file associations Scoop leaves out:

```powershell
winget install LifetimeLabs.PrivacyNotes
```

This bucket stays live and keeps getting new versions on its own, so a Scoop install keeps
working. It is no longer listed on our homepage.

### Move from Scoop to winget

Close PrivacyNotes, then run this in PowerShell:

```powershell
winget install LifetimeLabs.PrivacyNotes; scoop uninstall privacynotes
```

winget installs the app, then Scoop removes its copy. Your notes and settings stay: they
live in `%APPDATA%` and `%LOCALAPPDATA%`, outside the Scoop directory. The app's update notice
offers this same command under **Copy command**.

## Install with Scoop

```powershell
scoop bucket add lifetimelabs https://github.com/LifetimeLabsDev/scoop-bucket
scoop install lifetimelabs/privacynotes
```

## What you get

The same signed Windows build we publish everywhere else, taken from the GitHub release and
verified against the checksum in the manifest. The installer is Authenticode-signed by
Lifetime Labs LLC.

Scoop unpacks it rather than running it, so the app lives under your Scoop directory and no
file associations are registered.

## Updates

The app cannot update itself in a Scoop install. Run `scoop update privacynotes`.

The manifest carries `checkver` and `autoupdate`, both pointed at the Windows release feed, and
an Excavator workflow runs every four hours. New versions land here on their own, as soon as
the GitHub release exists.

Your notes are not touched by an update. They live outside the Scoop directory.
