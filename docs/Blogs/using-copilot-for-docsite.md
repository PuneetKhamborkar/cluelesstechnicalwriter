---
layout: post
title: "How I Used GitHub Copilot to Build My Tech Docs Site"
permalink: /Blogs/using-copilot-for-docsite/
date: 2026-03-19
toc: true
sidebar: Blogs
---

I am building a documentation site in Jekyll with the Minimal Mistakes theme, and GitHub Copilot has been my development partner. This post explains a complete, repeatable process for technical writers to use AI to generate SEO-friendly docs, navigation, and site architecture.

## What I did with Copilot

- Built and enriched the S-Docs section with user manual, configuration guide, API docs, release notes, quick start, quick installation, troubleshooting, and new feature docs.
- Added InfoDev Uni learning content for markup comparison, XML/DITA basics, and structured authoring concepts.
- Created a dedicated S-Docs landing page at `/S-Docs/` with meaningful internal links and a strong SEO title/description for high visibility.
- Standardized UI by setting `toc: true` and `sidebar: nav` across all documentation pages except homepage.
- Implemented a hierarchical sidebar tree in `_data/navigation.yml`, including nested “AcmeTasker (sample docs)” entries.

## How Copilot improves technical documentation productivity

- Generates first-pass drafts for headings, paragraphs, and lists based on prompts (e.g., “create user manual steps for task management software”).
- Suggests consistent, keyword-rich content for title, description, and long-form text (which boosts SEO indexability).
- Helps detect and fix invalid characters in markdown, ensuring Jekyll compliance and UTF-8 stability.
- Accelerates navigation schema updates (validate `_data/navigation.yml` format, add new pages, keep permalinks synchronized).

## Technical SEO checklist implemented

1. unique page titles and meta descriptions (`title`, `description`, `keywords` in front matter)
2. clean, semantic headings (`h1`/`h2`/`h3`) and an “On this page” local TOC section
3. proper canonical paths through `permalink` values and consistent sidebar URLs
4. internal links to key sections and site sections (InfoDev Uni, S-Docs, Beyond InfoDev)
5. markdown content that is clear, scannable, and keyword-optimized

## Best practices for writer+AI collaboration

1. treat Copilot output as draft content, then refine for accuracy and voice.
2. maintain format consistency in YAML front matter and use theme-ready flags (`toc`, `sidebar`, `layout`).
3. preserve reusable text patterns and scaling with template snippets (for guides, checklists, API endpoints).
4. run `bundle exec jekyll build` regularly to catch syntax or navigation regressions.

## Final verification step

- Start local server: `bundle exec jekyll serve`
- Validate pages:
  - `/` (homepage)
  - `/S-Docs/` (landing)
  - `/S-Docs/introduction/`
  - `/S-Docs/user-manual/`, etc.
  - `/Blogs/using-copilot-for-docsite/`
- Confirm sidebar tree includes S-Docs section and InfoDev Uni entries.
- Check the HTML for meta tags and ensure the content appears in the rendered page as expected.

By doing this, you can replicate an AI-assisted docsite workflow that is structured, maintainable, and optimized for search engines and human readers.
