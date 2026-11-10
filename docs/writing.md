# Writing on this site

The public site chrome (navigation, titles, and the about page) is in English. Individual articles may be written in English or Portuguese — use whichever language fits the piece. You do not need a separate language switch for now; the post’s own title and body carry the language.

## Add a blog post

1. Create a Markdown (`.md`) or MDX (`.mdx`) file in `src/content/blog/`.
2. Use a URL-friendly file name, for example `doorman-fallacy.md`. That name becomes the slug: `/blog/doorman-fallacy/`.
3. Start the file with frontmatter:

```md
---
title: Your title
description: A short summary for listings and social previews.
publishDate: 2026-11-10
tags:
  - software
draft: false
---

Your article starts here.
```

Optional fields: `heroImage` (an image imported from a path next to the post or under `src/`), and `draft`.

## Add a project

Create a Markdown or MDX file in `src/content/works/`. Frontmatter:

```md
---
title: Project name
description: One or two sentences.
tech:
  - TypeScript
  - Next.js
publishDate: 2026-01-15
order: 1
link: https://example.com
repo: https://github.com/owner/repo
---

The case study body.
```

`link` and `repo` are optional. `order` is optional; lower numbers appear first when dates are equal.

## Drafts

Set `draft: true` on a blog post to keep it out of the public build. Draft posts are omitted from the blog index, post pages, RSS feed, tag pages, search index (they are not built), and generated Open Graph images. This is implemented in the theme and was verified with a local production build.

Files whose names start with `_` are ignored by the content collections entirely, so they also stay out of the site.

Works do not have a `draft` field. To hold back a project, leave the file out of `src/content/works/` until you are ready to publish it.

## Preview locally

```bash
npm install
npm run dev
```

Open http://localhost:4321. Search is only available after `npm run build` and `npm run preview`.
