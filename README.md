# Terminal Jekyll Site Framework

This repository hosts a production-ready Jekyll framework for a terminal-style portfolio and writing archive. It is designed for GitHub Pages deployment and keeps all content in a single-column, reading-focused layout.

## Add content

Create new entries in the Jekyll collections below:

- Projects: `_projects/`
- Dev diaries: `_diaries/`
- Tech notes: `_notes/`
- Reading notes: `_readings/`
- Essays: `_essays/`

Use the templates in `projects/_project_template.md`, `diaries/_diary_template.md`, `notes/_note_template.md`, `thinking/readings/_reading_template.md`, and `thinking/essays/_essay_template.md` as starting points.

### Required front matter fields

**Projects**
- `title`
- `summary`
- `repo`
- `tags`
- `date` (optional)
- `status`

**Dev Diaries**
- `title`
- `date`
- `project`
- `summary`
- `commit_links` (optional list)
- `pr_links` (optional list)

**Tech Notes**
- `title`
- `source`
- `tags`
- `summary`

**Readings**
- `title`
- `author`
- `year`
- `tags`
- `summary`

**Essays**
- `title`
- `date`
- `tags`
- `summary`

## Local development (standard network)

```bash
bundle install
bundle exec jekyll serve
```

## Local development (restricted network fallback)

If `bundle install` cannot reach RubyGems, use Docker:

```bash
docker run --rm -it -p 4000:4000 -v "$PWD":/srv/jekyll jekyll/jekyll:4 \
  jekyll serve --watch --force_polling --host 0.0.0.0
```

## GitHub Pages enablement

If Pages is not yet configured:

1. Settings → Pages
2. Deploy from a branch → `main` / `(root)`
3. Save

## Resume file

If `resume.pdf` is present in the repository root, the navigation will link directly to it. If it is absent, the navigation points to the Resume section on the home page with instructions for adding the file.
