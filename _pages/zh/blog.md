---
layout: default
permalink: /zh/blog/
pagination:
  enabled: false
  collection: posts
  permalink: /zh/blog/:num/
  per_page: 3
  sort_field: date
  sort_reverse: true
  trail:
    before: 1 # The number of links before the current page
    after: 3  # The number of links after the current page
---

<div class="post">
  <ul class="post-list">
    {% for post in site.blogzh %}
        <li>
          <h3><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
          <p class="post-meta">{{ post.date | date: '%B %-d, %Y' }}</p>
          <p>{{ post.description }}</p>
        </li>
    {% endfor %}
  </ul>

</div>
