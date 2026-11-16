# DESIGN.md — NAPS Supplier Training (Invoice key-in & Fast Lane)

Direction: **"Clean industrial manual"** — feels like a well-made operations handbook,
not a marketing site. Calm, precise, easy for suppliers to follow step by step.
Light theme only (suppliers watch on office PCs and phones; one theme keeps it simple).

Note: chosen from the project context and general rules, not from compared real
sites (UXKIN not connected).

## Color

| Token | Value | Role |
|---|---|---|
| `--paper` | `#F6F5F1` | Page background (warm off-white, less glare than pure white) |
| `--surface` | `#FFFFFF` | Player panel, chapter rows on hover |
| `--ink` | `#16181D` | Headings and body text (16.9:1 on paper) |
| `--ink-2` | `#4A4F59` | Secondary text, descriptions (7.6:1 on paper) |
| `--ink-3` | `#6B717C` | Meta text: file size, duration (4.7:1 on paper) |
| `--line` | `#DEDBD3` | Borders, dividers |
| `--line-strong` | `#16181D` | Rule under section labels, the step rail |
| `--primary` | `#C8102E` | Primary buttons, active chapter, links (5.6:1 on paper) |
| `--primary-hover` | `#A50D26` | Hover / pressed |
| `--primary-tint` | `#FBEAEC` | Active chapter background |
| `--accent` | `#E8A317` | Only for the "choose one" fork marker in the flow |
| `--success` | `#1F7A4D` | "Watched" check |
| `--focus` | `#1D4ED8` | Focus ring (2px solid + 2px offset), distinct from primary |

One primary, one accent. No gradients, no glass.

## Typography

- Body & headings: **IBM Plex Sans Thai** (Google Fonts) — Thai + Latin in one family, technical feel.
- Labels, step numbers, file meta: **IBM Plex Mono**.
- Weights: 400, 500, 700.

| Token | Size / line-height | Use |
|---|---|---|
| `--fs-display` | clamp(2.25rem, 5vw, 3.5rem) / 1.15 | h1 |
| `--fs-h2` | clamp(1.5rem, 3vw, 2rem) / 1.25 | Section titles |
| `--fs-h3` | 1.25rem / 1.4 | Chapter titles |
| `--fs-body-lg` | 1.125rem / 1.7 | Hero support line |
| `--fs-body` | 1rem / 1.7 | Body (Thai needs taller line-height) |
| `--fs-small` | 0.875rem / 1.5 | Meta |
| `--fs-label` | 0.75rem / 1.4, mono, uppercase, +0.08em | Section labels ("STEP 01") |

Max text width 65ch.

## Spacing

8-based: `--s-1` 4px · `--s-2` 8px · `--s-3` 12px · `--s-4` 16px · `--s-5` 24px ·
`--s-6` 32px · `--s-7` 48px · `--s-8` 64px · `--s-9` 96px.
Section spacing: `--s-9` desktop, `--s-8` phone. Content width 1160px, side padding 24px (16px phone).

## Shape & depth

- Radius: `--r-1` 4px (buttons, tags) · `--r-2` 10px (player, panels). Nothing pill-shaped except status dots.
- Shadow: one only, `--shadow-1: 0 1px 2px rgb(22 24 29 / .06), 0 8px 24px rgb(22 24 29 / .06)` on the player.
- Structure comes from rules and borders, not from cards floating everywhere.

## Components

- **Button primary**: primary bg, white text, 44px min height, r-1. Hover → primary-hover. Focus → focus ring. Disabled → 40% opacity, no pointer.
- **Button secondary**: transparent, ink border 1px, ink text. Hover → surface bg.
- **Quiet link**: primary text, underline on hover/focus.
- **Chapter row**: mono step number (large), title, one-line description, meta (size · duration), play affordance. Active → primary-tint bg + 3px primary left bar. Watched → success check.
- **Flow rail**: vertical line (line-strong) connecting steps; the fork (method A / method B) marked with the accent.
- **Nav**: simple top bar — title left, "ติดต่อสอบถาม" link right. No hamburger needed.
- **Footer**: contact, owner department, last updated.

## Imagery & icons

- Icons: inline SVG, 1.5px stroke, 20px (play, check, download, external). No emoji.
- Visuals are the real product: video thumbnails / NAPS screenshots supplied by the owner. No stock photos, no abstract blobs.
- No company logo drawn by us; the owner may add the official file.
