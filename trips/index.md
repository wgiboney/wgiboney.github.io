---
layout: default
title: Trips
permalink: /trips/
---
<ul>
{% for trip in site.trips %}
  <li>
    <a href="{{ trip.url }}">{{ trip.title }} "-" {{ trip.date }}</a>
    {% if trip.location %} — {{ trip.location }}{% endif %}
  </li>
{% endfor %}
</ul>
