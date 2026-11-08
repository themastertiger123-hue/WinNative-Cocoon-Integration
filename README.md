<div align="center">

# WinNative × Cocoon

### AUTO-RETURN v5 · Android integration patch

**Launch your WinNative games from Cocoon and return to Cocoon when you exit the WinNative session.**

[⬇️ Download the v5 configuration](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/download/V1.1.0/Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)
·
[View the release](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/tag/V1.1.0)

</div>

---

## What it does

This project adds a custom platform/player configuration to **Cocoon Frontend** for launching game shortcuts exported from **WinNative Standard**.

The AUTO-RETURN v5 player also makes WinNative return to Cocoon when you choose **Exit** from WinNative's side menu.

> This is an integration configuration, not a game mod. It does not patch game files or change your saves.

## Requirements

- Android device with **Cocoon Frontend** installed.
- **WinNative Standard**, using package name `com.winnative.cmod`.
- At least one game added to WinNative and its shortcut exported.

## Installation

1. Download the **AUTO-RETURN v5 JSON** using the download button above.
2. In Cocoon, open **Settings → Library & Data → Platforms → Custom Platform** and import the JSON.
3. Open the **Windows (WinNative)** platform settings.
4. Set **Default player** to **WinNative Standard (Cocoon return)**.
5. Select the folder containing your exported WinNative shortcut files.
6. Launch a game from Cocoon.

Keep each game's exported `.desktop`, `.png` and `.bin` files together. Select their containing folder, not an individual shortcut file.

## Returning to Cocoon

While the game is running, open WinNative's side menu and choose **Exit**. The WinNative session should close and Cocoon should come back to the foreground.

**Important:** this return behaviour is for games launched from Cocoon with the custom player. It is triggered by WinNative's side-menu **Exit** option; it is not intended to intercept the game's own Quit option or sessions started directly inside WinNative.

## Verification and compatibility

The project creator has successfully tested the AUTO-RETURN v5 return flow on their Android device. Other devices, Cocoon versions and WinNative builds may behave differently; compatibility beyond the tested setup is not guaranteed.

## Troubleshooting

| Problem | What to check |
|---|---|
| WinNative opens its library instead of returning to Cocoon | Make sure **WinNative Standard (Cocoon return)** is selected as the default player, then launch the game from Cocoon and use WinNative's side-menu **Exit**. |
| Games do not appear | Check that Cocoon is pointed at the folder containing the exported shortcuts. Keep each game's related export files together. |
| Cocoon says WinNative is not installed | Confirm that WinNative Standard is installed and its package name is `com.winnative.cmod`. |

## Report a problem

[Open an issue](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/issues) and include your Android device/version, Cocoon version, WinNative build, and what happened.

## Credits and disclaimer

An independent community project. It is not affiliated with, endorsed by, or supported by the developers of Cocoon or WinNative. Product names belong to their respective owners.

Created by a community user with assistance from ChatGPT. Testing and feedback are welcome.
