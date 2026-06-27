# OSWE Project Knowledge

## Default Style

- Use terse Portuguese by default.
- Work locally first. Do not push GitHub Pages unless Bruno explicitly asks.
- Main HTML app is `oswe-html-library-claude-v5/site/index.html`.
- v5 is the OSWE Functions library: copy base first, then copy standalone functions above `main()` and call them manually inside `main()`.
- v4 is the legacy Exploit.py Builder: script-builder-first, ordered steps, copyable final `exploit.py`.
- Legacy/reference HTML apps are `oswe-html-library-claude-v2/site/index.html` and `oswe-html-library-claude-v3/site/index.html`.
- Local preview normally runs at `http://127.0.0.1:8765/`.

## Notion Notes -> HTML Workflow

When improving the OSWE HTML library from Bruno's Notion notes, assume screenshots/images contain important payloads, Burp requests, source-code snippets, outputs, and small exploit details.

Use this flow before changing HTML:

1. Prefer a Notion export of the target module/page as HTML or Markdown with images included.
2. If export is not available, use the Notion connector to fetch text and image URLs, then download images immediately because Notion file URLs expire.
3. Run local OCR with `tools/notion_ocr_extract.py`.
4. Review OCR output under `tmp/notion_ocr/`.
5. Compare OCR with local PDFs/text extracts and visible Notion text.
6. Only then update sanitized public HTML snippets.

Anti-palheiro rule for v5: consolidate, do not accumulate. If a generated snippet fits an existing family, improve the canonical function instead of creating a near-duplicate variant. Create a new function only for a genuinely new script-building primitive. Do not show `tested:false` in v5; Bruno removed that visual noise.

Reference doc: `docs/notion-ocr-pipeline.md`.

OCR command pattern:

```powershell
python tools/notion_ocr_extract.py --input "<notion-export-or-folder>" --module "<module-name>" --out tmp/notion_ocr/<module-name>-ocr.md
```

Tesseract expected path on this machine:

```text
C:\Program Files\Tesseract-OCR\tesseract.exe
```

Required Python packages:

```text
pillow pytesseract beautifulsoup4 requests
```

## HTML Snippet Rules

- Public HTML must stay sanitized: no real targets, tokens, flags, private course text, credentials, or live exam data.
- Convert course/lab findings into agnostic exploit primitives.
- Prefer copy-ready snippets with clear `EDIT` knobs.
- Keep code compact enough to read during exam.
- Add enough comments to explain when to use the snippet and what must be changed.
- Do not create Notion pages for scripts; Notion is only the embed/container.

## Current OSWE Library Direction

The library should help rebuild an exploit from manual work done in Burp/source review/sqlmap/etc. The product is not a vulnerability decision tree. It is a fast builder for the final `exploit.py` after Bruno already knows the path.

Useful entry shape:

- base/session setup
- request primitive
- extraction/oracle
- authentication/privilege step
- RCE trigger
- proof/report helper

For v4, multiple ordered steps are normal. Example:

```python
def main():
    login_low_priv()
    leak_reset_token()
    reset_admin_password()
    login_admin()
    upload_webshell()
    proof()
```

For SQLi and similar techniques, prefer agnostic roots:

- one generic technique
- DBMS/engine-specific knobs inside the snippet
- clear query/action menu such as `CURRENT_DB`, `LIST_TABLES`, `DUMP_TABLE`, `FILE_CONTENT`, `RESET_TOKEN`

# DOX framework

- DOX is highly performant AGENTS.md hierarchy installed here
- Agent must follow DOX instructions across any edits

## Core Contract

- AGENTS.md files are binding work contracts for their subtrees
- Work products, source materials, instructions, records, assets, and durable docs must stay understandable from the nearest applicable AGENTS.md plus every parent AGENTS.md above it

## Read Before Editing

