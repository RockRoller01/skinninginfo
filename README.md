## Skinning Tutorial

Website for skinship, one of the biggest osu! skinning communities.
https://skinship.xyz/

## Displaying notices

Set show_notice to true to display the notice, the content of the notice needs to be changed in the layout (master.html) tho, sadly can not manipulate that from \_config.yml.

The data to display can be found in \_data.

## Front Matter

every .md file need to have a front matter header with the following options

```
---
layout:
title:
description:
---
```

-   `layout` - This defines the layout of the site, aka the html template used for it. Please use the following:
    -   `tutorial` for all /tutorial/ articles
    -   `guides` for all /guides/ articles
    -   `resources` for all /resources/ articles
    -   All other layouts are for other general things or for specific pages. These 3 should fit all other categories.
-   `title` - This defines the title of the site and will show up as the name of the tab. It will also be displayed in the header on mobile pages. All titles should follow `Section | Title`, where section is either Guides, Resources, Tutorial or in case of a generic page skinship.
-   `description` - This defines the information shown in embeds and search results. Keep it short but concise.

## Formatting

Use `#` for the main heading of the site, all others need to be `##` or higher levels of headers.

Level 1 and 2 heading come with a divider due to our styling, so if you use those do not have a divider (`---`) directly before/after them.

All list styles are allowed. Tables can be padded to be human readable, but this is not required.

## Images

Depending on what you want to use the iamge for there are different spots for them:

-   tutorial:
    -   create a subfolder inside of /tutorial/img/ with the name of the tutorial
-   guides:
    -   put them into guides/img/
-   resources:
    -   create a subfolder inside of /resources/img/ with the name of the resource
-   anything else:
    -   everything else should go into /img/
