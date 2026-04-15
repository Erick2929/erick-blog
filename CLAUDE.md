# CLAUDE.md — erick-blog

## Language rule
**Everything must be in English** — all blog content, UI strings, code comments, commit messages, and any text written by Claude.

## Stack
- **Astro** v6 — static site generator
- **@astrojs/rss** — RSS feed
- **Shiki** (via Astro) — syntax highlighting, theme `github-dark`
- **JetBrains Mono** — monospace font via Google Fonts

## Dev commands
```bash
npm run dev      # localhost:4321
npm run build    # static build → dist/
npm run preview  # preview build
```

## Writing a post
1. Create `src/content/blog/YYYY-MM-DD-slug.md`
2. Add frontmatter:
   ```yaml
   ---
   title: "Post title"
   date: YYYY-MM-DD
   description: "One-line summary"  # optional
   tags: ["tag1", "tag2"]           # optional
   ---
   ```
3. Write content in Markdown below the frontmatter
4. `git push` → Vercel auto-deploys in ~30s

## Deployment
- Hosted on Vercel, target domain: `blog.erick.com`
- Every push to `main` triggers a deploy
