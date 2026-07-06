# Portfolio restructure — what changed and how to apply it

## The problem this fixes
Old flow: Home → category card ("Selected Projects") → subcategory card ("NLP" / "ML" / "CV") → post card → post page.
That's 4 clicks to reach a single project.

New flow: Home → project card → post page (or straight to GitHub).
That's 1–2 clicks, and the card list updates automatically whenever you add a new post to `_posts/`.

## Files to add / overwrite in your repo
Copy these into the matching paths in `danknyan/odin`, overwriting where they already exist:

- `index.html` — new single-page hero + project grid + certs + CV button
- `_includes/project-card.html` — new, renders each project card
- `_data/certifications.yml` — new, light list powering the certifications section
- `_posts/2026-07-06-global-news-lens.md` — new featured project post
- `_posts/2026-07-05-augvit-pdd.md` — new featured project post
- `_scss/_project-cards.scss` — new, styling for cards/pills/cert list
- `css/styles.scss` — one line added (`@import "../_scss/project-cards";`)

Your other existing posts (SpaceX, Waze, HR churn, YouTube comments, concrete crack) don't need any changes — they'll automatically show up in the "More Projects" section since they don't have `featured: true` set.

## Placeholders you need to fill in
I kept these as explicit placeholders rather than guessing:

- `_posts/2026-07-06-global-news-lens.md` → `repo_url` and `demo_url` (currently `PLACEHOLDER_global-news-lens`)
- `_posts/2026-07-05-augvit-pdd.md` → `repo_url` (currently `PLACEHOLDER_augvit-pdd`)
- `_data/certifications.yml` → double-check the exact certificate titles match your credentials

## Files you can now delete (no longer used)
These were only reachable through the old category → subcategory click path, which no longer exists:

- `my-projects.html`
- `machine-learning.html`
- `natural-language-processing.html`
- `advanced-projects.html`
- `_layouts/subcategory.html`

**Keep** `_layouts/category.html`, `_data/category_list.yml`, and `_data/subcategory_list.yml` — `my-cv.html` and `my-values.html` still use the `category` layout, and `subcategory_list.yml` now powers the small tag label ("NLP", "Machine Learning", etc.) shown on each project card.

## To feature a new project later
Add a new markdown file to `_posts/`, e.g. `_posts/2026-08-01-my-new-project.md`:

```yaml
---
layout: post
title: "My New Project"
category: machine-learning        # or natural-language-processing / advanced-projects
subcategory: machine-learning
author: dan
featured: true                    # true = shows in "Featured Projects"; omit/false = "More Projects"
short-description: "One sentence describing the project."
repo_url: https://github.com/danknyan/my-new-project
demo_url: https://danknyan.github.io/my-new-project/   # optional
---

Write your project details here.
```

No edits to `index.html` needed — it appears automatically.
