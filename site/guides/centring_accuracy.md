---
layout: guides
title: Guides | Centring Accuracy 
description: This guide teaches you how to centre the accuracy on the playfield.
---

# Centring Accuracy

This guide will teach you how to centre the accuracy counter on the playfield.

Note that by doing this, the percentage symbol after the accuracy will disappear. This is due to osu! stopping to load the texture and loading only the hitbox, due to its size. Also note that this will work in all game modes, but will look off in osu!taiko as the accuracy counter is shifted downwards due to the taiko scoring animation.

Knowledge of HD and SD files is needed. If you do not know the difference between these, or how they work, please read [this part](https://skinship.xyz/tutorial/introduction#hdsd-elements-aspect-ratios-and-resolution) of the skinning tutorial.

## Roughly centring accuracy

This part of the guide will teach you how to roughly centre the accuracy counter - i.e. centring it 'good enough'. To learn how to perfectly centre accuracy, look at the `Perfectly centring accuracy` part of this guide.

1. Open your skin's folder. The folder can be found by navigating to the `Skins\` directory of your osu! installation. By default this will be located at `C:\Users\[User Name]\AppData\Local\osu!\Skins\`. You can locate this by pressing `CTRL + O` in the osu! window to bring up settings, clicking `Open osu! folder`, and navigating to the `Skins\` directory. Alternatively, you can go to settings, navigate to the `SKIN` section, and click `Open current skin folder`.
2. Find your osu! resolution's width. This will be the first number in your resolution setting (e.g. 1920 is the width of the resolution 1920x1080). You can find this by opening up osu! settings, navigating to the `GRAPHICS` section, and viewing the `Resolution:` setting.
3. Use the following formula to find the canvas width that your `score-percent(@2x).png` file will need to be:
(width / 2)/0.57
4. Using an image editor, change the canvas width of `score-percent(@2x).png` to the number you got from step 3.
5. Reload your skin using `CTRL + ALT + SHIFT + S`. Your accuracy will now be displayed in the centre of the playfield.

## Perfectly centring accuracy

This part of the guide will teach you how to perfectly centre the accuracy counter.

1. Same as in the `Roughly centring accuracy` section of this guide.
2. Same as in the `Roughly centring accuracy` section of this guide.
3. Find the width of your `score-0(@2x).png` file. All of your score number files should be the same resolution. Also find the width of your `score-dot(@2x).png` or `score-comma(@2x).png` if your locale uses commas for decimals.
4. Find your score number overlap. This is located inside the skin.ini at the `ScoreOverlap:` command under `[Fonts]`. If it is not specified, it will be `-2` by default.
5. Open your `score-percent(@2x).png` file in an image editor and use the following formula to find the width which the file will need to be:
(a / 2 - (b/2 + 2c + 3d))/2 for SD, or (a / 2 - (b/2 + 2c + 6d))/0.57 for HD<br>
Where:<br>
`a` is the width of your osu! resolution<br>
`b` is the width of `score-dot(@2x)` or `score-comma(@2x)`<br>
`c` is the width of `score-0(@2x).png`<br>
`d` is the value of `ScoreOverlap:` in the skin.ini
1. Change the canvas width of `score-percent(@2x).png` to the number you got from step 5.
2. Same as step 5 in the `Roughly centring accuracy` section of this guide.
