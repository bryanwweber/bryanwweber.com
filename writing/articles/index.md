---
layout: default
title: Research Revealed
section: writing articles
---
  <h1>Research Revealed!</h1>
  <ul class="posts">
    {% for post in site.categories.articles %}
      <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></li>
      {% if post.excerpt %}
          {{ post.excerpt | markdownify }}
      {% else %}
          <p>No excerpt, sorry! Try clicking the title to read the whole post.</p>
      {% endif %}

    {% endfor %}
  </ul>