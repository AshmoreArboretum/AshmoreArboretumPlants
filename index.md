---
layout: default
title: Ashmore Arboretum Plants
permalink: /
---

- [Plants by Common Name]({{ site.baseurl }}/common/)
- [Plants by Scientific Name]({{ site.baseurl }}/scientific/)

Or browse the full plant collection:

<ul>
  {% for plant in site.plants %}
    <li><a href="{{ plant.url | relative_url }}">{{ plant.common_name | default: plant.title }}</a></li>
  {% endfor %}
</ul>
