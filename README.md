# Gianclaudio Carella

Personal site, selected work, and writing. Live URL (after the GitHub Pages source is switched and this branch is merged): [https://gianclaudiocarella.github.io](https://gianclaudiocarella.github.io).

The site is a static Astro 7 project based on [Astro Keel](https://github.com/kpab/astro-keel) (MIT), pinned at revision `0c901a19ade116f6d0a8b6d3b48ec83b060334bb`. See `LICENSE` for the theme licence and for the copyright on original content.

## Run locally

Requires Node.js 22 or newer (see `.nvmrc`).

```bash
npm install
npm run dev
```

Then open http://localhost:4321.

```bash
npm run check          # type-check
npm run build          # production build, including the Pagefind search index
npm run preview        # serve the build
npm run format:check   # Prettier
```

## Add a post or a project

- Blog posts: Markdown or MDX in `src/content/blog/`.
- Projects: Markdown or MDX in `src/content/works/`.

Frontmatter fields and draft behaviour are documented in [docs/writing.md](docs/writing.md). Site name, description, navigation, and social links live in `src/consts.ts`. The about page is `src/pages/about/index.astro`.

Articles can be in English or Portuguese; the surrounding site is in English.

## Deploy

GitHub Actions builds every pull request and every push to `master` (`CI` workflow).

The `Deploy to GitHub Pages` workflow runs only on a push or merge to `master`, or when started manually with `workflow_dispatch`. Pull requests do not deploy.

This repository currently uses the legacy GitHub Pages source (`master` branch root, Jekyll). Before the first Astro deploy can go live, change the repository Pages source to **GitHub Actions** in the repository settings. Do that only when you are ready to publish this site. Until then, the current live page is unchanged.

After that switch, merging this work into `master` publishes `https://gianclaudiocarella.github.io`.
