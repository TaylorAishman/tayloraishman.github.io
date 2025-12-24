---
layout: default
title: Thinking
---

## Reading Notes

{% assign reading_entries = site.readings | sort: "title" %}
{% if reading_entries.size > 0 %}
<ul>
  {% for entry in reading_entries %}
    <li>
      <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
      {% if entry.author %} — {{ entry.author }}{% endif %}
      {% if entry.summary %} — {{ entry.summary }}{% endif %}
    </li>
  {% endfor %}
</ul>
{% else %}
<p class="empty-state">No entries yet.</p>
{% endif %}

## Essays

{% assign essay_entries = site.essays | sort: "date" | reverse %}
{% if essay_entries.size > 0 %}
<ul>
  {% for entry in essay_entries %}
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
