---
layout: inner
title: Project
permalink: /project/
paginate: true
---

<div class="post-list">
  {% for post in paginator.posts %}
    <div class="wow fadeIn">
      {% if post.position == "left" %}
        {% include content-left.html %}
      {% endif %}

      {% if post.position == "right" %}
        {% include content-right.html %}
      {% endif %}
    </div>
  {% endfor %}
</div>

{% include pagination.html %}
