<div align="center">

# WinNative × Cocoon

### Launch your Windows games directly from the Cocoon frontend on Android

A community-made custom platform configuration that connects **WinNative** with **Cocoon**, allowing you to launch exported Windows game shortcuts from your frontend library.

[Installation](#-installation) · [Compatibility](#-compatibility) · [Troubleshooting](#-troubleshooting)

</div>

---

## ✨ What this does

This custom Cocoon platform adds **Windows (WinNative)** to your library and uses WinNative to open the selected game's exported shortcut.

- Launch supported WinNative game shortcuts from Cocoon.
- Keep your Windows games organised in one frontend library.
- Use a simple JSON configuration—no separate launcher app required.

> **Project status:** Successfully tested by the creator on the setup listed below. This is an independent community configuration, not an official integration.

## 📋 Requirements

Before starting, make sure you have:

- An Android device.
- **WinNative Standard** installed.
- **Cocoon Frontend** installed.
- At least one game added to WinNative.
- The ability to export that game's shortcut files from WinNative.

## 🧪 Compatibility

| Component | Tested setup |
| --- | --- |
| Operating system | Android |
| Frontend | Cocoon |
| Launcher | WinNative Standard 0.8.0-beta |
| Games | Successfully tested with several games |

**Important:** The configuration has been tested with WinNative Standard **0.8.0-beta**. Other WinNative versions or modified builds have not been independently verified. Compatibility may vary.

## 🚀 Installation

### 1. Export your games from WinNative

In WinNative, use its **export/shortcut** feature for each game you want to add to Cocoon.

The exported files include:

- `.desktop` — game shortcut
- `.png` — image
- `.bin` — associated data file

**Keep the files belonging to each exported game together in the same folder.** Do not move or rename individual files after exporting them.

### 2. Download the configuration

1. Open this repository's **Releases** section.
2. Open the latest release.
3. Scroll to **Assets**.
4. Download `Windows-WinNative-Cocoon-FIX2.json`.

[**Open Releases**](../../releases)

### 3. Import the JSON into Cocoon

1. Open **Cocoon**.
2. Go to **Settings**.
3. Open **Library & Data → Platforms**.
4. Select **Custom Platform**.
5. Choose the downloaded `Windows-WinNative-Cocoon-FIX2.json` file.

### 4. Select your exported games folder

When Cocoon asks for the games directory, select the folder containing the exported WinNative shortcut files.

Example folder name: `Games frontend`.

Make sure you select the folder that contains the exported files—not a different parent folder or an individual game's file.

### 5. Launch a game

Cocoon should now show a platform named **Windows (WinNative)**.

Open that platform, select one of your imported games, and launch it. The game should open through WinNative.

## ↩️ Returning to Cocoon

When you exit a game, you may return to WinNative instead of Cocoon. This is the current behaviour of the setup: **exit WinNative once more** to return to the frontend.

## 🛠️ Troubleshooting

**The Windows (WinNative) platform does not appear**
- Check that the custom platform JSON was imported successfully.
- Make sure you selected the correct JSON file from the release.

**Games do not appear in Cocoon**
- Check that Cocoon is pointing to the folder containing the exported shortcuts.
- Keep each game's `.desktop`, `.png`, and `.bin` files together.
- Re-export the shortcut from WinNative if one of its files is missing.

**Cocoon says the player is not installed**
- Confirm that WinNative Standard is installed on your device.
- This configuration targets the Android package `com.winnative.cmod`.
- Make sure you are using the supplied configuration rather than an older test version.

**The game opens, but exiting it does not return directly to Cocoon**
- This is a known limitation of the current setup. Exit WinNative once more.

## 💬 Feedback and support

If you find a bug, have a question, or discover a way to improve the integration, please open an issue in this repository or leave a comment in the discussion where you found the project.

When reporting a problem, please include:
- Your WinNative version.
- Your Cocoon version.
- Your Android version.
- What happens when you try to import or launch a game.

That information makes it easier to investigate and reproduce the issue.

## 🙌 Credits and disclaimer

This configuration was created by a community user with help from ChatGPT and tested on the setup described above.

**This is an unofficial community project.** It is not affiliated with, endorsed by, or supported by the developers of WinNative or Cocoon. Product and project names belong to their respective owners.

If this configuration helps you, feel free to share it with other users. ❤️
