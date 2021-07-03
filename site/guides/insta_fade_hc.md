---
layout: master
highlight: guides
description: This guide will teach you how to convert hitcircles into instant fading ones.
title: Guides | Instant Fading HitCircles
---

# Creating Instant Fading HitCircles

This guide will teach you how to convert hitcircles into instant fading ones. You should know what SD and HD images are, if you don't, please read [this part](https://rockroller01.github.io/skinninginfo/tutorial/introduction#hdsd-elements-aspect-ratios-and-resolution) of the skinning tutorial.

If you do not know what instant fading hitcircles are I recommend you to watch [this short 7 seconds video](https://www.youtube.com/watch?v=C2b8PEHarvM). The benefit of instant fading hitcircles is obvious, you don't get the fade-out animation of the hitcircle, leaving you with less clutter. However, there are a few drawbacks:

-   Your Hitcircle Numbers will look weird at combos of above 9, which is why it is recommended to use dots instead of numbers, but it is not required.
-   You are limited to a single combo colour.

---

1. Upscale your `hitcircle` and `hitcircleoverlay` by 1.25 times.
2. Tint the `hitcircle` with a combo colour of your choice.
3. Take your upscaled `hitcircle` and `hitcircleoverlay` files, and overlap them. Make sure the `hitcircleoverlay` is on top.
4. Now take the overlapped hitcircle file, and place it under your hitcircle numbers (`default-1` till `default-9`). If you do not have default-# images, please open your skin.ini file and check for a line called `HitCirclePrefix:`, it can change the prefix. If this line is set, please proceed with the prefix it lists.
5. Make a completely blank `default-0` image, but give it the same size as `default-1` till `default-9`.
6. Now that you merged your hitcircle with your hitcircle numbers, remove the `hitcircle` and `hitcircleoverlay` files, and replace them with transparent images.
7. Now open your skin.ini configuration file, and set `Combo1` to the colour you used for the hitcircle. Then delete all other lines starting with `Combo2` and onwards.
    - `Combo1` makes it so that your approachcircle is the same colour as the hitcircle. If you have more than one `Combo#` command present the approachcircle will switch between the colours, but the hitcircle will not.
8. In skin.ini Under `[Fonts]`, set the `HitCircleOverlap` line to the width of your `default-1` image. (e.g. when your default-1 is 160 pixels wide, set it to 160)
    - Setting this prevents hitcircles from appearing incorrectly when the combo is longer than 10 circles
9. Reload your skin by pressing `CTRL`+`SHIFT`+`ALT`+`S` or restarting the client and you should have instant fading hitcircles.

You can also use the exact same method to achieve hitcircles which have a different colour depending on their number. For example making all even numbered circles blue and all uneven numbers red.