1. Read the root AGENTS.md
2. Identify every file or folder you expect to touch
3. Walk from the repository root to each target path
4. Read every AGENTS.md found along each route
5. If a parent AGENTS.md lists a child AGENTS.md whose scope contains the path, read that child and continue from there
6. Use the nearest AGENTS.md as the local contract and parent docs for repo-wide rules
7. If docs conflict, the closer doc controls local work details, but no child doc may weaken DOX

Do not rely on memory. Re-read the applicable DOX chain in the current session before editing.

## Update After Editing

Every meaningful change requires a DOX pass before the task is done.

Update the closest owning AGENTS.md when a change affects:

- purpose, scope, ownership, or responsibilities
- durable structure, contracts, workflows, or operating rules
- required inputs, outputs, permissions, constraints, side effects, or artifacts
- user preferences about behavior, communication, process, organization, or quality
- AGENTS.md creation, deletion, move, rename, or index contents

Update parent docs when parent-level structure, ownership, workflow, or child index changes. Update child docs when parent changes alter local rules. Remove stale or contradictory text immediately. Small edits that do not change behavior or contracts may leave docs unchanged, but the DOX pass still must happen.

## Hierarchy

- Root AGENTS.md is the DOX rail: project-wide instructions, global preferences, durable workflow rules, and the top-level Child DOX Index
- Child AGENTS.md files own domain-specific instructions and their own Child DOX Index
- Each parent explains what its direct children cover and what stays owned by the parent
- The closer a doc is to the work, the more specific and practical it must be

## Child Doc Shape

- Create a child AGENTS.md when a folder becomes a durable boundary with its own purpose, rules, responsibilities, workflow, materials, or quality standards
- Work Guidance must reflect the current standards of the project or user instructions; if there are no specific standards or instructions yet, leave it empty
- Verification must reflect an existing check; if no verification framework exists yet, leave it empty and update it when one exists

Default section order:
- Purpose
- Ownership
- Local Contracts
- Work Guidance
- Verification
- Child DOX Index

## Style

- Keep docs concise, current, and operational
- Document stable contracts, not diary entries
- Put broad rules in parent docs and concrete details in child docs
- Prefer direct bullets with explicit names
- Do not duplicate rules across many files unless each scope needs a local version
- Delete stale notes instead of explaining history
- Trim obvious statements, repeated rules, misplaced detail, and warnings for risks that no longer exist

## Closeout

1. Re-check changed paths against the DOX chain
2. Update nearest owning docs and any affected parents or children
3. Refresh every affected Child DOX Index
4. Remove stale or contradictory text
5. Run existing verification when relevant
6. Report any docs intentionally left unchanged and why

## User Preferences

- Use terse Portuguese by default.
- Work locally first; push GitHub Pages only when Bruno explicitly asks.

## Child DOX Index

- `docs/AGENTS.md` - durable planning, handoff, coverage, and OCR workflow documentation.
- `tools/AGENTS.md` - local helper scripts and payload/OCR tooling.
- `oswe-html-library-claude-v5/AGENTS.md` - primary OSWE Functions static HTML library.
- `oswe-html-library-poc/AGENTS.md` - GitHub Pages publish repository for the public sanitized embed.
- `oswe-html-library-claude-v4/AGENTS.md` - legacy Exploit.py Builder workbench.
- `oswe-html-library-claude-v3/AGENTS.md` - archived/reference static HTML library with verifier.
- `oswe-html-library-claude-v2/AGENTS.md` - archived/reference static HTML library.
- `oswe-html-library-claude/AGENTS.md` - archived Claude-edition UI/reference app.
- `Jose_Abreu/AGENTS.md` - private challenge scripts and lab artifacts.
- `OSWE-Skill/AGENTS.md` - OSWE source materials, Notion scope, and skill/reference bundle.
- `tmp/AGENTS.md` - scratch, extracted, mirrored, and generated research material.
- `.claude/` - local agent settings; root-owned, do not edit unless explicitly requested.
