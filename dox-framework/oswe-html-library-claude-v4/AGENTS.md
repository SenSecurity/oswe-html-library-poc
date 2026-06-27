# Purpose

- Legacy OSWE Exploit.py Builder.
- Builds ordered chains and copyable final `exploit.py` scripts.

# Ownership

- This folder owns v4 app behavior and verifier.
- v5 is the primary active library; v4 is maintained only when explicitly requested or when legacy builder behavior matters.

# Local Contracts

- Main app: `site/index.html`.
- Keep public snippets sanitized.
- In v4, ordered multi-step chains are normal.
- Keep generated/new pieces marked `tested:false` until Bruno validates them in a lab.

# Work Guidance

- Do not migrate v5 function-library assumptions into v4 unless requested.
- Keep search and "show all" behavior as escape hatches.
- Consolidate canonical pieces rather than adding near duplicates.

# Verification

```powershell
node oswe-html-library-claude-v4\tools\verify-v4.js
```

- Preview:

```powershell
python -m http.server 8765 --bind 127.0.0.1 --directory oswe-html-library-claude-v4\site
```

# Child DOX Index

- `site/` - legacy builder static app.
- `tools/` - v4 verifier.
