---
layout: post
title: "France Day 5 - Bus ride, medieval construction"
date: 2026-09-04
location: "Bourges, France"
photo_folder: day-05
---

The morning started with our first bus ride.  Our driver, Jan, was a pro!  He was from demnark and it was so crazy seeing him navigate this huge bus in Paris

Our first stop was a medieval castle that is being created.  The project started roughly 20+ years ago.  The plan is to build a medieval castle using the means that were avaiable at that time.  That means they mined stoned, chissled it, had a working blacksmith.  It was an impressive setup and they had made great progress.  Many of the photos are of that below.

Back on the bus and heading to our next place where we would spend the night, Bourges.  We stayed in the city center and had a walking tour of the church there.  It was as if not more impressive than Notre Dam, but with way less people.  We had a great dinner and learned about one of the cities heroe, Jacques Ceur.

## Day 5

[Hotel in Bourges](https://youtube.com/shorts/NpCb9sibnzU)


### What do I remember about the day....
- Bourges - Jacques Ceur -"To the brave hearts nothing is impossible”
- Could have stayed an extra day there and shopped
- Leaving my shorts in the room and Marie bringing them back
- Nice group dinner with wine



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

