---
title: Plants by Scientific Name
permalink: /scientific/
---

# Plants by Scientific Name

Collection files found: {{ site.plants | map: 'path' | join: ', ' }}

Number of plants: {{ site.plants | size }}

<ul>
{% assign sorted_plants = site.plants | sort: 'scientific_name' %}
{% for plant in sorted_plants %}
  <li><a href="{{ plant.url }}">{{ plant.scientific_name }}</a> ({{ plant.common_name }})</li>
{% endfor %}
</ul>
