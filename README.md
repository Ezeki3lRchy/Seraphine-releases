<p align="center">
  <b>Seraphine — Releases</b><br>
  Cross-platform builds (macOS + Windows) of the League of Legends match-history & champ-select helper
</p>

<p align="center">
  <b>English</b> · <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine/releases/latest"><img src="https://img.shields.io/github/v/release/Ezeki3lRchy/Seraphine?style=flat&label=Latest" alt="Latest release"></a>
  <a href="https://github.com/Ezeki3lRchy/Seraphine/releases"><img src="https://img.shields.io/github/downloads/Ezeki3lRchy/Seraphine/total?style=flat&label=Downloads" alt="Downloads"></a>
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine/releases/latest"><b>⬇️ Download the latest release</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Ezeki3lRchy/Seraphine"><b>📦 Source code</b></a>
</p>

---

## What this repo is

This repository archives older Seraphine builds. Current Windows and macOS packages are published in the [main repository](https://github.com/Ezeki3lRchy/Seraphine/releases/latest).
The source code is open at [Ezeki3lRchy/Seraphine](https://github.com/Ezeki3lRchy/Seraphine) (GPL-3.0); features, issue reporting and notes are below.

Seraphine is a cross-platform fork of [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine): all upstream features are kept, the UI was migrated from PyQt5 to PySide6, and native macOS support was added.

## Download & install

Open the [latest release](https://github.com/Ezeki3lRchy/Seraphine/releases/latest) and download the installer for your platform from **Assets**.

| Platform | Asset | How to use |
|------|--------|----------|
| **Windows** | `Seraphine.7z` | Extract anywhere, run `Seraphine.exe` |
| **macOS** (Apple Silicon & Intel) | `Seraphine.dmg` | Open the `.dmg`, drag `Seraphine.app` into `Applications` |

> **First launch on macOS**
> The `.app` is an unsigned build, so Gatekeeper quarantines it after download. Run this once in Terminal before the first launch:
> ```shell
> xattr -cr /Applications/Seraphine.app
> ```
> After that, launch normally; later versions can be installed via **Update and Restart** inside the app.

## Features at a glance

- 🎮 **Champ-select automation**: auto-accept, auto pick / ban (including empty ban), auto-accept swap requests.
- 📊 **Auto stats for all 10 players**: teammates in champ select, opponents in game, any summoner on the same server.
- 🧠 **One-click OP.GG runes & builds**: tier lists, builds and skill order, one-click rune import; ARAM buffs shown automatically.
- 🍏 **Native macOS**: drag-and-drop `.dmg`, in-app **Update and Restart**, no Windows machine needed.
- 🛠 **Client & personalization**: custom 5v5 practice lobby, spectate same-server players, change profile background / status / bio / rank display, remove medals and avatar frame in one click.

> A few features that depend on native Windows window handles (post-game window fix, OP.GG overlay docking to the client) degrade gracefully on macOS.

## In-app updates

The in-app updater checks [releases in the main repository](https://github.com/Ezeki3lRchy/Seraphine/releases/latest) for the package that matches your platform. With automatic downloads enabled, eligible updates download in the background and prompt you to restart when ready.

On Windows, v1.4.5 and earlier cannot update in-app. Download a newer build manually once.

## Changelog

See the [main repository’s release notes](https://github.com/Ezeki3lRchy/Seraphine/releases) for current changes, or [archived releases](https://github.com/Ezeki3lRchy/Seraphine-releases/releases) for older builds.

## Feedback

For bugs or feature requests, open an [issue](https://github.com/Ezeki3lRchy/Seraphine-releases/issues) in this repo with your platform, version (shown under **About** on the settings page) and the log files (`Seraphine\_internal\log\` on Windows, `Seraphine.app/Contents/Frameworks/log/` on macOS via right-click → Show Package Contents).

## Uninstall

Delete the app folder and the per-platform config directory.

| Platform | Config directory |
|------|----------|
| Windows | `%AppData%\Seraphine` |
| macOS | `~/Library/Application Support/Seraphine` |

## Credits

Upstream project [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) and its contributors.
