---
layout: guides
description: "This guide teaches you how to import skins of .osk, .zip, .rar, or .7z formats."
title: Guides | Importing osu! skins
---

# How to Import osu! Skins

This guide will teach you how to import skins, those that come as .osk files and those that come as .zip, .rar, and .7z files. This guide is written for Windows, but it should work on other operating systems with a few changes here and there.

Windows by default does come with a tool to extract .zip files, but it is very limited in functionality, therefore, if the skin you want to import is a .zip, .rar, or .7z, it is recommended to have one of the following:

-   [7-Zip](https://www.7-zip.org/)
-   [WinRAR](https://www.rarlab.com/download.htm)
-   Any other file compression/archiving software

## Importing .osk files

1. Find the skin you want to import and double click on it, or drag it into your osu! window.
2. The skin should now be imported into osu! and automatically switched to.

## Importing .zip, .rar, and .7z skins

1. Find the skin you want to import and right click on it.
2. On the context menu that shows up, click on `Extract` (make sure to extract to a folder of the same name). The actual name and location of this will vary depending on the software you use, if at all. For 7-Zip users, it will be located in `7-Zip > Extract to "[Skin Name]\"`.
3. After extracting, navigate to the new folder the files have extracted to. There will usually be one of three things present in the folder:
    - An .osk file
    - Another folder containing the skin's assets
    - The skin's assets
4. Import the skin in one of three ways depending on what is present in the extracted folder:
    - In the case that an .osk file is present, follow the instructions in the `Importing .osk files` section of this guide.
    - In the case that another folder containing the skin's assets is present, you will have to move this folder into the `Skins\` directory of your osu! installation. By default this will be located at `C:\Users\[User Name]\AppData\Local\osu!\Skins\`. You can locate this by pressing `CTRL + O` in the osu! window to bring up settings, clicking `Open osu! folder`, and navigating to the `Skins\` directory.
    - In the case that the skin's assets are present, move that folder into the `Skins\` directory of your osu! installation. Instructions on finding this directory are listed in the case directly above.
5. If you had the osu! client open and had to move a folder into your `Skins\` directory, reload your skins by pressing `CTRL + SHIFT + ALT + S`, and select the skin you just imported in the skins drop-down menu.
