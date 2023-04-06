---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
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