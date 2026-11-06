# WinNative × Cocoon
### Launch your Windows games directly from the Cocoon frontend on Android

A community-made custom platform configuration that lets **Cocoon** launch games through **WinNative**, so you can start your Windows games from your frontend library.

> **Status:** Tested and working with WinNative Standard 0.8.0-beta on Android.

---

## ✨ Features

- Adds **Windows (WinNative)** as a custom platform in Cocoon.
- Launches exported WinNative game shortcuts directly from Cocoon.
- Keeps your Windows games together in your frontend library.
- Community-made configuration; independent of the official WinNative and Cocoon projects.

## 📋 Tested setup

| Component | Version / platform |
| --- | --- |
| WinNative | Standard 0.8.0-beta |
| Frontend | Cocoon |
| Device | Android |
| Games | Successfully tested with several games |

## 🚀 Installation

### 1. Export your games from WinNative

Use WinNative's export/shortcut feature for the games you want to add to Cocoon.

The export creates related files with these extensions:

- `.desktop`
- `.png`
- `.bin`

**Important:** Keep each game's exported files together, in the same folder.

### 2. Get the configuration file

Download **Windows-WinNative-Cocoon-FIX2.json** from the **Releases** section at the bottom of this GitHub page, under **Assets**.

### 3. Import it into Cocoon

1. Open **Cocoon**.
2. Go to **Settings**.
3. Open **Library & Data → Platforms**.
4. Choose **Custom Platform**.
5. Select `Windows-WinNative-Cocoon-FIX2.json`.

### 4. Choose the games folder

When Cocoon asks for the games directory, select the folder containing the exported WinNative shortcut files.

For example: `Games frontend`.

### 5. Launch!

Cocoon should now show a platform named **Windows (WinNative)**. Open it, choose a game, and launch it.

---

## ↩️ Returning to Cocoon

When you exit a game, WinNative may remain open. To return to Cocoon, exit WinNative once more.

## 🛠️ Troubleshooting

- **Games don't appear:** Check that you selected the folder containing the exported shortcut files.
- **A game fails to launch:** Make sure its `.desktop`, `.png`, and `.bin` files are kept together.
- **Cocoon says the player is not installed:** Check that the custom platform JSON was imported successfully.

## 💬 Feedback

Found a problem or have an idea to improve the configuration? Open an issue or leave a comment in the discussion where you found this project. I'll do my best to help and improve it.

## ℹ️ Credits & disclaimer

This configuration was put together by a community user with help from ChatGPT and tested on the setup listed above.

**This is an unofficial community project.** It is not affiliated with, endorsed by, or supported by the WinNative or Cocoon developers. Product and project names belong to their respective owners.

If this setup helps you, feel free to share it with other users. ❤️
