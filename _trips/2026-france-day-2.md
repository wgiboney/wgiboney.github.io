---
title: "Day 2 – Paris On our own"
date: 2026-09-01
photo_folder: Day-2
---

Your write-up........

{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}
{% for image in site.static_files %}
{% if image.path contains folder %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' %}
[![{{ image.name | split: '.' | first }}]({{ image.path }})]({{ image.path }})
{% endif %}
{% endif %}
{% endfor %}