---
layout: default
title: 'deedoubledub'
---

<div class="row bio">
  <div class="col-md-8 col-md-offset-2">
    <img class="profile img-circle" src="/assets/images/profile.jpg" />

    <ul class="fa-ul pull-right bio-list">
      <li><i class="fa fa-li fa-user"></i> {{ site.data.about.name }}</li>
      <li><i class="fa fa-li fa-calendar-o"></i> {{ site.data.about.birthdate.month | append: ' ' | append: site.data.about.birthdate.day | append: ', ' | append: site.data.about.birthdate.year }}</li>
      <li><i class="fa fa-li fa-map-marker"></i> {{ site.data.about.location.city | append: ', ' | append: site.data.about.location.state }}</li>
      <li><i class="fa fa-li fa-graduation-cap"></i> {{ site.data.about.education.major | append: ', ' | append: site.data.about.education.institution | append: ', Class of ' | append: site.data.about.education.class }}</li>
      <li><i class="fa fa-li fa-briefcase"></i> {{ site.data.about.job.title | append: ', ' | append: site.data.about.job.employer }}</li>
      <li><i class="fa fa-li fa-envelope"></i> {{ site.data.about.email }}</li>
      <li><i class="fa fa-li fa-link"></i> {{ site.data.about.site }}</li>
    </ul>
  </div>
</div>

<div class="row">
  <div class="col-md-3">
    <h1 class="text-center">Technology</h1>
    <ul class="hacker">
      {% for post in site.categories.technology %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>

  <div class="col-md-3">
    <h1 class="text-center">Hiking</h1>
    <ul class="hacker">
      {% for post in site.categories.hiking %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>

  <div class="col-md-3">
    <h1 class="text-center">Gaming</h1>
    <ul class="hacker">
      {% for post in site.categories.gaming %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>

  <div class="col-md-3">
    <h1 class="text-center">Fireworks</h1>
    <ul class="hacker">
      {% for post in site.categories.fireworks %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
      </li>
      {% endfor %}
    </ul>
  </div>
</div>
