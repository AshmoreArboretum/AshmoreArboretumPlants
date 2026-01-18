---
title: Plants by Scientific Name 2
permalink: /scientific/
---

# Plants by Scientific Name

<ul>
{% assign sorted_plants = site.plants | sort: 'scientific_name' %}
{% for plant in sorted_plants %}
  <li><a href="{{ plant.url }}">{{ plant.scientific_name }}</a> ({{ plant.common_name }})</li>
{% endfor %}
</ul>
