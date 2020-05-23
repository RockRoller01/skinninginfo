---
layout: default
title: Using Dots for HitCircle Numbers
---

# Creating Instant Fading Hitcircles
This guide will teach you how to use dots for your hitcircle numbers. You should know what SD and HD images are, if you don't, please read [this part](https://rockroller01.github.io/skinninginfo/tutorial/introduction.html#hdsd-elements-aspect-ratios-and-resolution) of the skinning tutorial.

***

1. You need a dot. You can either make this yourself, or if you are making a mixed skin, take it from a skin that has them.
2. Open your skin.ini file and make remove the line **HitCirclePrefix:**, if it is present.
3. Remove the default-0 till default-9 images from your skin. You should move them into a subfolder and not just delete them, in case you want to switch back.
4. Save your dot as default-1 till default-9. For default-0 you need a blank image that has the same size as the one used for the dot.
5. Open the skin.ini again and set **HitCircleOverlap:** under **[Fonts]** to the width of default-1.png. It is important to use the width of the SD image here.
6. Reload your skin inside of osu by pressing CTRl+ALT+SHIFT+S. If everything went right you should now have dots for your hitcirclenumbers.