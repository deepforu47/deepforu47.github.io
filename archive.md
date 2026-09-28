---
layout: page
title: Articles Archive
permalink: /archive/
description: A complete chronological archive of all blog posts.
---

{% if site.posts and site.posts.size > 0 %}
<div class="archive-container">
  {% for post in site.posts %}
    {% capture current_year %}{{ post.date | date: "%Y" }}{% endcapture %}
    {% if current_year != previous_year %}
      <h2 class="archive-year-heading">{{ current_year }}</h2>
      {% capture previous_year %}{{ current_year }}{% endcapture %}
    {% endif %}
    <article class="archive-item">
      <time datetime="{{ post.date | date_to_xmlschema }}" class="archive-date">
        {{ post.date | date: "%b %d" }}
      </time>
      <div class="archive-details">
        <a href="{{ post.url | relative_url }}" class="archive-title">{{ post.title }}</a>
        {% if post.tags and post.tags.size > 0 %}
          <span class="archive-tags">
            {% for tag in post.tags %}
              <span class="tag-badge">#{{ tag }}</span>
            {% endfor %}
          </span>
        {% endif %}
      </div>
    </article>
  {% endfor %}
</div>
{% else %}
<p>No articles found in archive.</p>
{% endif %}
