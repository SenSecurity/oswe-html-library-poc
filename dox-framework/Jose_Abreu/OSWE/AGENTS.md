# Purpose

- OSWE module/challenge scripts, routes, payloads, and local proof-of-concept code.

# Ownership

- This folder owns private target-specific work products.
- Public reusable patterns must be generalized into `../../oswe-html-library-claude-v5/`.

# Local Contracts

- Challenge directories may contain real lab details; do not publish.
- Keep route lists, payloads, and scripts tied to their challenge folder.
- Do not overwrite user scripts without reading them first.

# Work Guidance

- Prefer small, direct exploit scripts for local challenge work.
- When extracting a reusable primitive, remove target details and add clear `EDIT` knobs before touching v5.

# Verification

- No shared verifier.
- Use syntax checks for edited Python when practical:

```powershell
python -m py_compile <script.py>
```

# Child DOX Index

- `3-Challenge/` - SQLi/time-based challenge experiments.
- `5-Challenge/` - challenge scripts, SMTP sink, SQL query notes.
- `6-Challenge/` - challenge scripts and Java token helper.
- `7-Challenge/` - challenge scripts.
- `8-Challenge/` - challenge script and command notes.
- `9-Challenge/` - challenge scripts and HTML payloads.
- `10-Challenge/` - challenge scripts.
- `11-Challenge/` - bypass script.
- `12-Challenege/` - module 12 exploit and route notes.
