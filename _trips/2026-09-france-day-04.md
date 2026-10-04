---
layout: post
title: "France Day 4 - Louvre and more walking"
date: 2026-09-03
location: "Paris, France"
photo_folder: day-04
---

The day started off with a neighborhood tour near the Louvre.  There are some absolutely beautiful gardens here!  We saw several today.

Tour of the Louvre with one of our specialized guides.  So much was squeezed in a short time.  We were able to see David, the winged angel and the mona lisa!  The mona lisa was ok.  Not work the hype, but great to see.  It was so nice to have a guide who talked about several of the pieces in the meseue.  We could for sure come back and see more.

The outside grounds of the Louvre were beautiful as well.

[Video of us outside the louvre](https://youtube.com/shorts/alGdww2k9Cg?is=IRszzi1hSIFfp6D-)

[More Louvre](https://youtu.be/O-iNs-6GSxo)



### What do I remember about the day....
- 1664 beer was good
- the palace next to the Louvre was nice to walk
- lots of walking
- Too sweaty and too late for Hemingway bar; next time


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

