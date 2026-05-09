# OSWE HTML Library POC

Static HTML proof of concept for embedding an OSWE script-library interface in Notion.

## What This Contains

- `site/index.html`: sanitized HTML preview with generic skeleton snippets.
- `.github/workflows/deploy-pages.yml`: GitHub Actions workflow for GitHub Pages.
- No course-specific scripts, targets, credentials, tokens, or proprietary content.

## Publish Flow

1. Create a GitHub repository.
2. Push this folder to the repo as the root.
3. In GitHub, enable Pages with **GitHub Actions** as the source.
4. Run the `Deploy GitHub Pages` workflow.
5. Copy the resulting Pages URL.
6. In Notion, create an `/embed` block with that URL.

## Privacy Note

If the Pages URL is reachable by Notion, it is reachable by anyone with the URL unless access control is added in front of it.

For real OSWE/HTB-derived skeletons, decide first whether the deployed HTML may contain full code or only navigation. A safer production split is:

- Notion private pages: real code blocks.
- GitHub Pages HTML: navigation, matrix, playbooks, and sanitized/generic snippets.

## Local Preview

From this directory:

```bash
python3 -m http.server 8765 --directory site
```

Then open:

```text
http://127.0.0.1:8765/
```
