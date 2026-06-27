# Purpose

- Archived/reference OSWE static HTML library.
- Retained for UI and snippet history.

# Ownership

- Root owns decisions about whether this archive is edited.
- Prefer v5 for new work.

# Local Contracts

- Main app: `site/index.html`.
- Keep public content sanitized if edited.
- Do not port changes here unless the user explicitly asks for v3/reference updates.

# Work Guidance

- Treat screenshots as reference artifacts, not generated truth.

# Verification

```powershell
node oswe-html-library-claude-v3\tools\verify-v3.js
```

# Child DOX Index

- `site/` - archived static app.
- `tools/` - v3 verifier.
