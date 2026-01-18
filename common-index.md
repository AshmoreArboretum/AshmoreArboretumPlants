---
title: Plants by Common Name
permalink: /common/
---

# Plants by Common Name

Collection files found: {{ site.plants | map: 'path' | join: ', ' }}

Number of plants: {{ site.plants | size }}

<ul>
{% assign sorted_plants = site.plants | sort: 'common_name' %}
{% for plant in sorted_plants %}
  <li><a href="{{ plant.url }}">{{ plant.common_name }}</a> ({{ plant.scientific_name }})</li>
{% endfor %}
</ul>

Try again
