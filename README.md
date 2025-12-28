# 🎧 Stereo Installer

**One-click stereo audio restoration for Discord.**

![Version](https://img.shields.io/badge/Version-3.3-5865F2?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=flat-square)

---

## 🆕 What's New in v3.3

> [!TIP]
> **All bugs have been patched!** The ffmpeg.dll is no longer replaced, meaning full Discord functionality is preserved — notifications, soundboard, GIFs, and media previews all work perfectly.

| Before | After |
|:------:|:-----:|
| [![Before](https://i.ibb.co/j9x89156/before.png)](https://ibb.co/XfdWfv42) | [![After](https://i.ibb.co/WvqZ9n22/after.png)](https://ibb.co/jkBmKhrr) |
| *Original Discord Audio* | *99.9% Filterless Audio* |

---

## 🙌 Special Thanks

> **Huge shoutout to Sikimzo, Cypher , and Oracle** for the latest voice module fix that patched all the bugs! No more ffmpeg.dll replacement needed — everything just works now.

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
- 🔄 **Auto-Updates** — Detects Discord updates and alerts you
- 🎯 **Fix All** — Patch every installed client in one click
- 🧠 **Smart Detection** — Avoids double-patching shared folders
- ▶️ **Auto-Launch** — Starts Discord after patching
- 👁️ **High DPI Ready** — Scales correctly on 4K/1440p monitors

---

<details>
<summary><h2>🎛️ Buttons & Options</h2></summary>

<p align="center">
  <a href="https://ibb.co/NgSvzK6G">
    <img src="https://i.ibb.co/TDLf5tBN/GUI.png" alt="Stereo Installer GUI">
  </a>
</p>

### Buttons

| Button | Color | Description |
|--------|:-----:|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/_-5865F2?style=flat-square) | Apply fix to selected Discord client |
| **Fix All** | ![Blue](https://img.shields.io/badge/_-5865F2?style=flat-square) | Scan and fix all installed clients at once |
| **Rollback** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/_-faa81a?style=flat-square) | Check if Discord has updated since last fix |
| **Save Script** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Save script locally (required for startup shortcuts) |

### Options

| Option | Description |
|--------|-------------|
| Check for script updates | Checks GitHub for newer versions before applying fix |
| Auto-apply updates | Automatically downloads and applies script updates *(hidden until check enabled)* |
| Create startup shortcut | Creates a shortcut in Windows Startup folder |
| Run silently on startup | Skips GUI and auto-fixes all clients on boot *(hidden until shortcut enabled)* |
| Auto-start Discord | Launches Discord after the fix is applied |

</details>

<details>
<summary><h2>📂 File Locations</h2></summary>

| Path | Description |
|------|-------------|
| `%APPDATA%\StereoInstaller\settings.json` | Your preferences |
| `%APPDATA%\StereoInstaller\state.json` | Version tracking |
| `%APPDATA%\StereoInstaller\backups\` | Voice module backups |
| `%APPDATA%\StereoInstaller\DiscordVoiceFixer.ps1` | Saved script |

</details>

<details>
<summary><h2>📋 Changelog</h2></summary>

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

Made by **Oracle** · **Shaun** · **Terrain** · **Hallow** · **Ascend** · **Sentry** · **Sikimzo** · **Cypher**

---

> [!CAUTION]
> This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
