---
layout: page
title: Events list
permalink: /events/
---

<div class="list-group">
  {% for event in site.events %}
    <a href="{{ event.url | prepend: site.baseurl }}" class="list-group-item">
      <h4 class="list-group-item-heading">{{ event.title }}</h4>
      <p class="list-group-item-text">{% if event.dateend %}{{ event.date | date: "%b %-d" }} to {{ event.dateend | date: "%b %-d, %Y" }}{% else %}{{ event.date | date: "%b %-d, %Y" }}{% endif %}</p>
      <p class="list-group-item-text">
        {{ event.meta }}
      </p>
    </a>
  {% endfor %}
</div>




