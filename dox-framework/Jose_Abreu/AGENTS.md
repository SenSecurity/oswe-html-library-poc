# Purpose

- Private lab/challenge workspace for OSWE scripts and artifacts.

# Ownership

- This subtree owns target-specific local scripts and notes.
- Root owns public sanitization before anything is promoted to v5 or Pages.

# Local Contracts

- Treat everything here as private by default.
- Do not push or copy directly into public HTML.
- Sanitize target IPs, credentials, cookies, flags, OSIDs, and proprietary text before reusing snippets.
- Preserve challenge folders and user files unless Bruno explicitly asks for cleanup.

# Work Guidance

- Work locally first.
- Keep exploit scripts practical and target-specific here; generalize only when moving a pattern into v5.

# Verification

- No global verifier.
- Run script-specific checks only when safe for the current lab target.

# Child DOX Index

- `OSWE/AGENTS.md` - per-module challenge scripts and payloads.
