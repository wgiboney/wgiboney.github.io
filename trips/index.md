---
layout: default
title: Trips
permalink: /trips/
---
<ul>
{% for trip in site.trips %}
  <li>
    <a href="{{ trip.url }}">{{ trip.title }}</a>
    {% if trip.location %} — {{ trip.location }}{% endif %}
  </li>
{% endfor %}
</ul>
