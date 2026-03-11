# космолед.рф — Project Log

## Overview
Science blog about Arctic remote sensing, sea ice forecasting, and ML. Bilingual (ru/en).

## Tech Stack
- **SSG**: Hugo v0.157.0 extended
- **Theme**: hugo-coder (git submodule)
- **Hosting**: Cloudflare Pages (pending DNS setup)
- **Repo**: https://github.com/bolkhovsky/kosmoled.rf
- **Domain**: космолед.рф (punycode: xn--e1afkbacfh5a6i.xn--p1ai)

## Content Structure
```
content/
├── ru/
│   ├── _index.md
│   ├── about.md
│   └── posts/
│       └── 2026-03-11-titds-validation-pipeline.md
└── en/
    ├── _index.md
    ├── about.md
    └── posts/
```

## How to Add a Post
1. Create `content/ru/posts/YYYY-MM-DD-slug.md` with frontmatter
2. Add images to `static/images/<topic>/`
3. `hugo server -D` to preview
4. `git add && git commit && git push` — Cloudflare auto-deploys

## Deploy Setup (Cloudflare Pages)
1. Dashboard → Pages → Create → Connect GitHub → `bolkhovsky/kosmoled.rf`
2. Build: Framework = Hugo, Command = `hugo`, Output = `public`
3. Env var: `HUGO_VERSION` = `0.157.0`
4. Custom domain: космолед.рф → add DNS records

## Version History
- **2026-03-11**: Initial site. First post: TITDS-2025 validation pipeline (ru).
