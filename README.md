# kevincxie.github.io

Personal academic site for Kevin Xie, built with [Astro](https://astro.build)
and deployed to GitHub Pages via GitHub Actions.

## Editing

- **Add a publication**: append an entry to
  [`src/data/publications.yaml`](src/data/publications.yaml). Set
  `selected: true` to feature it, and drop a teaser image (or short muted
  video loop) under `public/assets/pubs/`.
- **Bio / links**: edit [`src/pages/index.astro`](src/pages/index.astro).
- **Design tokens** (colors, dark mode, spacing):
  [`src/styles/global.css`](src/styles/global.css).

## Developing

```bash
npm install
npm run dev      # local dev server with hot reload
npm run build    # static build into dist/
npm run preview  # serve the built site
```

## Deploying

Pushes to the deploy branch build and publish automatically via
[`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)
(GitHub Pages must be set to "GitHub Actions" under Settings → Pages).
