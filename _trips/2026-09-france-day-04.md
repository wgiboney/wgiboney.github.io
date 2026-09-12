---
title: "France Day 4 - Louvre and more walking"
date: 2026-09-03
location: "Paris, France"
photo_folder: day-04
---

## Day 4 - Neighborhood tour 
- Louvre 
- more walking

[Video of us outside the louvre](https://youtube.com/shorts/alGdww2k9Cg?is=IRszzi1hSIFfp6D-)


{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}
{% assign france_images = site.static_files | where_exp: "image", "image.path contains folder" %}

{% for image in france_images %}
{% unless image.name contains '-thumb' %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' or image.extname == '.webp' %}

{% assign basename = image.name | split: '.' | first %}
{% assign thumb_path = folder |append: '/' | append: basename | append: '-thumb' | append: image.extname %}

<p>
<a href="{{ image.path }}">
<img src="{{ thumb_path }}"
alt="{{ basename }}"
style="max-width: 400px; width: 100%; height: auto; display: block; margin: 1rem 0;">
</a>
</p>
{% endif %}
{% endunless %}
{% endfor %}

