<div align="center">

# WinNative × Cocoon

### Launch Windows games from Cocoon — and return to Cocoon when you exit the WinNative session.

[Installation](#installation) · [How it works](#how-it-works) · [Troubleshooting](#troubleshooting)

</div>

---

## Overview

**WinNative × Cocoon** is an unofficial custom-platform configuration for Android. It lets Cocoon launch exported WinNative game shortcuts from your library.

The updated **AUTO-RETURN v5** configuration also fixes the return flow: when a game is launched from Cocoon and you choose **Exit** from WinNative's side menu (ending the WinNative session), WinNative closes and Cocoon comes back to the foreground.

> **Verified:** The AUTO-RETURN v5 flow has been tested successfully by the project creator on their Android device. Compatibility with other WinNative builds and Cocoon versions may vary.

## What's new in AUTO-RETURN v5

- **Direct return to Cocoon:** choosing **Exit** from WinNative's side menu closes the WinNative app instead of returning to its library.
- **Correct frontend launch identity:** the player sends the ACTION_VIEW intent, the winnative://com.winnative.cmod/shortcut URI, and the launched_from_pinned_shortcut=true extra expected by WinNative's exit handling.
- **Separate player identity:** the custom player has its own unique ID, so it can be distinguished from the regular WinNative Standard player in Cocoon.
- The original WinNative game shortcuts and exported artwork/data files remain unchanged.

## Requirements

- Android device.
- **WinNative Standard** installed (package: com.winnative.cmod).
- **Cocoon Frontend** installed.
- At least one game added to WinNative.
- Permission to access the folder where the exported shortcut files are stored.

## Installation

### 1. Export your games from WinNative

In WinNative, use its shortcut export feature for each game you want to show in Cocoon.

Keep the files belonging to each game together in the same folder. Exports may include:

- .desktop — game shortcut used to launch the game.
- .png — artwork.
- .bin — associated shortcut data.

Do not rename or separate the files belonging to the same game.

### 2. Download the updated configuration

Download **AUTO-RETURN v5**:

[**Windows-WinNative-Cocoon-AUTO-RETURN-v5.json**](Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)

This file supersedes the earlier FIX2, AUTO-RETURN, v3 and v4 test configurations.

### 3. Import it into Cocoon

1. Open **Cocoon**.
2. Go to **Settings → Library & Data → Platforms**.
3. Choose **Custom Platform** and import the downloaded v5 JSON.
4. Open the **Windows (WinNative)** platform settings.
5. Under **Default player**, select **WinNative Standard (Cocoon return)** — the custom player added by this configuration.

Cocoon may also show the regular **WinNative Standard** player. Make sure the custom **Cocoon return** player is selected.

### 4. Select the exported games folder

When Cocoon asks for the games directory, select the folder containing the exported WinNative shortcut files (for example, Games frontend).

Choose the folder that contains the exported files, not an individual game's .desktop file.

### 5. Launch and exit

Open **Windows (WinNative)** in Cocoon, choose a game and launch it.

To return to Cocoon, open WinNative's side menu and choose **Exit** to end the WinNative session. WinNative should close and Cocoon should reappear automatically.

**Note:** This return behaviour is tied to launching through the custom Cocoon player. Launches started directly inside WinNative are not expected to use the Cocoon return flow.

## Troubleshooting

### WinNative returns to its own library instead of Cocoon

- Confirm that Cocoon's **Default player** is set to **WinNative Standard (Cocoon return)**.
- Confirm that you imported the AUTO-RETURN v5 JSON, not an older configuration.
- Launch the game from Cocoon; do not start it directly from WinNative for this test.
- From WinNative's side menu, choose **Exit** to end the session.

### The Windows platform does not appear

- Check that the custom platform import completed successfully.
- Reopen Cocoon and verify that **Windows (WinNative)** is listed in the library.

### Games do not appear

- Verify that Cocoon is pointing to the folder containing the exported shortcuts.
- Keep each game's .desktop, .png and .bin files together.
- Re-export the shortcut from WinNative if required files are missing.

### Cocoon says the player is not installed

- Make sure WinNative Standard is installed.
- Check that the installed package is com.winnative.cmod.
- Select the custom player from this configuration rather than an unrelated WinNative build.

## Compatibility

| Component | Tested setup |
| --- | --- |
| Operating system | Android |
| Frontend | Cocoon |
| Launcher | WinNative Standard |
| Integration configuration | AUTO-RETURN v5 |
| Return flow | Confirmed by the project creator |

Other Android devices, WinNative variants and Cocoon releases have not all been tested. Please report your versions when opening an issue.

## Feedback and support

For problems or suggestions, open an issue in this repository. Helpful details include:

- WinNative version/build.
- Cocoon version.
- Android version and device.
- Whether the regular launch works and what happens after selecting **Exit**.

## Credits and disclaimer

This is an independent community project. It is not affiliated with, endorsed by, or supported by the developers of WinNative or Cocoon. Product and project names belong to their respective owners.

Created by a community user with assistance from ChatGPT. Contributions, testing and feedback are welcome.
