<p align="center">
  <b>Seraphine — 发布仓库</b><br>
  英雄联盟战绩查询与选英雄辅助工具的跨平台构建（macOS + Windows）
</p>

<p align="center">
  <a href="README.md">English</a> · <b>简体中文</b>
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest"><img src="https://img.shields.io/github/v/release/Ezeki3lRchy/Seraphine-releases?style=flat&label=Latest" alt="Latest release"></a>
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases"><img src="https://img.shields.io/github/downloads/Ezeki3lRchy/Seraphine-releases/total?style=flat&label=Downloads" alt="Downloads"></a>
</p>

<p align="center">
  <a href="https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest"><b>⬇️ 下载最新版</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/Ezeki3lRchy/Seraphine"><b>📦 源码</b></a>
</p>

---

## 这个仓库是什么

本仓库只托管 **Seraphine 跨平台分支**编译好的安装包，并作为应用内更新器的下载源。
源码开源在 [Ezeki3lRchy/Seraphine](https://github.com/Ezeki3lRchy/Seraphine)（GPL-3.0）；功能、问题反馈与说明见下方。

Seraphine 是 [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) 的跨平台分支：在保留原版全部功能的基础上，将界面从 PyQt5 迁移到 PySide6，并新增原生 macOS 支持。

## 下载与安装

进入 [最新发布页](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest)，在 **Assets** 中下载对应平台的安装包。

| 平台 | 安装包 | 使用方式 |
|------|--------|----------|
| **Windows** | `Seraphine.7z` | 解压到任意文件夹，双击运行 `Seraphine.exe` |
| **macOS** (Apple Silicon & Intel) | `Seraphine.dmg` | 打开 `.dmg`，将 `Seraphine.app` 拖入 `Applications` |

> **macOS 首次启动**
> 当前 `.app` 为未签名构建，Gatekeeper 会在下载后将其隔离。首次运行前在终端执行一次：
> ```shell
> xattr -cr /Applications/Seraphine.app
> ```
> 之后正常双击启动；后续版本可直接在应用内「更新并重启」。

## 功能速览

- 🎮 **选英雄全自动**：自动接受对局、自动选 / 禁英雄（含自动空 ban）、自动接受换英雄请求。
- 📊 **自动查 10 人战绩**：进入英雄选择自动查队友，进入游戏自动查对手，同大区召唤师战绩随手查。
- 🧠 **OP.GG 一键符文出装**：自动显示英雄排行、出装与加点，一键写入符文；大乱斗自动显示英雄 Buff。
- 🍏 **原生 macOS**：`.dmg` 拖入即用，应用内一键「更新并重启」，全程无需 Windows 环境。
- 🛠 **客户端与个性化**：创建 5v5 自定义训练房、观战同大区玩家、修改主页背景 / 在线状态 / 签名 / 段位显示、一键卸下勋章与头像框。

> 部分依赖 Windows 原生窗口句柄的能力（如修复结算界面缩成一块、OPGG 悬浮窗贴靠客户端窗口）在 macOS 上会优雅降级。

## 应用内更新

应用启动时会读取本仓库的 [最新 release](https://github.com/Ezeki3lRchy/Seraphine-releases/releases/latest)，并只在存在当前平台对应安装包（macOS 取 `.dmg`，Windows 取 `.7z`）时提示更新。
`document/ver.json` 用于标记被禁用的版本，`document/notice.md` 为应用内显示的更新日志与公告。

## 更新日志

完整更新日志见 [document/notice.md](document/notice.md) 与各 [release 页面](https://github.com/Ezeki3lRchy/Seraphine-releases/releases)。

## 反馈

遇到问题或有功能建议，请在本仓库的 [Issues](https://github.com/Ezeki3lRchy/Seraphine-releases/issues) 中提交，并附上平台、版本号（设置页「关于」可见）以及日志文件（Windows 在 `Seraphine\_internal\log\`，macOS 在 `Seraphine.app/Contents/Frameworks/log/`，右键 App →「显示包内容」）。

## 卸载

删除程序文件夹，并删除对应平台的配置目录。

| 平台 | 配置目录 |
|------|----------|
| Windows | `%AppData%\Seraphine` |
| macOS | `~/Library/Application Support/Seraphine` |

## 致谢

上游项目 [Zzaphkiel/Seraphine](https://github.com/Zzaphkiel/Seraphine) 及其贡献者。
