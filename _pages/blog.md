---
layout: archive
title: "Blog"
permalink: /blog/
author_profile: false
---

<h3 class="archive__subtitle">모든 포스트</h3>

{% assign posts = site.posts %}
{% assign entries_layout = 'list' %}

<div class="entries-{{ entries_layout }}">
  {% for post in posts %}
    {% include archive-single.html type=entries_layout %}
  {% endfor %}
</div>
