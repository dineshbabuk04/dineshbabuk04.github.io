---
layout: default
title: Writing
description: Notes on distributed systems, engineering, and other things
permalink: /blog/
---

<div class="section-label">writing</div>

{% if site.posts.size > 0 %}
<ul class="post-list">
  {% for post in site.posts %}
  <li class="post-list-item">
    <time class="post-list-date">{{ post.date | date: "%Y-%m-%d" }}</time>
    <a href="{{ post.url | relative_url }}" class="post-list-title">{{ post.title }}</a>
    {% if post.description %}
    <p class="post-list-desc">{{ post.description }}</p>
    {% endif %}
  </li>
  {% endfor %}
</ul>
{% else %}
<p style="font-size:0.9rem; color: var(--text-dim);">Nothing published yet. Coming soon.</p>
{% endif %}
