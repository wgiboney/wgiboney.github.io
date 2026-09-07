---
layout: default
title: Home
---

<h1>Welcome</h1>

<h2>Latest Posts</h2>
<ul>
{% for post in site.posts limit:15 %}
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a>
    <span> — {{ post.date | date: "%b %d, %Y" }}</span>
  </li>
{% endfor %}
</ul>

<h2><a href="{{ '/trips/' | relative_url }}">✈️ Trips</a></h2>
<p>Check out places I've traveled — <a href="{{ '/trips/' | relative_url }}">see all trips</a>.</p>
