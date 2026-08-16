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
| `CNAME` | Custom domain for GitHub Pages. |

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
