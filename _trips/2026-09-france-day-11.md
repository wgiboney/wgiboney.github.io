---
title: "France Day 11 - Monets Garden and return to Paris"
date: 2026-09-10
location: "Giverny and Paris, France"
photo_folder: day-11
---

## Day 11

 

[Our last hotel room in paris](https://youtube.com/shorts/xdHOLyea6sY)






{% assign folder = '/assets/img/2026-france/' | append: page.photo_folder %}
{% assign france_images = site.static_files | where_exp: "image", "image.path contains folder" %}

{% for image in france_images %}
{% if image.extname == '.jpeg' or image.extname == '.jpg' or image.extname == '.png' or image.extname == '.webp' %}
<p>
<a href="{{ image.path }}">
<img src="{{ image.path }}"
alt="{{ image.name | split: '.' | first }}"
style="max-width: 400px; width: 100%; height: auto; display: block; margin: 1rem 0;">
</a>
</p>
{% endif %}
{% endfor %}
