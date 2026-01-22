---
layout: default
title: Plants by Common Name
permalink: /common/
---

# <span style="font-size: 1.5rem;">Plants by Common Name</span>

Number of plants: {{ site.plants | size }}

<ul>
{% assign sorted_plants = site.plants | sort: 'common_name' %}
{% for plant in sorted_plants %}
  <li><a href="{{ plant.url | relative_url }}">{{ plant.common_name }}</a> ({{ plant.scientific_name }})</li>
{% endfor %}
</ul>
