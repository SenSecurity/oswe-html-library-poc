# Purpose

- GitHub Pages publish repository for the sanitized OSWE HTML library embed.
- Public Pages URL: `https://sensecurity.github.io/oswe-html-library-poc/`.

# Ownership

- This nested Git repository owns deployable public output.
- Source-of-truth edits normally happen in `../oswe-html-library-claude-v5/`.

# Local Contracts

- Repository: `https://github.com/SenSecurity/oswe-html-library-poc`.
- This repo is public; keep all content sanitized.
- Do not push unless Bruno explicitly asks.
- Current published surface is the user-approved v5 vision generated at `../tmp/v5-design-vision/index.html` from canonical v5 entries; copy that artifact into `site/index.html` until the vision is promoted into the canonical generator.
- Preserve `.github/workflows/deploy-pages.yml` and `.nojekyll`.

# Work Guidance

- Before commit/push, confirm `git status -sb` and inspect the diff.
- Stage only intended publish files.
- Never publish local lab IPs, cookies, tokens, credentials, flags, OSIDs, or proprietary course text.

# Verification

- Verify source before copying:

```powershell
node ..\oswe-html-library-claude-v5\tools\build-v5.js
node ..\oswe-html-library-claude-v5\tools\verify-v5.js
```

- Optional local preview from this folder:

```powershell
python -m http.server 8765 --bind 127.0.0.1 --directory site
```

# Child DOX Index

- `.github/workflows/` - GitHub Pages deploy workflow.
- `dox-framework/` - mirrored OSWE DOX `AGENTS.md` hierarchy for portable agent instructions.
- `site/` - published static app.
