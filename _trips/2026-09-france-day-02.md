---
layout: post
title: "France Day 2 – Versailles Palace and meeting our travel group"
date: 2026-09-01
location: "Paris, France"
photo_folder: day-02
---

## Taking the subway out to Versailles.
We took the subway out to Versailles.  Its a lot different from the town in Missouri!

Met up with my buddy Ed.  He just moved to France from KC the month before.  

Subway was kind of hectic and busy.  Our train pulled up to our stop and was packed!  We stepped in and joined the crowd.  It was neat how so many people used the subway.

Met up with our traveling group.  Wanted us to introduce our selves as the 'Traveling Ramboneys'!  We'll save that gem for the next tour group :)


[Hotel Room in Paris](https://youtube.com/shorts/7mnkoLI1Jck)

[Hall of Mirrors - Versailles Palace](https://youtube.com/shorts/DftOMX3nA98)

[Versailles Gardens](https://youtu.be/7lbJPNSGs4Q)



### What do I remember about the day....
- Subway ride; so cool how everyone packed in and politely; tons of people biking to work
- Train exchange on the way to Versailles
- Cool to meet up with Ed
- The Versailles gardens were very impressive!
- Had a great french cheeseburger and beer in Versailles
 


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
