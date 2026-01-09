# 🎧 Stereo Installer

**One-click stereo audio restoration for Discord.**

![Version](https://img.shields.io/badge/Version-3.5-5865F2?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=flat-square)

---

## 🆕 What's New in v3.5

> [!TIP]
> **NEW: Original Module Preservation!** The installer now automatically saves your original Discord voice modules on first use. These backups are **never deleted**, so you can always revert to mono audio if you decide stereo isn't for you. Look for `[ORIGINAL]` backups in the rollback menu!

| Before | After |
|:------:|:-----:|
| [![Before](https://i.ibb.co/j9x89156/before.png)](https://ibb.co/XfdWfv42) | [![After](https://i.ibb.co/WvqZ9n22/after.png)](https://ibb.co/jkBmKhrr) |
| *Original Discord Audio* | *99.9% Filterless Audio* |

---

## 🙌 Special Thanks

> **Huge shoutout to Sikimzo, Cypher, and Oracle** for the latest voice module fix that patched all the bugs! No more ffmpeg.dll replacement needed — everything just works now.

---

## 🚀 Quick Install

**Option 1: One-Line Command** *(Recommended)*

Press `Win + R`, paste this, and hit Enter:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/ProdHallow/installer/main/DiscordVoiceFixer.ps1 | iex"
```

**Option 2: Download**

Download [Stereo Installer.bat](https://github.com/ProdHallow/Discord-Stereo-Installer/releases/latest) and double-click to run.

<details>
<summary><strong>Option 3: Command Line (Advanced)</strong></summary>
```powershell
.\DiscordVoiceFixer.ps1 -Silent      # Auto-fix all clients without GUI
.\DiscordVoiceFixer.ps1 -CheckOnly   # Check if Discord has updated
.\DiscordVoiceFixer.ps1 -FixClient "Discord - Stable"   # Fix specific client
.\DiscordVoiceFixer.ps1 -Help        # Show help
```
</details>

---

## 💬 Supported Clients

| Official | Modded |
|:--------:|:------:|
| Discord Stable | Vencord |
| Discord PTB | BetterDiscord |
| Discord Canary | BetterVencord |
| Discord Development | Equicord |
| | Lightcord |

---

## ✨ Features

- 📂 **Any Drive Support** — Finds Discord on C:, D:, E:, etc. automatically
- 🛡️ **No Admin Needed** — Runs safely in user space
- 💾 **Safe Backups** — Backs up your voice module before patching
- 🔒 **Original Preservation** — First-time backups are kept forever for easy mono revert
- 🔄 **Auto-Updates** — Detects Discord updates and alerts you
- 🎯 **Fix All** — Patch every installed client in one click
- 🧠 **Smart Detection** — Avoids double-patching shared folders
- ▶️ **Auto-Launch** — Starts Discord after patching
- 👁️ **High DPI Ready** — Scales correctly on 4K/1440p monitors
- 🎛️ **EQ APO Fix** — One-click solution for EQ APO compatibility issues

---

<details>
<summary><h2>🎛️ Buttons & Options</h2></summary>

<p align="center">
  <a href="https://ibb.co/zHH6qnwd">
    <img src="https://i.ibb.co/zHH6qnwd/GUI.png" alt="Stereo Installer GUI">
  </a>
</p>

### Buttons

| Button | Color | Description |
|--------|:-----:|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/_-5865F2?style=flat-square) | Apply fix to selected Discord client |
| **Fix All** | ![Green](https://img.shields.io/badge/_-579E57?style=flat-square) | Scan and fix all installed clients at once |
| **Rollback** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/_-faa81a?style=flat-square) | Check if Discord has updated since last fix |
| **Apply EQ APO Fix Only** | ![Orange](https://img.shields.io/badge/_-faa81a?style=flat-square) | Apply only the EQ APO settings fix without patching voice module |
| **Save Script** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Save script locally (required for startup shortcuts) |

### Options

| Option | Description |
|--------|-------------|
| Check for script updates | Checks GitHub for newer versions before applying fix |
| Auto-apply updates | Automatically downloads and applies script updates *(hidden until check enabled)* |
| Create startup shortcut | Creates a shortcut in Windows Startup folder |
| Run silently on startup | Skips GUI and auto-fixes all clients on boot *(hidden until shortcut enabled)* |
| Auto-start Discord | Launches Discord after the fix is applied |
| **Fix EQ APO not working** | Replaces Discord settings.json with EQ APO-compatible version *(backs up original first)* |

</details>

<details>
<summary><h2>📂 File Locations</h2></summary>

| Path | Description |
|------|-------------|
| `%APPDATA%\StereoInstaller\settings.json` | Your preferences |
| `%APPDATA%\StereoInstaller\state.json` | Version tracking |
| `%APPDATA%\StereoInstaller\backups\` | Voice module backups (rotated, 1 per client) |
| `%APPDATA%\StereoInstaller\original_discord_modules\` | **Permanent** original backups (never deleted) |
| `%APPDATA%\StereoInstaller\settings_backups\` | Discord settings.json backups |
| `%APPDATA%\StereoInstaller\DiscordVoiceFixer.ps1` | Saved script |
| `%APPDATA%\discord\settings.json` | Discord settings (backed up when using EQ APO fix) |

</details>

<details>
<summary><h2>📋 Changelog</h2></summary>

### v3.5
- 🔒 **Original Module Preservation** — First backup for each client is now permanent
- 📁 **New Backup Structure** — Original backups stored separately in `original_discord_modules` folder
- 🔄 **Easy Mono Revert** — Restore original Discord modules anytime to go back to mono audio
- ⚠️ **Restore Warnings** — Special confirmation when restoring original (mono) backups
- 🎨 **Enhanced Rollback UI** — Original backups highlighted with `[ORIGINAL]` prefix
- 📝 **Check Button Update** — Now shows original backup status for selected client

### v3.4
- 🎛️ **EQ APO Fix** — Added one-click fix for EQ APO compatibility
- 💾 **Auto Backup** — Automatically backs up settings.json before replacement
- ⚠️ **User Confirmation** — Asks for confirmation before applying EQ APO fix
- 📝 **Detailed Logging** — Shows all EQ APO fix operations in status box
- 🔘 **Standalone Button** — Added "Apply EQ APO Fix Only" button for quick settings fix
- 🐛 **Bug Fixes** — Fixed invalid backup error when restoring discord voice modules for the first time

### v3.3
- 🐛 **All Bugs Patched** — Every known issue resolved
- 🎵 **No ffmpeg Replacement** — Full Discord functionality preserved
- 🔊 **99.9% Filterless Audio** — Near-perfect audio quality

### v3.2
- 🐛 Fixed Backup Manager syntax error
- ✨ Added Lightcord support
- 🧠 Smart de-duplication for "Fix All"
- 🤫 Silent Discord launch (no console spam)

### v3.1
- ✨ Custom drive support (D:, E:, etc.)
- ⚡ Fixed slow download speeds
- 👁️ High DPI support

### v3.0
- ✨ Settings persistence
- ✨ Full CLI support
- ✨ Live process monitoring

### v2.0
- Fix All Clients feature
- Backup and rollback functionality
- Discord update detection

</details>

---

## 📦 Source Code

[ProdHallow/installer](https://github.com/ProdHallow/installer) · [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup)

---

## 👥 Credits

Made by **Oracle** · **Shaun** · **Hallow** · **Ascend** · **Sentry** · **Sikimzo** · **Cypher**

---

> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
