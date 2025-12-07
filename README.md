# 🎧 Stereo Installer

A one-click install tool for Discord Stereo Modules. Automatically downloads and applies the latest voice module patches to restore lossless stereo audio functionality.

---

## 🚀 Quick Install

> [!TIP]
> **Recommended:** Use the one-line command for the fastest setup.

### Option 1: One-Line Command
Press `Win + R`, paste this command, and hit Enter:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/ProdHallow/installer/main/DiscordVoiceFixer.ps1 | iex"
```

### Option 2: Download Batch File
1. Download [Stereo Installer.bat](https://github.com/ProdHallow/Discord-Stereo-Installer/releases/latest)
2. Double-click to run

---

## 💬 Supported Clients

| Client | Type |
|--------|------|
| Discord Stable | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord PTB | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord Canary | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| Discord Development | ![Official](https://img.shields.io/badge/Official-5865F2?style=flat-square) |
| BetterDiscord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Vencord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |
| Equicord | ![Mod](https://img.shields.io/badge/Mod-57a657?style=flat-square) |

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🔄 **Automatic Updates** | Always runs the latest version |
| 🎯 **Fix All Clients** | Scan and patch all installed Discord clients at once |
| 💾 **Backup & Rollback** | Automatically backs up voice modules before patching; restore anytime |
| 🔔 **Update Detection** | Alerts you when Discord updates and the fix needs to be reapplied |
| 📁 **Quick Backup Access** | Open your backup folder directly from the app |
| ⚠️ **Running Warning** | Warns you if Discord is running and will be closed |
| 🔊 **Completion Sound** | Audio notification when fix completes |
| 🚀 **Startup Shortcut** | Optional auto-fix on Windows boot |
| ▶️ **Auto-Launch** | Starts Discord after patching |

---

## 🎛️ Buttons

| Button | Color | Description |
|--------|-------|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/Blue-5865F2?style=flat-square) | Apply fix to the selected Discord client |
| **Fix All** | ![Green](https://img.shields.io/badge/Green-57a657?style=flat-square) | Scan and fix all installed Discord clients at once |
| **Rollback** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/Gray-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/Orange-faa81a?style=flat-square) | Check if Discord has updated since last fix |

---

## ⚠️ Known Bugs

> [!WARNING]
> **ffmpeg.dll Limitations**
> 
> The current ffmpeg.dll has some known issues:
> - ❌ Notifications do not play
> - ❌ Soundboards do not work
> - ❌ GIFs may not play properly
> - ❌ Most MP3 and MP4 files will not play

> [!NOTE]
> **Upside:** ✅ The camera crashing issue is fixed with this version.
> 
> We are actively working on finding a better ffmpeg.dll to resolve these issues.

---

## 📦 Source Code

| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files and ffmpeg.dll |

---

## 👥 Credits

Made by **Oracle** | **Shaun** | **Terrain** | **Hallow** | **Ascend** | **Sentry**

---

## ⚖️ Disclaimer

> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
