---
title: "France Day 2 – Versailles Palace and meeting our travel group"
date: 2026-09-01
location: "Paris, France"
photo_folder: Day-2
---

## Taking the subway out to Versailes.
We took the subway out to Versailes.  Its a lot different from the town in Missouri!
Subway was kind of hectic and busy.  Our train pulled up to our stop and was packed!  We stepped in and joined the crowd.  It was neat how so many people used the subway.


## Meeting our travel group

- link to hotel room

{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}

{{ folder }}
{% for image in site.static_files %}
{{ image.path }}
{% if image.path contains folder %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' %}
[![{{ image.name | split: '.' | first }}]({{ image.path }})]({{ image.path }})
{% endif %}
{% endif %}
{% endfor %}