# Purpose

- Primary OSWE Functions static HTML library.
- Users copy the base first, paste standalone functions above `main()`, and call them manually inside `main()`.

# Ownership

- This folder owns v5 source and generated app output.
- Root owns public sanitization and OSWE library direction.

# Local Contracts

- Canonical app file: `site/index.html`.
- Canonical source generator: `tools/build-v5.js`.
- Do not hand-edit `site/index.html` for durable changes; edit `tools/build-v5.js`, then rebuild.
- `tools/build-v5.js` also owns compact local utility modes embedded in the static app, currently including the `Regex helper`.
- Public output must stay sanitized: no real targets, credentials, tokens, flags, OSIDs, or proprietary course text.
- Anti-palheiro rule: improve the canonical function family instead of adding near-duplicate snippets.
- Do not show `tested:false` in v5.

# Work Guidance

- Entries should be generic exploit primitives with clear `EDIT` knobs.
- Prefer compact copy-ready functions using the base contract: `def something(session, cfg):`.
- Use English inside code entries and metadata.
- Keep comments practical and short.
- Keep the primary UI focused on snippets left and active code right.
- Supplemental tools such as `Regex helper` must stay compact, local-only, and exam-practical; no recipes/copy kits/hero/marketing sections.

# Verification

```powershell
node oswe-html-library-claude-v5\tools\build-v5.js
node oswe-html-library-claude-v5\tools\verify-v5.js
```

- Preview normally at `http://127.0.0.1:8765/` with:

```powershell
python -m http.server 8765 --bind 127.0.0.1 --directory oswe-html-library-claude-v5\site
```

# Child DOX Index

- `site/` - generated static app output; rebuild from `tools/build-v5.js`.
- `tools/` - builder and verifier for v5.
