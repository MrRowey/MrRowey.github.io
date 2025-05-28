---
layout: default
title: 'Development Log'
description: 'Thoughts on technology, education and more'
---

<main class="section blog-section">
  <div class="container">
    <h2 class="section-title">Latest Posts</h2>

    {% if site.posts != empty %}
      <div class="blog-list">
        {% for post in site.posts %}
          <article class="blog-post" itemscope itemtype="http://schema.org/BlogPosting">
            <header>
              <h3 class="blog-post-title" itemprop="headline">
                <a href="{{ post.url | relative_url }}" itemprop="url">{{ post.title }}</a>
              </h3>
              <time datetime="{{ post.date | date_to_xmlschema }}" class="post-date" itemprop="datePublished">
                {{ post.date | date: "%B %d, %Y" }}
              </time>
            </header>
            <section class="post-excerpt" itemprop="description">
              {{ post.excerpt | strip_html | truncatewords: 30 }}
            </section>
            <a href="{{ post.url | relative_url }}" class="read-more" aria-label="Read full post titled {{ post.title }}">
              Read More &rarr;
            </a>
          </article>
        {% endfor %}
      </div>

      {% if paginator.total_pages > 1 %}
        <nav class="pagination" role="navigation" aria-label="Pagination">
          {% if paginator.previous_page %}
            <a href="{{ paginator.previous_page_path | relative_url }}" class="pagination-prev">← Newer Posts</a>
          {% else %}
            <span class="pagination-prev disabled">← Newer Posts</span>
          {% endif %}

          <span class="pagination-page">Page {{ paginator.page }} of {{ paginator.total_pages }}</span>

          {% if paginator.next_page %}
            <a href="{{ paginator.next_page_path | relative_url }}" class="pagination-next">Older Posts →</a>
          {% else %}
            <span class="pagination-next disabled">Older Posts →</span>
          {% endif %}
        </nav>
      {% endif %}

    {% else %}
      <p>No posts yet! Check back soon. 🚀</p>
    {% endif %}
  </div>
</main>
