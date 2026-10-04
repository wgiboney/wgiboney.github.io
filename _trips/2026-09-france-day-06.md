---
layout: post
title: "France Day 6 - Bus ride, lorie valley, wine tasting, chateaus"
date: 2026-09-05
location: ", France"
photo_folder: day-06
---

The day started with a bus ride to the Lore Valley.  We stopped at a small castle where the current owners had a wine tasting for us.  Great owner with great energy!  We sampled some of his wines and chesse and then had our own picnic lunch on the castle grounds.

Back on the bus to our next stop, Chateau Chambord.  It is an extremely large estate.  I dont think the pictures fully show how impressive it is.

The middle of the chateau had a keep.  It allowed sunlight down into the lower levels. There was a dual stair case in the middle that circled the keep.  The light from the top of the keep looked like a bright light shining down into the bottom of the stairs.

Another feature of the Chateau was a dual stair case where you could see the people on the other side.  It was designed by Lenardo Divinci.


### What do I remember about the day....
- The Chataeu Chambord was impressive
- The wine / castle owner was a hoot
- Need to do more picnic lunches!  That was fun!




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

