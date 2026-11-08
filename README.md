<div align="center">

# WinNative × Cocoon

### AUTO-RETURN v5 — Android integration for Cocoon Frontend

**Launch your Windows games from Cocoon using WinNative Standard, then return straight to Cocoon when you exit the WinNative session.**

[⬇️ **Download AUTO-RETURN v5**](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/download/V1.1.0/Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)
&nbsp; · &nbsp;
[📦 **Latest release**](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/latest)
&nbsp; · &nbsp;
[🐛 **Report an issue**](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/issues)

![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?logo=android&logoColor=white)
![Frontend](https://img.shields.io/badge/Frontend-Cocoon-7B61FF)
![Launcher](https://img.shields.io/badge/Launcher-WinNative-2684FC)
![Version](https://img.shields.io/badge/Integration-AUTO--RETURN%20v5-2EA44F)

</div>

---

## 📖 Table of contents

- [Overview](#-overview)
- [Features](#-features)
- [Requirements](#-requirements)
- [Repository structure](#-repository-structure)
- [Installation](#-installation)
- [Using the integration](#-using-the-integration)
- [How AUTO-RETURN works](#-how-auto-return-works)
- [Troubleshooting](#-troubleshooting)
- [Compatibility and testing](#-compatibility-and-testing)
- [Version history](#-version-history)
- [Credits and disclaimer](#-credits-and-disclaimer)

## 🎮 Overview

**WinNative × Cocoon** is an unofficial custom-platform and player configuration for Android. It connects **Cocoon Frontend** with **WinNative Standard**, allowing game shortcuts exported from WinNative to appear in your Cocoon library and launch from there.

The main improvement in **AUTO-RETURN v5** is the session exit behaviour. When a game is launched through Cocoon with the custom player, choosing **Exit** from WinNative's side menu closes the WinNative session and brings Cocoon back to the foreground.

This project is a frontend integration patch: it configures how Cocoon starts WinNative. It does **not** modify the games themselves, game files, saves, or WinNative installations.

## ✨ Features

- **Cocoon library integration:** use exported WinNative game shortcuts from your Cocoon library.
- **Dedicated player entry:** adds **WinNative Standard (Cocoon return)**, separate from the regular WinNative Standard player.
- **Direct return to Cocoon:** the tested AUTO-RETURN flow brings Cocoon back when you select **Exit** in WinNative's side menu.
- **Existing game data stays untouched:** the configuration does not alter game files, saves, or exported artwork.
- **Easy to identify:** the current v5 configuration is kept separate from older files.

## 📱 Requirements

Before installing, make sure you have:

- An Android device.
- **Cocoon Frontend** installed.
- **WinNative Standard** installed with the Android package name `com.winnative.cmod`.
- At least one game added to WinNative.
- The game's shortcut exported from WinNative, including the associated export files.

## 📁 Repository structure

The repository is organised to distinguish the current patch from previous versions:

| Location | Contents | Which should I use? |
|---|---|---|
| `README.md` | Project overview, installation guide and troubleshooting | Start here |
| `config/` | Current AUTO-RETURN v5 JSON configuration | **Use this for the current setup** |
| `archive/` | Previous FIX2 configuration, retained for reference | Only for legacy setups |
| GitHub Releases | Versioned downloads and release information | **Recommended download location** |

For a new installation, download the JSON attached to the [latest release](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/latest). The archived FIX2 file is an older configuration and has been superseded by v5.

## 🛠️ Installation

### 1. Export your game shortcuts from WinNative

In WinNative, use its shortcut export function for the games you want to display in Cocoon.

Keep the files associated with each game together. Depending on the export, these can include:

- `.desktop` — the game shortcut Cocoon uses to identify and launch the game.
- `.png` — artwork for the shortcut.
- `.bin` — additional shortcut data.

Do not rename or separate files belonging to the same game.

### 2. Download AUTO-RETURN v5

Download the configuration file from the link at the top of this page:

**[Download Windows-WinNative-Cocoon-AUTO-RETURN-v5.json](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/download/V1.1.0/Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)**

The release download is the recommended file for installation.

### 3. Import the configuration into Cocoon

1. Open **Cocoon**.
2. Go to **Settings → Library & Data → Platforms**.
3. Open **Custom Platform** and import the downloaded JSON file.
4. Find the **Windows (WinNative)** platform in your library settings.
5. Under **Default player**, select **WinNative Standard (Cocoon return)**.

There may also be a regular **WinNative Standard** entry. Make sure you select the one that says **Cocoon return**, as this is the player containing the AUTO-RETURN launch configuration.

### 4. Choose your exported games folder

When Cocoon asks for the games directory, select the folder containing the WinNative shortcut exports.

For example, if your exported shortcuts are stored in a folder named `Games frontend`, select that folder. Do not select an individual `.desktop` file.

Once the folder is selected and Cocoon has scanned it, your exported games should appear in the Windows (WinNative) platform.

## ▶️ Using the integration

1. Open the **Windows (WinNative)** platform in Cocoon.
2. Choose the game you want to play.
3. Launch it using **WinNative Standard (Cocoon return)**.
4. When you have finished playing, open WinNative's side menu.
5. Select **Exit** to end the WinNative session.

After the WinNative session closes, Cocoon should return to the foreground.

> **Important:** AUTO-RETURN v5 is designed for the WinNative side-menu **Exit** action after launching through Cocoon with the custom player. It is not intended to intercept a game's own in-game Quit option, nor does the return flow apply to sessions started directly inside WinNative.

## 🔄 How AUTO-RETURN works

The custom player starts WinNative's display activity with the launch information expected by WinNative's shortcut/session handling. It includes the shortcut path, the Android `ACTION_VIEW` intent, the WinNative shortcut URI and the frontend-session flag.

This lets WinNative recognise the launch as coming from the Cocoon integration. When the session is ended with the supported **Exit** action, WinNative closes instead of leaving its library in front of Cocoon.

The v5 configuration also uses its own player identifier. This keeps **WinNative Standard (Cocoon return)** separate from the regular WinNative player entry in Cocoon.

You do not need to edit the JSON manually for a normal installation.

## 🧰 Troubleshooting

| Problem | What to check |
|---|---|
| WinNative returns to its own library instead of Cocoon | Confirm that **WinNative Standard (Cocoon return)** is selected as the default player. Start the game from Cocoon and use **Exit** in WinNative's side menu. |
| The game does not appear in Cocoon | Check that Cocoon is scanning the folder containing the exported shortcuts. Keep each game's `.desktop`, `.png` and `.bin` files together. |
| Cocoon says WinNative is not installed | Confirm that WinNative Standard is installed and that its package name is `com.winnative.cmod`. |
| The wrong WinNative player is being used | Open the Windows (WinNative) platform settings and select **WinNative Standard (Cocoon return)** as the default player. |
| The return behaviour does not happen when quitting a game | End the WinNative session using **Exit** from WinNative's side menu. The game's own Quit option is not the tested return method. |

If the problem persists, include your device model, Android version, Cocoon version and WinNative build when [opening an issue](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/issues).

## ✅ Compatibility and testing

The AUTO-RETURN v5 flow has been successfully tested by the project creator on an Android device.

| Component | Configuration |
|---|---|
| Operating system | Android |
| Frontend | Cocoon Frontend |
| Launcher | WinNative Standard |
| Android package | `com.winnative.cmod` |
| Custom player | WinNative Standard (Cocoon return) |
| Configuration revision | AUTO-RETURN v5 |
| Tested return action | WinNative side-menu **Exit** |

Compatibility with other Android devices, Cocoon versions and WinNative builds may vary. The return flow is confirmed on the creator's setup, but not every possible device or version combination has been tested.

## 🧾 Version history

### AUTO-RETURN v5 — current

- Added the frontend-session launch information required for the tested return-to-Cocoon flow.
- Added a dedicated player identifier to distinguish the custom player from regular WinNative Standard.
- Confirmed that ending the WinNative session through the side-menu **Exit** action returns to Cocoon on the creator's device.

### FIX2 — archived

The previous FIX2 configuration is retained in the `archive/` folder for reference. It is no longer the recommended version for new installations.

For downloads and version details, visit [GitHub Releases](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases).

## 🤝 Credits and disclaimer

This is an independent community project created to improve the workflow between Cocoon Frontend and WinNative Standard.

It is **not affiliated with, endorsed by, or supported by** the developers of Cocoon or WinNative. All product names and trademarks belong to their respective owners.

Created by a community member with assistance from ChatGPT. Testing reports, feedback and contributions are welcome.
