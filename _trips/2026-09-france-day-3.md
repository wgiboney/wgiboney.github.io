---
title: "France Day 3"
date: 2026-08-31
location: "Paris, France"
photo_folder: day-03
---

## Day 3 – Paris On our own

 

text about the day 

- billet 1
- bullet 2



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

