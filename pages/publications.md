---
layout: page
title: Publications
permalink: /publications/
feature-img: "assets/img/pexels/book-glass.jpeg"
excluded: true
position: 4
tags: [Page]
---

{% assign count = 1 %}
{% for post in site.posts %}
{% if post.categories contains "Publications" %}
<div class="publication" style="border-left: 4px solid #98cbcf; padding-left: 10px; margin-bottom: 10px;">
<h3>{{ count }}. <a href="{{ post.url }}">{{ post.title }}</a></h3>
</div>
{% assign count = count | plus: 1 %}
{% endif %}
{% endfor %}
