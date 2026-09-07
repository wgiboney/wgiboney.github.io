---
title: "France Day 2"
date: 2026-09-01
location: "Paris, France"
photo_folder: Day-02
---




## Day 2 – Versailles (not like the Missouri town) 

and meeting up with ed ...


{% assign france_images = site.static_files | where_exp: "image", "image.path contains 'assets/img/2026-france'" %}
{% assign photo_path = 'assets/img/2026-france/' | append: page.photo_folder %}
{% assign day_photos = site.static_files | where_exp: "image", "image.path contains photo_path" %}




{% for image in day_photos %}
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