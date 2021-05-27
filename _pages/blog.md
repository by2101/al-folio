---
layout: default
permalink: /blog/
---

<div class="post">
  <ul class="post-list">
    {% for post in site.blog %}
        <li>
          <h3><a class="post-title" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
          <p class="post-meta">{{ post.date | date: '%B %-d, %Y' }}</p>
          <p>{{ post.description }}</p>
        </li>
    {% endfor %}
  </ul>
</div>
