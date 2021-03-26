---
layout: guides
title: Guides | Mixing Skins
description: This guide teaches you how to create your own personal mixed skin.
---

# Mixing Skins

This guide will teach you how to create your own personal mix skin. You will need to know the file names of assets in a skin. If you don't, please consult the [skinnable files list](https://docs.google.com/spreadsheets/d/1bhnV-CQRMy3Z0npQd9XSoTdkYxz0ew5e648S00qkJZ8/edit#gid=2074725196) for file names and other bits of information.

Please note that more often than not, the different skins' assets will look wildly different from each other. This means that mixing is often best reserved for mixing gameplay elements.

## Basic knowledge

For more information about the following, read [this part](https://skinship.xyz/tutorial/introduction#hdsd-elements-aspect-ratios-and-resolution) of the skinning tutorial.

- HD and SD images - Your game will either render SD or HD images depending on your resolution. To check this, open settings in-game, using `CTRL + O`, navigate to the `GRAPHICS` section, and find the `Resolution` setting. If you have a vertical resolution (the second value) of 800 or above, your game is using HD images. If it is less, your game will be using SD images. HD images have an `@2x` suffix appended to them (indicating that the image resolution is double that of the SD resolution). Note that if you use an HD resolution and no HD image is present for an element, it will automatically fall back to the SD image, if it is present. As such, you should be mixing with both HD and SD images so that your mixed skin displays correctly for anyone who wants to use it.
- .png vs. .jpg - osu! **only** supports .png images for skin elements, with **one** exception - `menu-background.jpg`, which must be a .jpg image.
- .mp3 vs. .wav - While osu! supports both .mp3 and .wav sounds, it prioritizes .wav sounds. If `failsound.mp3` and `failsound.wav` are both present, `failsound.wav` will play when you fail a map. As .mp3 is much smaller than .wav, it is recommended to use .mp3 for longer sounds such as `failsound.mp3` and `applause.mp3`. It is not recommended to use .mp3 for gameplay or interface sounds as they have a slight delay when playing.
- `skin.ini` - This file defines skin behavior, such as whether the cursor should expand or not, what color your combo colors are, etc. There are many more commands that dictate your skin's properties so read the `The skin.ini` section of this guide for more information.
- All animation frames start at 0.

## Mixing images

Mixing images is simple if you learn the different file names, or consult the skinnable files list. The steps are as follows:

1. Open the folders of the skins you want to mix from in your file explorer. These folders can be found by navigating to the `Skins\` directory of your osu! installation. By default this will be located at `C:\Users\[User Name]\AppData\Local\osu!\Skins\`. You can locate this by pressing `CTRL + O` in the osu! window to bring up settings, clicking `Open osu! folder`, and navigating to the `Skins\` directory. Alternatively, you can go to settings, navigate to the `SKIN` section, and click `Open current skin folder` for all skins you want to mix.
2. Create a new folder in the `Skins\` directory and name it something that you will remember, we will call our example `mixedskin`.
3. Select your mixed skin from the skins drop down list. This can be found by pressing `CTRL + O` to bring up settings, navigating to the `SKIN` section, and clicking on `Current skin:`.
4. Decide what images from which skins you want to use. For example, we want to use the cursor from `skin1`, the hitcircle and hitcircle overlay from `skin2`, and so on, in `mixedskin`.
5. Copy these images into the folder we created. We copy `cursor.png` and `cursortrail.png` from `skin1`, and `hitcircle.png` and `hitcircleoverlay.png` from `skin2`, and all of their HD equivalents, if present, into `mixedskin`
6. Reload your skin with `CTRL + ALT + SHIFT + S`. With our example, it should be the default skin with `skin1`'s cursor and `skin2`'s hitcircle. Make sure to reload your skin after all changes you make for those changes to take effect.
7. Repeat steps 4 and 5 until you have reached your desired result.

If you are mixing `default-x.png`, `score-x.png`, and/or `combo-x.png` numbers, please also read the `The skin.ini` section of this guide.

## Mixing animations

The steps for mixing animations are largely similar to the steps for mixing images, with only a few major differences:

- You will need to delete **all** animations and/or images of the same element already present in your mixed skin. (e.g. delete all `followpoint-x.png` files present if you wish to use followpoints from a different skin).
- You will have to copy **all** animation files.
- You might need to make sure that the `AnimationFramerate:` command in your mixed skin's `skin.ini` (talked about in the `The skin.ini` section of this guide) is set to the same value as it was set in the skin you are taking the animation from for some animations to look as they should. **Note that this will probably break other animations, such as `followpoint-x.png`, so most of the time it is better not to specify this command at all.**

Apart from these differences above, the process is the same as described in the `Mixing images` section of this guide.

## Mixing sounds

The steps for mixing sounds are also largely similar to the `Mixing images` section of this guide, with the difference that the files you are replacing will be .mp3 or .wav instead of .png. Follow the instructions in the `Mixing images` section, using sound files instead. Note that there are numerous menu sounds but you can get a full menu sound set with ~7 sound files.

## The skin.ini

There are a few things that you should check when mixing a skin:

- `AnimationFramerate:` - This dictates how many frames of an animation will be displayed in one second. If this command is not present, the default setting will be used which is to display all frames of an animation once every second. If the animation(s) you are copying over to your mixed skin relies on this command being set to 30 frames per second, 60 frames per second, etc., you will have to adjust other animations in your skin to compensate for this. For example, if we have to use an `AnimationFramerate` setting of `60` but our `followpoint-x.png` only goes up to 9 (10 frames), you will need to have six copies of each frame. Copy `followpoint-0` five times and name these copies `followpoint-1`, `followpoint-2`, and so on and so forth. Then do the same for the other 9 frames. Your followpoints will now look normal as they animate at the same framerate as your `AnimationFramerate` setting.
- `Combo#:` - This dictates your combo colors, i.e., the tint that is applied to your `hitcircle.png`, and `sliderstartcircle.png` in gameplay. This setting goes up to 8 and takes `r, g, b` color codes. Note that the combo colors start at `Combo2` and loop back around to finish on `Combo1`. The color is applied multiplicatively, so if you want your `hitcircle.png`, and `sliderstartcircle.png` to be un-tinted, use `Combo1: 255, 255, 255`. This setting also affects approach circles in osu!standard and fruits in osu!catch.
- `HitCirclePrefix:`, `ScorePrefix:`, `ComboPrefix:` - This dictates the prefix for the default, score, and combo images. Make sure to set these to the same prefix as the skin you copied the files from, or they will not display in game. Note that if your default, score, and/or combo images are in a nested folder, you will have to specify this here. For example, if your `default-x.png` images are in a folder called `num`, and are prefixed with `c-`, set `HitCirclePrefix:` to `num\c`.
- `HitCircleOverlap:`, `ScoreOverlap:`, `ComboOverlap:` - This dictates how many pixels the default, score, and combo images will overlap with each other. Higher values will lead to a greater overlap and lower values will lead to a lesser overlap. Note that this value is for the SD overlap, it will be doubled for HD resolutions and images. Set this to the same value as in the skin you mixed default, score, and combo images from if you want them to be spaced the same as that skin.
