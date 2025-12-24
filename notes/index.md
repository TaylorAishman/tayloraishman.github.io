---
layout: default
title: Tech Notes
---

## Tech Notes Index

{% assign entries = site.notes | sort: "title" %}
{% if entries.size > 0 %}
<ul>
  {% for entry in entries %}
    <li>
      <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
      {% if entry.summary %} — {{ entry.summary }}{% endif %}
      {% if entry.source %} (Source: {{ entry.source }}){% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty-state">No entries yet.</p>
{% endif %}
