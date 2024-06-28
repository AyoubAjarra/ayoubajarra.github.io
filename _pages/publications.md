---
layout: page
permalink: /publications/
title: Publications
description: Preprints under progress, please come back later.
nav: true
nav_order: 1
---

<div class="publications">
  {% assign publications = site.data.papers | where_exp: "item", "item.entry_type == 'article'" %}
  {% for pub in publications %}
    <div class="publication">
      <h2>{{ pub.title }}</h2>
      <p><strong>Authors:</strong> {{ pub.author }}</p>
      <p><strong>Journal:</strong> {{ pub.journal }}</p>
      <p><strong>Year:</strong> {{ pub.year }}</p>
      {% if pub.url %}
        <p><a href="{{ pub.url }}" target="_blank">PDF</a></p>
      {% endif %}
    </div>
  {% endfor %}
</div>

