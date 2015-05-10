---
layout: page
title: Projects
permalink: /projects/
---

<div class="list-group">
  {% for project in site.projects %}
    <a href="{{ project.url | prepend: site.baseurl }}" class="list-group-item project">
      <img src="{% if project.image %}{{site.baseurl}}/img/projects/{{project.image}}{% else %}{{site.baseurl}}/img/cogs220.png{% endif %}" alt="{{project.title}}" title="{{project.meta}}" class="img-rounded project-logo img-responsive" />
      <h4 class="list-group-item-heading">{{ project.title }}</h4>
      <p class="list-group-item-text">
        {{ project.meta }}
        {% if project.tags %}<br/><br/>{{ project.tags }}{% endif %}
      </p>
    </a>
  {% endfor %}
</div>



  {% comment %}
  <p class="rss-subscribe">subscribe <a href="{{ "/feed.xml" | prepend: site.baseurl }}">via RSS</a></p>
  {% endcomment %}

