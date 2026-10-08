# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Jekyll source for Liu Peng's personal website, hosted on GitHub Pages at the custom domain in `CNAME` (www.liupeng.eu). Pushing to `master` triggers GitHub Pages' automatic Jekyll build — there is no CI/CD config in this repo.

## Commands

```bash
bundle install                          # install gems (Ruby 3.3.7, see .ruby-version)
bundle exec jekyll serve --livereload   # local dev server at http://localhost:4000
bundle exec jekyll build                # build to _site/
```

No test suite or linter is configured.

## Architecture

- **Data-driven content**: experience, skills, awards, projects, and interests live as YAML in `_data/*.yml`, not hardcoded in pages. Edit the YAML to change content; the page markdown/layout just iterates over it.
- **`_includes/`**: one Jekyll include per card type (`experience-item.html`, `skill-category.html`, `award-item.html`, `project-card.html`, `interest-card.html`) — these render the corresponding `_data` entries and are the reusable building blocks for any new card-based section.
- **`pages/aboutme.md` and `pages/projects.md`**: thin markdown pages that pull in `_data` via the includes above.
- **`_layouts/default.html`**: the single layout used by all pages — holds the nav, header/hero (homepage only, gated by `page.layout == 'default' and page.url == '/'`), and footer. There are no other layouts.
- **Navigation** is defined in two places that must stay in sync: `_config.yml`'s `navbar-links` and the hardcoded `<nav>` markup in `_layouts/default.html`.
- **Styling**: `assets/css/style.css` is the main stylesheet, driven by CSS custom properties in `:root`; dark mode is pure `@media (prefers-color-scheme: dark)`, no JS. Font Awesome and Google Fonts (Inter) are loaded via CDN in the layout `<head>`.
- Ruby gems `csv` and `rexml` are pinned in the `Gemfile` for Ruby 3.3+/Cloudflare Pages compatibility with Jekyll 3.8.
