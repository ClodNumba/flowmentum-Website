# FLOWmentum™ website

Marketing site for FLOWmentum™ (Claudia Masüger), deployed on Vercel and served at
[flowmentum.world](https://flowmentum.world).

## Bilingual (English + German)

The site is available in two languages, each as a self-contained static page that
shares the same design:

| URL    | File         | Language |
| ------ | ------------ | -------- |
| `/`    | `index.html` | English  |
| `/de`  | `de.html`    | German   |

- An **EN · DE toggle** in the top navigation switches between them on every screen.
- The visitor's choice is remembered (`localStorage`), so returning visitors land in
  their preferred language.
- `hreflang` tags tell search engines about both versions, so Google can index and
  serve the right language.
- `/de` is served from `de.html` via Vercel's `cleanUrls` setting (see `vercel.json`).

When you change copy in one language, make the matching change in the other file so the
two stay in sync.

## Structure

- `index.html` — English page (hero, the Block Finder quiz, sections, FAQ, contact).
- `de.html` — German translation of the same page.
- `assets/` — images (logos and portraits).
- `vercel.json` — enables clean URLs (`/de` → `de.html`).

It's a plain static site — no build step. Vercel serves the files directly.

## Forms

The "Apply" form and the Block Finder both submit to Formspree
(`https://formspree.io/f/xjgqegrd`). No backend or API keys live in this repo.
