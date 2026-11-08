# WinNative × Cocoon — AUTO-RETURN v5

### The Android integration patch that returns you to Cocoon when you exit a WinNative session.

[⬇️ **Download AUTO-RETURN v5**](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/download/V1.1.0/Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)

> **What this is:** a custom-platform and player configuration for Cocoon Frontend. It is an integration patch for launching WinNative game shortcuts from Cocoon — it is not a game mod or a patch to the game files.

## ✨ What the patch does

- Launches exported WinNative game shortcuts directly from **Cocoon**.
- Adds a dedicated player entry: **WinNative Standard (Cocoon return)**.
- When you choose **Exit** in WinNative's side menu, the WinNative session closes and **Cocoon returns to the foreground**.
- Leaves your original game shortcuts, saves and artwork untouched.

## ✅ Verified behaviour

AUTO-RETURN v5 has been tested successfully by the project creator.

**Important:** the return-to-Cocoon behaviour applies when you launch a game through Cocoon using the custom player and then choose **Exit** from WinNative's side menu. It is not intended to intercept a game's own in-game Quit option or sessions started directly inside WinNative.

## Requirements

- Android device.
- Cocoon Frontend.
- WinNative Standard installed with package name `com.winnative.cmod`.
- At least one game added to WinNative and its shortcut exported.

## Installation

1. Download the JSON configuration from the link at the top of this page.
2. Open Cocoon and go to **Settings → Library & Data → Platforms → Custom Platform**.
3. Import the AUTO-RETURN v5 JSON file.
4. Open the **Windows (WinNative)** platform settings.
5. Set **Default player** to **WinNative Standard (Cocoon return)**.
6. Select the folder containing your exported WinNative shortcut files.
7. Launch a game from Cocoon. To return, open WinNative's side menu and tap **Exit**.

Keep each game's exported `.desktop`, `.png` and `.bin` files together. Select the folder containing those files, not an individual shortcut.

## Troubleshooting

**It returns to the WinNative library instead of Cocoon**
- Confirm that **WinNative Standard (Cocoon return)** is selected as Cocoon's default player.
- Make sure you imported v5, not an older configuration.
- Start the game from Cocoon and use WinNative's side-menu **Exit** option.

**Games do not appear in Cocoon**
- Check that Cocoon is reading the correct exported-shortcuts folder.
- Keep each game's related export files together.
- Re-export the shortcut from WinNative if a required file is missing.

**Cocoon says WinNative is not installed**
- Confirm that WinNative Standard is installed.
- Check that its Android package is `com.winnative.cmod`.

## Compatibility

| Component | Configuration |
|---|---|
| Platform | Android |
| Frontend | Cocoon |
| Launcher | WinNative Standard |
| Patch/configuration | AUTO-RETURN v5 |
| Exit-to-Cocoon flow | Confirmed by project creator |

Other devices, versions and WinNative variants may behave differently. Compatibility is not guaranteed beyond the tested setup.

## Feedback

To report a problem, open an issue and include your Android version/device, Cocoon version, WinNative build, and what happens after choosing **Exit**.

## Credits and disclaimer

An independent community project, not affiliated with or endorsed by the developers of Cocoon or WinNative. All product names belong to their respective owners.

Created by a community user with assistance from ChatGPT. Testing, feedback and contributions are welcome.
