# Stereo Installer

A one-click fix for Discord voice module issues. Automatically downloads and applies the latest voice module patches to restore stereo audio functionality.

## Quick Install

### Option 1: One-Line Command
Press `Win + R`, paste this command, and hit Enter:
```powershell
powershell -ExecutionPolicy Bypass -c "irm https://raw.githubusercontent.com/ProdHallow/installer/main/DiscordVoiceFixer.ps1 | iex"
```

### Option 2: Download Batch File
1. Download [StereoFix.bat](https://github.com/ProdHallow/installer/raw/main/StereoFix.bat)
2. Double-click to run

## Supported Clients

| Client | Type |
|--------|------|
| Discord Stable | Official |
| Discord PTB | Official |
| Discord Canary | Official |
| Discord Development | Official |
| BetterDiscord | Mod |
| Vencord | Mod |
| Equicord | Mod |

## Features

- Automatic updates — always runs the latest version
- Downloads fresh voice module files each run
- Creates optional startup shortcut to auto-fix on boot
- Auto-launches Discord after patching

## Source Code

| Repository | Description |
|------------|-------------|
| [ProdHallow/installer](https://github.com/ProdHallow/installer) | Installer script and batch file |
| [ProdHallow/voice-backup](https://github.com/ProdHallow/voice-backup) | Voice module backup files and ffmpeg.dll |

## Credits

Made by **Oracle** | **Shaun** | **Terrain** | **Hallow** | **Ascend**

## Disclaimer

This tool modifies Discord's voice module files. Use at your own risk. Not affiliated with Discord Inc.
