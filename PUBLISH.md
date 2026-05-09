# Publish Checklist

## Current Blocker

The local `gh` CLI is not authenticated, and the GitHub connector currently lists no accessible repositories.

To let Codex push this automatically, one of these must be true:

- `gh auth login` has been completed locally, or
- the GitHub app connector has access to the target repository, or
- you provide an existing `owner/repo` where the connector can create files.

## Target Repo Shape

Recommended repo name:

```text
oswe-html-library
```

Recommended visibility for this POC:

```text
private repo, public/sanitized Pages output
```

## Notion Embed

After deployment, use Notion manually:

```text
/embed
<GitHub Pages URL>
```

The POC proved that plain links are not enough for the desired render. The Notion block should be a real embed block.
