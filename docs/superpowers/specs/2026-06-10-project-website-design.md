# OpenTrace Project Website — Design

Approved 2026-06-10.

## Goal

A single-page, modern/academic project site outlining OpenTrace — an open data
standard and corpus for process-tracing data in decision research — published
automatically via GitHub Pages. The page makes no reference to AI/LLM usage.

## Architecture

- `site/index.html` + `site/styles.css`: hand-crafted static HTML/CSS, no build
  step, no JS frameworks. Inline SVG trace motif. Repo root stays free for the
  actual standard/corpus work later.
- `.github/workflows/deploy-pages.yml`: official GitHub Pages Actions workflow.
  On push to `main`, upload `site/` as the Pages artifact and deploy.
- Pages source must be set to "GitHub Actions" (via `gh api` or repo settings).

## Page sections (anchor nav)

1. Hero — name, tagline, GitHub link
2. Why — process-tracing data (eye-tracking, mouse-/cursor-tracing, Mouselab,
   think-aloud, response dynamics) is siloed in lab-specific formats, hindering
   reuse, meta-analysis, and reproducibility
3. The Standard — common data model: shared schema for trials, stimuli, AOIs,
   timestamped events; format-agnostic (CSV/JSON/Parquet); validation tooling
4. The Corpus — curated, openly licensed collection of standardized datasets
5. Roadmap — schema draft → reference converters → seed corpus → community
   governance (milestones, no invented dates)
6. Get involved — contribute datasets, comment on schema, GitHub issues
7. People — Michael Schulte-Mecklenbeck, University of Bern, links
8. Footer — license (MIT per repo LICENSE), repo link

## Visual direction

Clean tech-minimal: Inter-style sans-serif, near-white background, structured
grid, one restrained accent color, monospace touches for schema content.
Responsive; only external dependency is a Google Font.
