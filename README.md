# Engaz Website

Official static website for Engaz Business Solutions.

## Production

The production website is published with GitHub Pages from the repository root
on the `main` branch. The site is intentionally static and contains no runtime
credentials, customer data, database access, or deployment secrets.

## Scope

This repository contains the marketing website only. Interactive demos are
maintained separately and are intentionally excluded from production here.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole site: markup, styles, and behaviour in one file. |
| `404.html` | Styled not-found page served by GitHub Pages. |
| `robots.txt` | Crawler policy and sitemap pointer. |
| `sitemap.xml` | Single-page sitemap with `ar` / `en` alternates. |
| `site.webmanifest` | Install metadata, theme colours. |
| `social-preview.png` | Open Graph and Twitter card image. |
| `brand/` | Official Engaz brand assets (see below). |
| `CNAME` | Custom domain for GitHub Pages. |

## Brand assets

`brand/` holds the official Engaz identity, copied verbatim from the company
brand kit (`03-brand/brand-kit` on the shared Drive). The SVGs are
byte-for-byte the approved files; the PNG icons are rendered from
`favicon.svg`.

| File | Use |
| --- | --- |
| `engaz-logo-horizontal.svg` | Full lockup, navy wordmark — light backgrounds (site header). |
| `engaz-logo-horizontal-dark.svg` | Full lockup, white wordmark and bare check — dark backgrounds (site footer). |
| `engaz-badge.svg` | Navy badge with the check, on its own. |
| `engaz-mark-check.svg` | The check with no badge, for dark grounds. |
| `favicon.svg` | Browser tab icon. |
| `apple-touch-icon-180.png`, `engaz-icon-192.png`, `engaz-icon-512.png` | Home-screen and manifest icons. |

Brand colours: Primary Navy `#122247` · Accent Gold `#E8A020` ·
Deep Navy `#0C1637` · Slate `#5A6785` · White `#FFFFFF`.

The logo must not be recoloured, rotated, stretched, or have its name reset in
another typeface, and it must never render narrower than 140px. Keep clear
space around it equal to the badge height. Use the badge on light backgrounds
and the bare check on dark ones.

The page is Arabic-first (`dir="rtl"`) with a full English translation held in
`data-ar` / `data-en` attribute pairs and switched client-side. English is also
reachable directly at `?lang=en`, which is what the `hreflang` alternates point
at. Any new copy needs both attributes, or the language switch will leave that
string untranslated.

The calculator and readiness index run entirely in the browser. They send
nothing anywhere; the only outbound action on the page is a WhatsApp link the
visitor chooses to open.

## Safe update flow

1. Create a branch.
2. Review and test the website locally.
3. Open a pull request.
4. Merge only after the checks pass.

Do not commit environment files, credentials, exports, logs, or customer data.
Engaz Business Solutions official website
