---
title: "Java"
layout: archive
permalink: /categories/java
author_profile: true
sidebar_main: true
sidebar:
  nav: "docs"
---


{% assign posts = site.categories.java %}
{% for post in posts %} {% include custom-archive-single.html type=entries_layout %} {% endfor %}