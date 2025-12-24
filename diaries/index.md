---
layout: default
title: Dev Diaries
---

## Dev Diary Index

{% assign entries = site.diaries | sort: "date" | reverse %}
{% if entries.size > 0 %}
<ul>
  {% for entry in entries %}
    <li>
      <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
      {% if entry.date %} — {{ entry.date | date: "%Y-%m-%d" }}{% endif %}
      {% if entry.summary %} — {{ entry.summary }}{% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty-state">No entries yet.</p>
{% endif %}
