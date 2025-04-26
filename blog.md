---
layout: default
title: 'Development Log'
description: 'Thoughts on technology, education and more'
---

<section class="section">
  <div class="container">
    <h2>Latest Posts</h2>

    {% if site.posts != empty %}
      <div class="blog-list">
        {% for post in site.posts %}
          <article class="blog-post">
            <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
            <p class="post-date">{{ post.date | date: "%B %d, %Y" }}</p>
            <p class="post-excerpt">{{ post.excerpt | strip_html | truncate: 150 }}</p>
            <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
          </article>
        {% endfor %}
      </div>
    {% else %}
      <p>No posts yet! Check back soon. 🚀</p>
    {% endif %}

  </div>
</section>
