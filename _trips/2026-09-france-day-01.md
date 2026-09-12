---
title: "France Day 1 - Arc de Triumph amd walking around"
date: 2026-08-31
location: "Paris, France"
photo_folder: day-01
---

## Day 1

 

We landed super early in the morning and explored a bit of Paris before we could check into our hotel.  
We walked to the Arc De Triomphe.  It is a large monument built by Napoleon to celebrate and honor fallen soldiers.  It is a massive round about with about 6 lanes of traffic moving around it.  Really cool to see on day 1.  
We wandered a bit and crashed pretty early because of the jet lag.  
We met the rest of our tour group later that night and got settled into our hotel.  
It’s a small hotel and the rooms are even smaller!  
Just ask Bethany, but really nice.

- billet 1
- bullet 2

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
