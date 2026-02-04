---
layout: single
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

{% assign past_events = site.posts | where: "category", "events" %}
{% for post in past_events %}
{% if post.date < site.time %}
  {% unless post.title contains "2026" %}
<article>
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  <p class="post-meta">{{ post.date | date: "%B %Y" }}</p>
</article>
  {% endunless %}
{% endif %}
{% endfor %}

---

*For events prior to 2023, please visit the [SCAR Documents Archive](https://scar.org/~documents/science-4/life-sciences/skeg?layout=list).*
