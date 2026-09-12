---
title: "France Day 2 – Versailles Palace and meeting our travel group"
date: 2026-09-01
location: "Paris, France"
photo_folder: day-02
---

## Taking the subway out to Versailes.
We took the subway out to Versailes.  Its a lot different from the town in Missouri!
Subway was kind of hectic and busy.  Our train pulled up to our stop and was packed!  We stepped in and joined the crowd.  It was neat how so many people used the subway.


## Meeting our travel group

- link to hotel room

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
