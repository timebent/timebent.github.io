---
layout: post
title:  "Electrotactile maps"
subtitle: Audiovisual work
date:   2023-04-05 23:00 -0400
categories: music audiovisual
tags: [music]
---

{% assign categories = site.categories | sort %}
{% for category in site.categories %}
 <span class="site-tag">
    <a href="/category/{{ category | first | slugify }}/"
        style="font-size: {{ category | last | size  |  times: 4 | plus: 80  }}%">
            {{ tag[0] | replace:'-', ' ' }} ({{ category | last | size }})
    </a>
</span>
{% endfor %}