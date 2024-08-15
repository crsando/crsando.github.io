---
layout: default
title: Weekly
---

## Weekly

My Weekly Publication : **MacroDelivery**

The aim of this publication is focused on Chinese Bond Market and certain Global Commodities (Gold, Oil, etc.) that can be traded in Chinsese Futures Exchanges.

<ul class="posts">
  {% for weekly in site.categories.weekly %}
    <li class="post">
      <a href="{{ weekly.url }}">{{ weekly.title }}</a>
      <time class="publish-date" datetime="{{ thought.date | date: '%F' }}">
        {{ weekly.date | date: "%B %-d, %Y" }}
      </time>
    </li>
  {% endfor %}
</ul>