---
layout: default
title: Events list
permalink: /events/
---

<div class="home">

  <h1 class="page-heading">Events list</h1>

  <ul class="post-list">
    {% for event in site.events %}
      <li>
        <span class="post-meta">{% if event.dateend %}{{ event.date | date: "%b %-d" }} to {{ event.dateend | date: "%b %-d, %Y" }}{% else %}{{ event.date | date: "%b %-d, %Y %H" }}{% endif %}</span>

        <h2>
          <a class="post-link" href="{{ event.url | prepend: site.baseurl }}">{{ event.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>

  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>

</div>