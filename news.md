---
layout: single
title: News
permalink: /news/
---

![SKEG News Bulletin](/assets/skeg-new-bulletin-v2.png){: .align-center style="max-width: 600px;"}

## Latest Updates

Stay up to date with the latest from SKEG—research highlights, task force updates, member activities, and news from related meetings and workshops.

{% assign news_posts = site.posts | where: "category", "news" %}
{% if news_posts.size > 0 %}
  {% for post in news_posts %}
  <article>
    <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
    <p class="post-meta">{{ post.date | date: "%B %-d, %Y" }}</p>
    {{ post.excerpt }}
  </article>
  <hr>
  {% endfor %}
{% else %}
  *No news posted yet. Check back soon!*
{% endif %}
