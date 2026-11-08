# WinNative × Cocoon — AUTO-RETURN v5
## Exit-to-Cocoon integration patch for Android

**Purpose:** launch WinNative game shortcuts from Cocoon Frontend and return to Cocoon when the WinNative session is ended with **Exit** from WinNative's side menu.

### Download
[Download the AUTO-RETURN v5 configuration](https://github.com/themastertiger123-hue/WinNative-Cocoon-Integration/releases/download/V1.1.0/Windows-WinNative-Cocoon-AUTO-RETURN-v5.json)

### What's included
- A dedicated Cocoon player entry: **WinNative Standard (Cocoon return)**.
- The WinNative launch intent and frontend-session flag required for the tested return flow.
- A separate player identifier, so it can be selected independently from the regular WinNative Standard player.

### Installation
1. Import the JSON in Cocoon: **Settings → Library & Data → Platforms → Custom Platform**.
2. Open **Windows (WinNative)** and set **Default player** to **WinNative Standard (Cocoon return)**.
3. Select the folder containing your exported WinNative game shortcuts.
4. Launch a game from Cocoon.
5. To return to Cocoon, open WinNative's side menu and choose **Exit**.

### Important behaviour note
The return flow is for sessions launched from Cocoon with this custom player. It is triggered by WinNative's side-menu **Exit** option. It does not promise to intercept a game's own in-game Quit option or sessions started directly inside WinNative.

### Verification and compatibility
The project creator has confirmed that AUTO-RETURN v5 works on their Android device. Other devices, Cocoon versions and WinNative builds may differ.

This is an unofficial community integration patch. It does not modify game files and is not affiliated with the Cocoon or WinNative developers.
