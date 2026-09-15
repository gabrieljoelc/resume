---
name: refresh
description: Update profile.yaml and linkedin.md from entries in data/. Use when Gabe asks to refresh, update, or sync the profile or the LinkedIn copy.
---

# refresh

Stub: roadmap step 3 fills in the behavior. Intended contract:

- **Input:** `data/` entries not yet reflected in `profile.yaml`, plus the current `profile.yaml`.
- **Output:** edits to `profile.yaml` (JSON Resume), then `linkedin.md` regenerated from it. Gabe reviews the diff; this skill publishes nothing.
- **Rules:** apply the confidentiality rules in `CLAUDE.md` at the `profile.yaml` boundary. Rewrite from `data/`, never copy. Cite the source entry in a YAML comment on each highlight (`# from: data/<file>.md`). Never invent content.
