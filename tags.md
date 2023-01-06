---
layout: post
title: Topics
description: The different topics
permalink: /topics/
---

<div class="tags">
  <div class="tags-clouds">
    {% for tag in site.tags %}
    <a href="#{{ tag[0] }}">{{ tag[0] }}</a>
    {% endfor %}
  </div>
  {% for tag in site.tags %}
  <div class="tags-item" id="{{ tag[0] }}">
    <h2 class="tags-item-label">{{ tag[0] }}</h2>
    {% for post in tag[1] %}
    <a class="tags-post" href="{{ post.url | prepend: site.baseurl }}">
      <div>
        <span class="tags-post-title">{{ post.title }}</span>
        <div class="tags-post-line"></div>
      </div>
      <span class="tags-post-meta">
        <time datetime="{{ post.date }}">
          {{ post.date | date:"%Y-%m-%d" }}
        </time>
      </span>
    </a>
    {% endfor %}
  </div>
  {% endfor %}
  <p></p>
</div>