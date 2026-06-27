# Purpose

- Scratch space for OCR output, extracted PDFs, cloned public research, mirrored challenge apps, generated payloads, and temporary experiments.

# Ownership

- This folder owns temporary and derived material only.
- Durable, sanitized lessons should move to `../docs/` or `../oswe-html-library-claude-v5/`.

# Local Contracts

- Treat content here as untrusted and potentially private.
- Do not publish or push from this subtree unless the user explicitly asks and the content is sanitized.
- Nested Git repositories are external/mirrored material; do not rewrite their history or clean them unless asked.
- `__pycache__/`, rendered images, and OCR intermediates are disposable.

# Work Guidance

- Prefer writing generated OCR/extract/research outputs here.
- Keep generated filenames descriptive enough to trace source/module.
- When promoting a pattern to v5, sanitize and generalize it first.

# Verification

- No global verifier.
- Run project-specific checks inside nested repos only when working on that repo.

# Child DOX Index

- `notion_ocr/` - local OCR outputs and downloaded Notion images.
- `oswe_pdf_extract/`, `oswe_pdf_review/`, `exam_pdf_extract/` - PDF text/image extraction outputs.
- `htb_senior_web/` - extracted HTB reference text/rendered pages.
- `github_tudo/`, `research/tudo/` - mirrored target app/source research.
- `BlindBrute/`, `research/WhiteboxPentest/`, `oswe-public-research/` - external public research/tools.
