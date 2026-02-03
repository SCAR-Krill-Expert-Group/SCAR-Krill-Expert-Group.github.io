---
layout: page
title: Events
permalink: /events/
---

## Upcoming Events

Find details on SKEG symposia, workshops, webinars, and other opportunities to connect with the krill research community.

{% assign event_posts = site.posts | where: "category", "events" %}
{% if event_posts.size > 0 %}
  {% for post in event_posts %}
  <article>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {{ post.excerpt }}
  </article>
  <hr>
  {% endfor %}
{% else %}
  *No events posted yet. Check back soon!*
{% endif %}

---

## Past Events

*Archive coming soon*
