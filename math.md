---
layout: default
title: Weekly
---

## Math

My Math Collections

<ul class="posts">
  {% for math in site.categories.math %}
    <li class="post">
      <a href="{{ math.url }}">{{ math.title }}</a>
      <time class="publish-date" datetime="{{ math.date | date: '%F' }}">
        {{ math.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>