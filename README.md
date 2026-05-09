# OSWE HTML Library POC

Static HTML proof of concept for embedding the full OSWE script-library interface in Notion.

## What This Contains

- `site/index.html`: full static HTML library with navigation, search, filters, copy kits, scripts, copy buttons, and downloads.
- `.github/workflows/deploy-pages.yml`: GitHub Actions workflow for GitHub Pages.
- No course-specific scripts, targets, credentials, tokens, or proprietary content.

## Publish Flow

Published POC:

- Repository: `https://github.com/SenSecurity/oswe-html-library-poc`
- GitHub Pages: `https://sensecurity.github.io/oswe-html-library-poc/`
- Notion POC: `https://www.notion.so/35bd56f648e28187be88e4833d9bc40c`

To reproduce:

1. Push this folder to a GitHub repository.
2. In GitHub, enable Pages with **GitHub Actions** as the source.
3. Run the `Deploy GitHub Pages` workflow.
4. Copy the resulting Pages URL.
5. In Notion, create an `/embed` block with that URL.

The POC was confirmed working in Notion with a real `/embed` block.

## Privacy Note

This POC repository is public because the current GitHub plan rejected Pages for a private repository. If the Pages URL is reachable by Notion, it is reachable by anyone with the URL unless access control is added in front of it.

Current direction: everything needed for retrieval and copying lives in the HTML. Notion is the embed container.

For real OSWE/HTB-derived skeletons, keep the deployed HTML private or access-controlled if the code should not be public. This POC stays sanitized because GitHub Pages is public under the current account plan.

## Local Preview

From this directory:

```bash
python3 -m http.server 8765 --directory site
```

Then open:

```text
http://127.0.0.1:8765/
```
