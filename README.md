# 🎧 Stereo Installer

**One-click stereo audio restoration for Discord.**

![Version](https://img.shields.io/badge/Version-4.0-5865F2?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5.1+-5391FE?style=flat-square)

---

## 🆕 What's New in v4.0

> [!TIP]
> **Smart Update Detection & Fix Verification!** The installer now automatically detects Discord updates on startup and prompts you to re-apply the fix. Plus, a new Verify Fix button lets you confirm the stereo fix is active using MD5 hash comparison!

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
``` powershell
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
- 🔍 **Auto-Detect Updates** — Scans all clients for version changes on startup
- ⚡ **Smart Auto-Fix** — Only re-fixes updated clients when auto-fix is enabled
- ✅ **Verify Fix** — Confirm stereo fix status with MD5 hash comparison
- 🎯 **Fix All** — Patch every installed client in one click
- 🧠 **Smart Detection** — Avoids double-patching shared folders
- ▶️ **Auto-Launch** — Starts Discord after patching
- 👁️ **High DPI Ready** — Scales correctly on 4K/1440p monitors
- 🎛️ **EQ APO Fix** — One-click solution for EQ APO compatibility (fixes ALL clients)
- 🔧 **Auto-Repair** — Automatically reinstalls corrupted Discord installations

---

<details>
<summary><h2>🎛️ Buttons & Options</h2></summary>

<p align="center">
  <a href="https://ibb.co/Y73x4ThW">
    <img src="https://i.ibb.co/C5zfpsQt/GUI.png" alt="Stereo Installer GUI">
  </a>
</p>

### Buttons

| Button | Color | Description |
|--------|:-----:|-------------|
| **Start Fix** | ![Blue](https://img.shields.io/badge/_-5865F2?style=flat-square) | Apply fix to selected Discord client |
| **Fix All** | ![Green](https://img.shields.io/badge/_-579E57?style=flat-square) | Scan and fix all installed clients at once |
| **Verify Fix** | ![Green](https://img.shields.io/badge/_-579E57?style=flat-square) | Check if stereo fix is active using MD5 hash comparison |
| **Rollback** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Restore voice module from a previous backup |
| **Backups** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Open the backup folder in Explorer |
| **Check** | ![Orange](https://img.shields.io/badge/_-faa81a?style=flat-square) | Check if Discord has updated since last fix |
| **Apply EQ APO Fix Only** | ![Orange](https://img.shields.io/badge/_-faa81a?style=flat-square) | Apply EQ APO settings fix to all installed clients |
| **Save Script** | ![Gray](https://img.shields.io/badge/_-464950?style=flat-square) | Save script locally (required for startup shortcuts) |

### Options

| Option | Description |
|--------|-------------|
| Check for script updates | Checks GitHub for newer versions before applying fix |
| Auto-apply updates | Automatically downloads and applies script updates *(hidden until check enabled)* |
| Create startup shortcut | Creates a shortcut in Windows Startup folder |
| Run silently on startup | Skips GUI and auto-fixes all clients on boot *(hidden until shortcut enabled)* |
| Auto-fix when Discord updates | Automatically re-applies fix when Discord updates are detected on startup *(enabled by default)* |
| Auto-start Discord | Launches Discord after the fix is applied |
| **Fix EQ APO not working** | Replaces settings.json for ALL Discord clients with EQ APO-compatible version *(backs up originals first)* |

</details>

<details>
<summary><h2>📂 File Locations</h2></summary>

| Path | Description |
|------|-------------|
| `%APPDATA%\StereoInstaller\settings.json` | Your preferences |
| `%APPDATA%\StereoInstaller\state.json` | Version tracking |
| `%APPDATA%\StereoInstaller\backups\` | Voice module backups (rotated, 1 per client) |
| `%APPDATA%\StereoInstaller\original_discord_modules\` | **Permanent** original backups (never deleted) |
| `%APPDATA%\StereoInstaller\settings_backups\` | Discord settings.json backups (per client) |
| `%APPDATA%\StereoInstaller\DiscordVoiceFixer.ps1` | Saved script |
| `%APPDATA%\discord\settings.json` | Discord Stable settings |
| `%APPDATA%\discordcanary\settings.json` | Discord Canary settings |
| `%APPDATA%\discordptb\settings.json` | Discord PTB settings |
| `%APPDATA%\discorddevelopment\settings.json` | Discord Development settings |

</details>

<details>
<summary><h2>📋 Changelog</h2></summary>

### v4.0
- ✅ **Verify Fix Button** — New button to verify stereo fix status using MD5 hash comparison against original backups
- 🔍 **Auto-Detect Discord Updates** — Automatically scans all installed clients for version changes on GUI startup
- ⚙️ **Auto-Fix on Discord Update** — New option to automatically re-apply fix when Discord updates are detected *(enabled by default)*
- 💬 **Update Prompts** — Shows detailed update notification with version changes (e.g., `v1.0.9176 -> v1.0.9177`)
- ⚡ **Smart Silent Mode** — When auto-fix enabled + updates detected, only fixes updated clients; when no updates, skips fix and just starts Discord
- 📊 **Status Bar Notifications** — Update detection status displayed in the status bar

### v3.7
- 🎛️ **Multi-Client EQ APO Fix** — EQ APO fix now applies to ALL installed Discord clients (Stable, Canary, PTB, Development)
- 🛡️ **Backup Validation** — Backups are now verified to contain actual files before being listed
- 🌍 **Locale Fix** — Fixed date parsing bug that caused backups to silently fail on non-US systems
- 📝 **Detailed Rollback Errors** — Rollback now explains exactly why it failed (missing files, corrupted metadata, empty backups, etc.)
- 🔍 **Corrupted Backup Detection** — Invalid backups are identified and reported instead of silently skipped
- ✅ **Restore Verification** — Confirms files were actually copied after restore completes
- 📊 **Backup Metadata** — Backups now track file count and total size for diagnostics
- 💾 **Per-Client Settings Backups** — Settings.json backups now include client name in filename
- 🧹 **Code Cleanup** — Streamlined codebase with minimal comments

### v3.6
- 🔧 **Improved Silent Mode** — Clear, actionable error messages when voice module isn't downloaded
- 📝 **Better Diagnostics** — Distinguishes between "no modules folder" and "no voice module" errors
- ✅ **Fixed Process Detection** — Correctly reports success when no Discord processes are running
- 🎯 **Smarter Error Handling** — Provides step-by-step instructions for missing voice module issue
- 🛠️ **Memory Execution Support** — Works reliably when running from memory via bat file or web download

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
