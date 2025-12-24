---
layout: default
title: Home
---

This site is a terminal-style framework for a portfolio and writing archive. Sections will populate as new entries are published.

## Sections

- [Projects]({{ "/projects/" | relative_url }})
- [Dev Diaries]({{ "/diaries/" | relative_url }})
- [Tech Notes]({{ "/notes/" | relative_url }})
- [Thinking]({{ "/thinking/" | relative_url }})

## Resume {#resume}

{% assign resume_file = site.static_files | where: "name", "resume.pdf" %}
{% if resume_file.size > 0 %}
The resume is available here: [Resume]({{ "/resume.pdf" | relative_url }}).
{% else %}
Add a `resume.pdf` file to the repository root to enable the resume link in the navigation.
{% endif %}
