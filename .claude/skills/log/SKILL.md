---
name: log
description: Capture a piece of work Gabe did as a dated evidence entry in data/. Use when Gabe mentions shipping, leading, fixing, or learning something worth remembering, or asks to catch up on recent work.
---

# log

Stub: roadmap step 3 fills in the behavior. Intended contract:

- **Input:** a conversation. Gabe describes the work, or pastes or points at material from the current workplace. Ask where to look rather than assuming a source.
- **Output:** one new file per piece of work in `data/`, named `YYYY-MM-DD-short-slug.md` and following `data/_template.md`.
- **Rules:** write summaries in Gabe's words, never copied excerpts. Real client names are fine here because `data/` is never published. If the result or impact is missing, ask for it.
