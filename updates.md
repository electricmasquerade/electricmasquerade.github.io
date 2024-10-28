---
layout: default
title: Updates
permalink: /updates/
---

<h2>Latest Updates</h2>

<ul class="post-list">
  {% for post in site.posts %}
    <li class="post-item">
      <a href="{{ post.url | relative_url }}">
        <h3>{{ post.title }}</h3>
      </a>
      <small class="post-date">{{ post.date | date: "%B %d, %Y" }}</small>
      <p>{{ post.excerpt | strip_html | truncate: 160 }}</p> <!-- Display excerpt (first 160 characters) -->
      <a href="{{ post.url | relative_url }}" class="read-more">Read more</a>
    </li>
  {% endfor %}
</ul>