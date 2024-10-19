---
layout: default
title: Weekly
---

## Chinese

My Chinese Articles

<ul class="posts">
  {% for weekly in site.categories.chinese %}
    <li class="post">
      <a href="{{ weekly.url }}">{{ weekly.title }}</a>
      <time class="publish-date" datetime="{{ weekly.date | date: '%F' }}">
        {{ weekly.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>