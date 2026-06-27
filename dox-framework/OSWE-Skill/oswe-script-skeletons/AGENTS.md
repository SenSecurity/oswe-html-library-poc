# Purpose

- Local skill bundle for maintaining OSWE script skeletons and transforming source material into reusable snippets.

# Ownership

- This folder owns `SKILL.md`, skill agent config, and transformation reference docs.
- Active generated library output is owned by `../../oswe-html-library-claude-v5/`.

# Local Contracts

- Keep `SKILL.md` and `references/` aligned.
- Use relative paths from this folder for skill references.
- Do not add private target data or proprietary course text to skill docs.

# Work Guidance

- Update reference docs when snippet classification, page schema, or transformation rules change durably.
- Keep skill instructions operational and concise.

# Verification

- No automated verifier.
- Manual check: every file referenced by `SKILL.md` exists under `references/` or `agents/`.

# Child DOX Index

- `agents/` - skill agent configs.
- `references/` - transformation, page template, Notion scope, and HTB skeleton references.
