# Purpose

- Durable project documentation: plans, handoffs, coverage notes, brainstorms, and OCR workflow records.
- `docs/notion-ocr-pipeline.md` owns the Notion export/OCR process referenced by root rules.

# Ownership

- Root owns broad project direction.
- This folder owns durable docs only; do not store throwaway extracts or generated OCR blobs here.

# Local Contracts

- Keep docs concise, current, and operational.
- Do not include live targets, credentials, flags, private tokens, or proprietary course text.
- Prefer dated filenames for plans, handoffs, and one-off decision records.

# Work Guidance

- Move stable lessons from `tmp/` into `docs/` only after sanitizing.
- Put implementation details near the code if they are only useful while editing that code.

# Verification

- No automated doc verifier currently exists.
- For Markdown-only edits, review rendered structure manually when practical.

# Child DOX Index

- `brainstorms/` - dated exploration notes.
- `coverage/` - library coverage and gap analysis.
- `handoffs/` - transfer notes for future work.
- `plans/` - implementation and product plans.
