---
layout: page
title: Events list
permalink: /events/
---

<div class="list-group">
  {% for event in site.events %}
    <div class="h-event">
      <a href="{{ event.url | prepend: site.baseurl }}" class="list-group-item u-url">
        <h4 class="list-group-item-heading p-name">{{ event.title }}</h4>
        <p class="list-group-item-text">{% if event.dateend %}<time class="dt-start">{{ event.date | date: "%b %-d" }}</time> to <time class="dt-end">{{ event.dateend | date: "%b %-d, %Y" }}</time>{% else %}<time class="dt-start">{{ event.date | date: "%b %-d, %Y" }}</time>{% endif %}</p>
        <p class="list-group-item-text">
          {{ event.meta }}
        </p>
      </a>
    </div>
  {% endfor %}
</div>




