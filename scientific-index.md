---
layout: default
title: Plants by Scientific Name
permalink: /scientific/
---
# <span style="font-size: 1.5rem;">Plants by Scientific Name</span>
Number of plants: {{ site.plants | size }}

<ul>
{% assign sorted_plants = site.plants | sort: 'scientific_name' %}
{% for plant in sorted_plants %}
  <li><a href="{{ plant.url | relative_url }}">{{ plant.scientific_name }}</a> ({{ plant.common_name }})</li>
{% endfor %}
</ul>
