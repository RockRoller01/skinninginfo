---
layout: master
description: main site of skinship
title: skinship | Home
---

# Welcome!

This site is a collection of information related to osu! skinning. It is maintained by me, [RockRoller](https://osu.ppy.sh/users/8388854). The navigation bar at the top should lead you to everything you could want.<br>
If you encounter any problems with the site or any mistakes within its content please either notify me directly or go to the GitHub repository of this site and open an issue.

If you need any additional help with anything skinning related, feel free to ask on the forums or join the [skinship discord server](https://discord.skinship.xyz/).
If you want to contribute to this site, please contact me beforehand. Just opening a pull request without contacting me first may lead to wasted time. I don't upload all work in progress articles.

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
| 27/03/2021 |          Guide: Mixing Skins           |
| 15/03/2021 |    Guide: How to import osu! skins     |
| 09/02/2021 |        Resource: Fringe Remover        |
| 20/01/2021 |          Tutorial: Animations          |
| 13/01/2021 | Resource: 21:9 Song Selection Template |
| 29/07/2020 |   Guide: Non-Pulsating Combo Numbers   |
