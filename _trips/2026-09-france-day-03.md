---
layout: post
title: "France Day 3 - Notre Dame, KC BBQ, St Chapelle"
date: 2026-09-02
location: "Paris, France"
photo_folder: day-03
---
Started the day with another subway ride to Notre Dam Catehdral.  Very Impressive!  It was right on the the river.  Our tour guide, Marie, was aweseome she added so much detail to the trip.  For instance I now know what a flying butterss is.  Also she talked about how the church changed through the french revoltion (kinda crazy to think about)

After Notre Dam, we walked to another smaller church.  St Chapelle.  It was included in a complex of buildings that were used for the city of paris.  Think court house with this beautiful stained glass church inside of it.  Some of the pics below are from there.

I had on my list to check out the 'KC BBQ' place in the gothic quarter.  It wasnt really that good, but fun to see a smoker, hickory wood and some chiefs gear there!

We ended our sightseeing day by visiting a medieval museum.  It had remnants of ancient Roman baths.  

We then met up with Ed, Russ and James for dinner.  They just moved there from KC.  




### What do I remember about the day....
- I now know what a buttress is
- Meeting up with Ed / Russ / James for dinner
- Another fun subway ride with our group
- lots of steps





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

