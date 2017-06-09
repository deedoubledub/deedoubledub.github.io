---
layout: post
title: 'title'
date: YYYY-MM-DD
categories: cat1 cat2
imagepath: '/assets/images/YYYY/MM/post-slug/'
---

post content

# image include
{% capture url %}{{ 'image01.jpg' | prepend: page.imagepath }}{% endcapture %}
{% include image.html url=url caption="caption text" %}
