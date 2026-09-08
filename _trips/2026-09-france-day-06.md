---
title: "France Day 6 - Bus ride, lorie valley, wine tasting, chateaus"
date: 2026-08-31
location: "Paris, France"
photo_folder: day-06
---

## Day 6

 

text about the day 

- billet 1
- bullet 2

[Video of us outside the louvre](https://youtube.com/shorts/alGdww2k9Cg?is=IRszzi1hSIFfp6D-)


{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}
{% assign france_images = site.static_files | where_exp: "image", "image.path contains folder" %}

{% for image in france_images %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' or image.extname == '.webp' %}
<p>
  <a href="{{ image.path }}">
    <img src="{{ image.path }}" 
         alt="{{ image.name | split: '.' | first }}" 
         style="max-width: 100%; height: auto; display: block; margin: 1rem 0;">
  </a>
</p>
{% endif %}
{% endfor %}

