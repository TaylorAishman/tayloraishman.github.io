---
layout: default
title: Projects
---

## Project Index

{% assign entries = site.projects | sort: "date" | reverse %}
{% if entries.size > 0 %}
<ul>
  {% for entry in entries %}
    <li>
      <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
      {% if entry.summary %} — {{ entry.summary }}{% endif %}
      {% if entry.repo %} (<a href="{{ entry.repo }}">Repo</a>){% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty-state">No entries yet.</p>
{% endif %}
