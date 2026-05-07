# sniffrpack-com

Marketing site for [sniffrpack.com](https://sniffrpack.com) &mdash; the public face of Sniffr, software for dog-care businesses.

A [Papyrus Labs AI](https://papyruslabs.ai) product.

## Stack

- **Astro 5** &mdash; static site generator, content-first, ships zero JS by default
- **Tailwind 4** &mdash; via the `@tailwindcss/vite` plugin
- **Cloudflare Pages** &mdash; deploy target

## Local development

```sh
npm install
npm run dev      # localhost:4321
npm run build    # ./dist
npm run preview  # serve ./dist locally
```

## Deploy

This repo is wired to Cloudflare Pages. To set up:

1. In Cloudflare dashboard &rarr; Pages &rarr; Create a project &rarr; Connect to Git
2. Select `papyruslabs-ai/sniffrpack-com`
3. Build command: `npm run build`
4. Build output directory: `dist`
5. Node version: `20` (or latest LTS)
6. Add custom domain: `sniffrpack.com`

`public/_headers` provides default cache &amp; security headers.

## Structure

```
src/
  layouts/
    Layout.astro      # shared head + nav + footer
  components/
    Nav.astro
    Footer.astro
  pages/
    index.astro       # the splash page (10 screens)
    roadmap.astro     # /roadmap &mdash; the 2026 build plan
  styles/
    global.css        # Tailwind import + theme tokens
public/
  favicon.svg
  _headers            # Cloudflare Pages headers config
```

## Editing copy

Most copy lives directly in `src/pages/index.astro` and `src/pages/roadmap.astro`. The screens on the homepage are clearly delimited with HTML comments (`<!-- Hero -->`, `<!-- Thesis -->`, etc.) so an editor can find the right block without reading the whole file.

## Theme tokens

Colors and typography are defined as CSS custom properties in `src/styles/global.css` under `@theme`. Adjust there to retheme.

| Token | Default | Use |
| --- | --- | --- |
| `--color-bg` | `#FAF8F4` | Page background (warm off-white) |
| `--color-ink` | `#1A1814` | Primary text |
| `--color-muted` | `#5A554E` | Secondary text |
| `--color-rule` | `#E5DED1` | Borders, rules |
| `--color-accent` | `#B8501E` | Accent (warm rust) |

Fonts: **Fraunces** (display, serif) and **Inter** (body, sans). Loaded from Google Fonts.
