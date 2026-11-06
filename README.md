# WinNative-Cocoon-Frontend-Integration-Launch-Windows-games-directly-from-Cocoon-
WinNative + Cocoon Frontend Integration – Launch Windows games directly from Cocoon!

Hi everyone!

I managed to get WinNative working as a player in Cocoon, allowing me to launch Windows games directly from the frontend instead of opening WinNative manually.

I couldn't find an existing configuration for this combination, so I worked together with ChatGPT to create a custom Cocoon platform/player configuration.

I'm sharing our work with the community in case it's useful to other users!

Tested setup

- WinNative Standard 0.8.0-beta
- Cocoon Frontend
- Android
- Tested successfully with several games.

Installation guide

1. Export your games from WinNative

Use WinNative's export/shortcut feature to generate the game shortcuts.

The exported files include:

- ".desktop"
- ".png"
- ".bin"

Keep the exported files together in the same folder.

2. Download our custom Cocoon configuration

Download the attached file:

"Windows-WinNative-Cocoon-FIX2.json"

3. Import the configuration into Cocoon

1. Open Cocoon.
2. Go to Settings.
3. Open Library & Data → Platforms.
4. Select Custom Platform.
5. Choose the downloaded "Windows-WinNative-Cocoon-FIX2.json" file.

4. Select your games folder

When Cocoon asks for the games directory, select the folder containing your exported WinNative shortcuts.

For example: "Juegos frontend"

5. Launch your games!

Cocoon should now display a new platform called Windows (WinNative).

Select a game and launch it. It should open directly in WinNative!

One small detail

When you exit a game, you may find yourself back in WinNative rather than Cocoon. You simply need to exit WinNative once more to return to Cocoon.

About this configuration

This configuration was created by me with the help of ChatGPT. We worked together to develop and test a solution for integrating WinNative with Cocoon, as I couldn't find an existing configuration for this combination.

This is an independent project, not an official integration from the Cocoon or WinNative developers.

Feedback and support

If you run into any problems, have questions, or find something that could be improved, please leave a comment in this thread. I'll do my best to help and keep improving the configuration based on your feedback!

I hope it helps other WinNative users! ❤️
