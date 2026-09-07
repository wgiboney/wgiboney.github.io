---
title: "Day 1 – Paris On our own"
date: 2026-08-31
photo_folder: Day-02
---

Your write-up...

{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}
{% for image in site.static_files %}
{% if image.path contains folder %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' %}
[![{{ image.name | split: '.' | first }}]({{ image.path }})]({{ image.path }})
{% endif %}
{% endif %}
{% endfor %}