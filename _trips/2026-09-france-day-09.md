---
title: "France Day 9 -  A Taste of Normandy"
date: 2026-09-08
location: "Mont St-Michel, France"
photo_folder: day-09
---

## Day 8

 

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

