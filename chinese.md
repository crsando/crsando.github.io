---
layout: default
title: Weekly
---

## Chinese

My Chinese Articles

<ul class="posts">
  {% for chinese in site.categories.chinese %}
    <li class="post">
      <a href="{{ chinese.url }}">{{ chinese.title }}</a>
      <time class="publish-date" datetime="{{ chinese.date | date: '%F' }}">
        {{ chinese.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>