---
layout: default
title: 'deedoubledub'
---

<div class="bio">
  <img id="profile" src="/assets/images/profile.jpg" />

  <ul class="fa-ul">
    <li><i class="fa fa-li fa-user"></i> {{ site.data.about.name }}</li>
    <li><i class="fa fa-li fa-calendar-o"></i> {{ site.data.about.birthdate.month | append: ' ' | append: site.data.about.birthdate.day | append: ', ' | append: site.data.about.birthdate.year }}</li>
    <li><i class="fa fa-li fa-map-marker"></i> {{ site.data.about.location.city | append: ', ' | append: site.data.about.location.state }}</li>
    <li><i class="fa fa-li fa-graduation-cap"></i> {{ site.data.about.education.major | append: ', ' | append: site.data.about.education.institution | append: ', Class of ' | append: site.data.about.education.class }}</li>
    <li><i class="fa fa-li fa-briefcase"></i> {{ site.data.about.job.title | append: ', ' | append: site.data.about.job.employer }}</li>
    <li><i class="fa fa-li fa-envelope"></i> {{ site.data.about.email }}</li>
    <li><i class="fa fa-li fa-link"></i> {{ site.data.about.site }}</li>
  </ul>
</div>

<h1>Technology</h1>
<ul>
  {% for post in site.categories.technology %}
  <li>{{ post.title }}</li>
  {% endfor %}
</ul>

<h1>Hiking</h1>
<ul>
  {% for post in site.categories.hiking %}
  <li>{{ post.title }}</li>
  {% endfor %}
</ul>

<h1>Gaming</h1>
<ul>
  {% for post in site.categories.gaming %}
  <li>{{ post.title }}</li>
  {% endfor %}
</ul>

<h1>Fireworks</h1>
<ul>
  {% for post in site.categories.fireworks %}
  <li>{{ post.title }}</li>
  {% endfor %}
</ul>
