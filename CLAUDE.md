# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal blog built with **Jekyll** using the **Chirpy** theme (`jekyll-theme-chirpy`), deployed via **GitHub Pages**.

## Commands

```bash
# Install dependencies
bundle install

# Run locally
bundle exec jekyll serve        # http://127.0.0.1:4000

# Build for production
JEKYLL_ENV=production bundle exec jekyll b

# Test site (HTML validation)
bundle exec htmlproofer _site --disable-external
```

## Architecture

- **Theme:** `jekyll-theme-chirpy` (gem-based, v7.4+)
- **Config:** `_config.yml` — site title, URL, social links, theme settings
- **Posts:** `_posts/YYYY-MM-DD-title-slug.md`
- **Tabs:** `_tabs/` — sidebar navigation pages (about, archives, categories, tags)
- **Data:** `_data/contact.yml` (sidebar links), `_data/share.yml` (post sharing buttons)
- **Plugin:** `_plugins/posts-lastmod-hook.rb` — auto-sets `last_modified_at` from git history
- **Deployment:** `.github/workflows/pages-deploy.yml` — builds and deploys on push to `main`

## Blog Post Front Matter

```yaml
---
title: "Post Title"
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORY, SUB_CATEGORY]
tags: [tag1, tag2]
description: "Optional description for SEO"
---
```

## Theme Features

- Dark/light mode toggle (auto-follows system preference)
- Table of contents per post (`toc: true` by default)
- Categories and tags with archive pages
- Code syntax highlighting with line numbers
