# Purpose

- Local helper tooling used by the OSWE project.
- Current tools include Notion OCR extraction and local deserialization payload generation.

# Ownership

- Root owns workflow rules.
- This folder owns reusable helper scripts and their companion docs.

# Local Contracts

- Keep helpers local-first and explicit about inputs/outputs.
- Do not bake real targets, credentials, tokens, flags, or private course text into tool defaults.
- Generated outputs should go under `tmp/` unless the user names another destination.

# Work Guidance

- Prefer Python standard library plus already documented dependencies.
- Keep CLI flags discoverable with `--help`.
- For OCR work, follow root Notion Notes -> HTML workflow.

# Verification

- Python syntax check for edited scripts:

```powershell
python -m py_compile tools\notion_ocr_extract.py tools\deser_payload_builder.py
```

- For `notion_ocr_extract.py`, use the sample/test source when changing OCR parsing.

# Child DOX Index

- No child AGENTS.md files.
