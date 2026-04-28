# CLAUDE.md

Quick orientation for Claude sessions working on this site.

## Project

Personal academic website for Thien (Theo) Pham, PhD candidate in Biostatistics
at the University of Pittsburgh. Jekyll site built on Minimal Mistakes (academic
fork). Deploys via GitHub Pages from `master` to `quythien/personal`.

## Build

- `bundle exec jekyll serve` for local dev
- GitHub Pages rebuilds automatically on push to `master`

## Palette role system

Each color has a single, learnable job. Don't introduce new colors — activate
existing tokens. Defined in `assets/css/typography.css`.

| Token | Hex | Single job |
|---|---|---|
| `--accent` (forest) | `#2d5d4f` | Primary interactive: links, current-year news date, h2 hairlines, default `.venue` |
| `--accent-soft` (sage) | `#4a7d6f` | Hover state, prior-year news date |
| `--accent-deep` | `#1f4338` | Button hover bg |
| `--navy` | `#2e4858` | Methods / quantitative category. Theme 01 rail+kicker, methods venue, CTA-button-alt bg |
| `--clay` | `#9d5a35` | Applied / clinical category. Theme 02 rail+kicker, clinical venue |
| `--gold` | `#a8924a` | Award marker only. Funding-note left border, `li.news-award` gold pip. **Never used for text.** |
| `--ink` | `#1f1d1a` | Body text |
| `--ink-soft` | `#4a463f` | Secondary text, ≤2024 news dates |
| `--paper` (bone) | `#f6f3ec` | Pub-figure left panel, supporting surface |
| `--rule` | `#a8a294` | Borders, hairlines |

### Surfaces

- **Page background** `#eff1e7` (sage-tinted bone). Set via `--global-bg-color`
  override. Body has a faint SVG paper-grain texture, disabled below 600px.
- **Masthead** `#d8cdb0` (kraft). `.greedy-nav` and `.masthead__menu-item` are
  set to `background: transparent` so the kraft shows through (those elements
  have hardcoded `background: var(--global-bg-color)` in the theme SCSS).
- **Funding-note** `#ece4cd` (parchment), gold left border. Class:
  `.funding-note`. Used for in-prose highlighted asides.
- **CTA-collab card** parchment-to-kraft gradient
  `linear-gradient(135deg, #ece4cd 0%, #d6c8a4 100%)`. Joins the warm callout
  family with the masthead and funding-note.
- **Theme cards / pub cards** `#fff`. Discrete research artifact surface.

### Mental model the reader picks up

- Cool sage = main reading
- White = discrete artifact (publication, theme)
- Warm tones (kraft, parchment) = chrome / aside
- Forest = "you can click this"
- Navy / clay / gold = category signals, never decoration

## File ownership

- `_config.yml` — site config. **`scripts/` is in `exclude:`** because
  `scripts/cv.md` declares `permalink: /cv/` and would shadow `_pages/cv.md`.
- `_pages/cv.md` — the live CV page (PDF embed). Don't touch `scripts/cv.md`;
  it's the markdown source for the CV→JSON pipeline only.
- `_data/navigation.yml` — top nav. Five items max — see gotcha below.
- `assets/css/typography.css` — sitewide tokens, h2 hairlines, masthead
  overrides, paper-grain texture, smooth scroll. Loaded after `main.css`.
- `assets/css/home.css` — homepage-only styles (themes-grid, featured-pubs,
  news-list, cta cards). Loaded via the `custom_css` frontmatter mechanism
  in `_pages/about.md`.
- `assets/css/talks.css`, `cv.css`, `teaching.css`, `collapse.css` — per-page
  CSS, also loaded via `custom_css`.

## Visual conventions worth preserving

- **STATGEN** is uppercase sitewide (matches the conference's official rendering).
- **Section h2s** get a 56×2px forest hairline as `::after`, not a full-width
  border-bottom. Editorial section-marker treatment.
- **Theme kickers** ("Theme 01" / "02" / "03") match their rail color
  (navy / clay / forest). Don't fade with opacity.
- **News-list dates** are colored by year via `data-year` attribute. Award
  entries get a 6×6px gold pip via `li.news-award`.
- **Pub-figure venues** are colored by category via `.venue.venue-method` and
  `.venue.venue-clinical` modifier classes. Default (no modifier) = forest.
- **Anchor links** (e.g., `Research` nav → `/#research-themes`) rely on
  `html { scroll-behavior: smooth }` + `scroll-margin-top: 90px` on `h1–h6` to
  clear the 70px fixed masthead.

## Gotchas

- **Don't add a 6th nav item.** Five items fit; six pushes past `greedy-nav.js`'s
  overflow threshold and collapses the last item into a hidden dropdown. Rename
  existing items or accept the collapse.
- **Don't change `--global-bg-color`** without also retesting the masthead — it
  reads the same token, which is why we override `.masthead` background
  separately.
- **Don't reintroduce hardcoded border colors** like `#bccdc4` or `#d9d4c8`.
  Use `var(--rule)` so a future palette tune is one-line.
- **Don't restore long-form CV to `_pages/`.** `/cv/` should remain a PDF embed.

## Commit style

- Match recent commits: short subject (≤72 char), wrapped body explaining the
  *why* (not the *what*).
- **No `Co-Authored-By: Claude` trailers** — the user explicitly opts out.
- Don't push to remote without explicit confirmation in the conversation.
