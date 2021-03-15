---
layout: home
description: main site of skinship
title: skinship | Home
---

# Welcome!

You most likely got here by following the [forum post](https://osu.ppy.sh/community/forums/topics/881367) that is pinned in the [skinning forum](https://osu.ppy.sh/community/forums/15) or from my forum signature.

This site is a collection of information related to osu! skinning. It is maintained by me, [RockRoller](https://osu.ppy.sh/users/8388854). The navigation bar at the top should lead you to everything you could want.<br>
If you encounter any problems with the site or any mistakes within its content please either notify me directly or go to the GitHub repository of this site and open an issue, but please make sure that there is no issue already for your problem.

If you need any additional help with anything skinning related, feel free to ask on the forums, contact me directly via the forums or Discord: RockRoller#1909 or join the [skinship discord server](https://discord.skinship.xyz/).
If you want to contribute to this site, please contact me via Discord or the forums as well. Just opening a pull request without contacting me first may lead to wasted time. I don't upload all work in progress articles.

Thanks to all these people that helped me get this site up and running:<br>
[Death](https://osu.ppy.sh/users/3242450), [Enitoni](https://osu.ppy.sh/users/9118958), [MegaApple_Pi](https://osu.ppy.sh/users/2148208), [\_julia](https://osu.ppy.sh/users/11909549), [Matt2e2](https://osu.ppy.sh/users/12144912), [vvivi](https://osu.ppy.sh/users/10432755) and [Roan](https://osu.ppy.sh/users/8214639).

# Skinship Staff

<ul class="staff-grid">
  {% for staff in site.data.staff %}
    <li class="staff-item">
        <img class="avatar" src="https://a.ppy.sh/{{ staff.id }}">
        <div class="staff-description">
            <a href="https://osu.ppy.sh/users/{{ staff.id }}" class="name">{{ staff.name }}</a>
            <span class="role">{{ staff.role }}</span>
        </div>
    </li>
  {% endfor %}
</ul>

## Latest Updates

| Date       |                  Type                  |
| ---------- | :------------------------------------: |
| 15/03/2021 |    Guide: How to import osu! skins     |
| 09/02/2021 |        Resource: Fringe Remover        |
| 20/01/2021 |          Tutorial: Animations          |
| 13/01/2021 | Resource: 21:9 Song Selection Template |
| 29/07/2020 |   Guide: Non-Pulsating Combo Numbers   |
