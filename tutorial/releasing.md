---
layout: tutorial-sidenav
title: Releasing
description: Releasing your skin.
---

# Releasing Your Skin

There are two main places to release your skin, [the skinning forum](https://osu.ppy.sh/forum/15) and [the r/OsuSkins subreddit](https://www.reddit.com/r/OsuSkins/). Make sure to read the rules of the skinning forum **before** you post your skin. The major difference between the forum and the subreddit is, that the forum forbids mixed skins aka using other peoples part without their permission (besides stealing sounds, thats the only thing that is allowed) and NSFW content (this refers to skins, links to image sources and everything else!), while the subreddit allows those. However, the subreddit may allow mixed skins, but don't expect a positive response if your skin is mostly made up from other peoples elements.
There are a few things you should do when posting your skin:

-   Use [BBCode](https://osu.ppy.sh/help/wiki/BBCode) to format your post. Use Markdown or reddits editor if you post on the subreddit.
-   Either add a spoiler box and embed screenshots of the skin by using the `[img][/img]` tag or add a link to an imgur album that contains all screenshots.
-   You can make images that lead to sites by nesting an img tag inside of a url one.
    -   `[url=URL HERE][img]IMG URL HERE[/img][/url]`
-   Upload your skin to a reliable filehoster, such as mediafire, mega or google drive. Note that you should not use mediafire for skins with high file sizes, it has a very limited download speed. Under no circumstances use puu.sh or a similar service. Puu.sh deletes files if they are not frequently accessed, which is the reason why a lot of skins on the forum do not have a working download link anymore. Make sure to make a backup of your skin on another filehoster, in case the host you used stops its service or deletes the file for some reason.
-   Make some fancy banner. It may sound stupid, but it really helps your post to stand out.
-   Make sure that your skin does not contain any parts from another skin that weren't made by you (besides sounds) when posting in the skinning forum. This isn't a rule on the subreddit, but it always is appreciated if your skin is truly original.
-   Please link your sources. This isn't a rule, but it would be nice to link your font, the image sources, sound sources and whatever else you used. If we steal from artists the least we can do is to give them proper credit.

## Optimization

There are various things you can do to optimize your skins file size:

-   Reduce the file size of the images, the best way to do this is to use [pinga](https://css-ig.net/pingo). Make a copy of your skin and use it on the copy. Never use pinga on original files. With the default settings it will greatly reduce file sizes without losing any image quality. However, if you run it more than once on the same file you can see a noticeable loss of image quality. So if you publish e.g. an update for your skin, you need to update the original files, make a copy and then run pinga on those.
-   Make sure that applause, failsound and pause-loop are using .mp3 and not .wav. This is especially important if they are longer than 10 seconds, long audio files have big file sizes as .wavs.
-   If you want to include .psd files or other source files make sure to put them into their own separate download and not into the skin itself. Especially .psd files can easily use over 100mb combined for a full skin.
-   Make sure to not have any foreign or deprecated files inside of your skin. There are various files that are no longer used. Check [skinning history](https://osu.ppy.sh/help/wiki/Skinning/History) on the osu!wiki for a full list. [Skin checker](https://osu.ppy.sh/community/forums/topics/617168) can also list all files in your skin that are deprecated and/or foreign, if you don't want to manually check your skin.
