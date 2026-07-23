---
layout: default
title: "Archivio"
permalink: /archive/
---

<section class="archive-container">
  <h2>Archivio</h2>
  <p class="archive-intro">Tutte le uscite quotidiane precedenti, in ordine cronologico.</p>

  <ul class="archive-list">
    {% for post in site.posts %}
      <li>
        <time class="archive-date" datetime="{{ post.date | date_to_xmlschema }}">
          {{ post.date | date: "%B %d, %Y" }}
        </time>
        <a href="{{ post.url | relative_url }}" class="archive-link">
          {{ post.title }}
        </a>
      </li>
    {% endfor %}
  </ul>
</section>
