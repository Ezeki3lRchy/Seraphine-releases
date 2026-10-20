<p align="center">
  <b>Seraphine — 发布仓库 / Releases</b><br>
  英雄联盟战绩查询与选英雄辅助工具的跨平台构建（macOS + Windows）<br>
  Cross-platform builds (macOS + Windows) of the League of Legends match-history & champ-select helper
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest"><img src="https://img.shields.io/github/v/release/Ezeki3lRchy/Seraphine-releases?style=flat&label=Latest" alt="Latest release"></a>
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases"><img src="https://img.shields.io/github/downloads/Ezeki3lRchy/Seraphine-releases/total?style=flat&label=Downloads" alt="Downloads"></a>
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest"><b>⬇️ 下载最新版 / Download the latest release</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Ezeki3lRchy/Seraphine"><b>📦 源码 / Source code</b></a>
</p>

---

## 这个仓库是什么 / What this repo is

本仓库只托管 **Seraphine 跨平台分支**编译好的安装包，并作为应用内更新器的下载源。
源码开源在 [Ezeki3lRchy/Seraphine](https://github.com/Ezeki3lRchy/Seraphine)（GPL-3.0）；功能、问题反馈与说明见下方。

This repo hosts only the **compiled installers** of the Seraphine cross-platform fork and serves as the download source for the in-app updater.
The source code is open at [Ezeki3lRchy/Seraphine](https://github.com/Ezeki3lRchy/Seraphine) (GPL-3.0); features, issue reporting and notes are below.

Seraphine 是 [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) 的跨平台分支：在保留原版全部功能的基础上，将界面从 PyQt5 迁移到 PySide6，并新增原生 macOS 支持。

Seraphine is a cross-platform fork of [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine): all upstream features are kept, the UI was migrated from PyQt5 to PySide6, and native macOS support was added.

## 下载与安装 / Download & install

进入 [最新发布页](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest)，在 **Assets** 中下载对应平台的安装包。
Open the [latest release](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest) and download the installer for your platform from **Assets**.

| 平台 / Platform | 安装包 / Asset | 使用方式 / How to use |
|------|--------|----------|
| **Windows** | `Seraphine.7z` | 解压到任意文件夹，双击运行 `Seraphine.exe` / Extract anywhere, run `Seraphine.exe` |
| **macOS** (Apple Silicon & Intel) | `Seraphine.dmg` | 打开 `.dmg`，将 `Seraphine.app` 拖入 `Applications` / Open the `.dmg`, drag `Seraphine.app` into `Applications` |

> **macOS 首次启动 / First launch on macOS**
> 当前 `.app` 为未签名构建，Gatekeeper 会在下载后将其隔离。首次运行前在终端执行一次：
> The `.app` is an unsigned build, so Gatekeeper quarantines it after download. Run this once in Terminal before the first launch:
> ```shell
> xattr -cr /Applications/Seraphine.app
> ```
> 之后正常双击启动；后续版本可直接在应用内「更新并重启」。
> After that, launch normally; later versions can be installed via **Update and Restart** inside the app.

## 功能速览 / Features at a glance

- 🎮 **选英雄全自动 / Champ-select automation**：自动接受对局、自动选 / 禁英雄（含自动空 ban）、自动接受换英雄请求。 Auto-accept, auto pick / ban (including empty ban), auto-accept swap requests.
- 📊 **自动查 10 人战绩 / Auto stats for all 10 players**：进入英雄选择自动查队友，进入游戏自动查对手，同大区召唤师战绩随手查。 Teammates in champ select, opponents in game, any summoner on the same server.
- 🧠 **OP.GG 一键符文出装 / One-click OP.GG runes & builds**：自动显示英雄排行、出装与加点，一键写入符文；大乱斗自动显示英雄 Buff。 Tier lists, builds and skill order, one-click rune import; ARAM buffs shown automatically.
- 🍏 **原生 macOS / Native macOS**：`.dmg` 拖入即用，应用内一键「更新并重启」，全程无需 Windows 环境。 Drag-and-drop `.dmg`, in-app **Update and Restart**, no Windows machine needed.
- 🛠 **客户端与个性化 / Client & personalization**：创建 5v5 自定义训练房、观战同大区玩家、修改主页背景 / 在线状态 / 签名 / 段位显示、一键卸下勋章与头像框。 Custom 5v5 practice lobby, spectate same-server players, change profile background / status / bio / rank display, remove medals and avatar frame in one click.

> 部分依赖 Windows 原生窗口句柄的能力（如修复结算界面缩成一块、OPGG 悬浮窗贴靠客户端窗口）在 macOS 上会优雅降级。
> A few features that depend on native Windows window handles (post-game window fix, OP.GG overlay docking to the client) degrade gracefully on macOS.

## 应用内更新 / In-app updates

应用启动时会读取本仓库的 [最新 release](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest)，并只在存在当前平台对应安装包（macOS 取 `.dmg`，Windows 取 `.7z`）时提示更新。
`document/ver.json` 用于标记被禁用的版本，`document/notice.md` 为应用内显示的更新日志与公告。

On startup the app reads this repo's [latest release](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest) and prompts for an update only when an asset for the current platform exists (`.dmg` on macOS, `.7z` on Windows).
`document/ver.json` marks disabled versions; `document/notice.md` is the changelog and notice shown inside the app.

## 更新日志 / Changelog

完整更新日志见 [document/notice.md](document/notice.md) 与各 [release 页面](https://github.com/Ezeki3lRchy/Seraphine-releases/releases)。

The full changelog is in [document/notice.md](document/notice.md) and on each [release page](https://github.com/Ezeki3lRchy/Seraphine-releases/releases).

## 反馈 / Feedback

遇到问题或有功能建议，请在本仓库的 [Issues](https://github.com/Ezeki3lRchy/Seraphine-releases/issues) 中提交，并附上平台、版本号（设置页「关于」可见）以及日志文件（Windows 在 `Seraphine\_internal\log\`，macOS 在 `Seraphine.app/Contents/Frameworks/log/`，右键 App →「显示包内容」）。

For bugs or feature requests, open an [issue](https://github.com/Ezeki3lRchy/Seraphine-releases/issues) in this repo with your platform, version (shown under **About** on the settings page) and the log files (`Seraphine\_internal\log\` on Windows, `Seraphine.app/Contents/Frameworks/log/` on macOS via right-click → Show Package Contents).

## 卸载 / Uninstall

删除程序文件夹，并删除对应平台的配置目录。
Delete the app folder and the per-platform config directory.

| 平台 / Platform | 配置目录 / Config directory |
|------|----------|
| Windows | `%AppData%\Seraphine` |
| macOS | `~/Library/Application Support/Seraphine` |

## 致谢 / Credits

上游项目 [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) 及其贡献者。
Upstream project [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) and its contributors.
