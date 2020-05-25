---
layout: tutorial-sidenav
title: Main Menu
---

# Main Menu

The main menu consists of 4 files:
- ``menu-background.jpg``, ``welcome-text@2x``, ``seeya.wav`` and ``welcome.wav``

All of these four elements will only be shown to osu!supporters and ``seeya`` and ``welcome.wav`` will only play if they are enabled in the options, which they are by default. You can still skin them without being a supporter, they just will not show up in game for you. Welcome-text will be shown when you open up the game and welcome.wav plays at the same time. There isn't anything special to note about these. Seeya will play when you close the game.

``menu-background.jpg`` has a few things to note. First of all, you will probably have noticed that it has ``.jpg`` as its file format. It is the only element that can be a jpg and actually requires to be one. It will not show up as a ``.png``. Menu-background is shown on multiple screen:
- the main menu
- osu!direct
- in the lobby and multiplayer rooms
- on beatmaps that don't have their own background

This makes it quite hard for some to come up with a good design. If menu-background would only show up on a single screen, for example the main menu you could add things to it that pronounce e.g. parts of the music player or osu!direct. You can however only really do this if it won't look weird on other screen. Adding a background where the player listing in a multiplayer room is may look good in those rooms, but most likely will not look good on any of the other screen. You can only really add features like this to your menu-background if you find a way to cleverly incorporate them into your design in a way which won't make them look bad on the other screen.

Something else you might have noticed is that I did not add the HD prefix to it when listing all the files. Menu-background is the only element besides fail-background that scales to the screen. This means you can make a HD version, but save it as the SD image. No matter what resolution you use, it will scale to it. This allows you to save a bit of file size, which is really nice, since depending on your exact design menu-background can be multiple megabytes, while most images are in the range of a couple hundred kilobytes.

Below you can find a template of the menu-background that shows how much space the cookie will take up. This template is from one of the various official fanart contests.

<details><summary>Image</summary>

<img src="img/main_menu/main_menu_template.png" style="width:100%">

</details>