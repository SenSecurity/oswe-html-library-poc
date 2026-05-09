# Publish Checklist

## Published POC

- Repository: `https://github.com/SenSecurity/oswe-html-library-poc`
- GitHub Pages URL: `https://sensecurity.github.io/oswe-html-library-poc/`
- Notion POC page: `https://www.notion.so/35bd56f648e28187be88e4833d9bc40c`

## Target Repo Shape

Recommended repo name:

```text
oswe-html-library
```

Visibility used for this POC:

```text
public repo, public/sanitized Pages output
```

GitHub rejected Pages for the private POC repository under the current account plan, so the POC repo was made public. Keep this repo sanitized.

## Notion Embed

After deployment, use Notion manually:

```text
/embed
<GitHub Pages URL>
```

The POC proved that plain links are not enough for the desired render. The Notion block should be a real embed block.

Browser automation could not create the `/embed` block because the automated browser was not logged into Notion. The Notion MCP connector can update page text, but did not expose a reliable create-embed-block operation in this session.
