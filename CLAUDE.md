# Career pipeline

This repo keeps Gabe's professional profiles up to date. Evidence of work goes in, Claude shapes it into a public-safe profile, and the profile fans out to each destination.

## Pipeline

```
data/ ──/refresh──▶ profile.yaml ──┬──/refresh──▶ linkedin.md ──paste──▶ LinkedIn
                                   └──CI build──▶ site/ ──deploy──▶ Vercel (HTML + PDF)
```

| Path | Stage | Written by |
| --- | --- | --- |
| `data/` | Evidence: one dated entry per piece of work | `/log` |
| `profile.yaml` | Model: public-safe profile in JSON Resume format | `/refresh` |
| `linkedin.md` | Output: paste-ready LinkedIn copy | `/refresh` |
| `site/` | Output: renders `profile.yaml` to HTML and PDF | CI |
| `src/default.yml` | Legacy FRESH resume, removed once migrated | none |

AI stages (`/log`, `/refresh`) run in Claude sessions and produce diffs Gabe reviews. Deterministic stages (the site build) run in CI. Several parts are still stubs; the roadmap in `README.md` says which step fills each one.

## Hard rules

- `profile.yaml` is the confidentiality boundary. Everything downstream of it is public; nothing in `data/` is. Public text is rewritten from `data/`, never copied.
- Only **Imgix** may be named as a client, always capitalized. Every other client is anonymized by industry ("Fintech client", "EdTech client", "supply-chain client").
- Client label map: TODO, add real client name → label pairs here once the repo is private. Never add them while the repo is public.
- `data/` entries are Gabe's own summaries. Never store excerpts copied from work systems (Slack, meeting notes, docs, tickets).
- Never invent content. If something is missing, such as the About section, ask.
- LinkedIn is read-only. Draft changes in `linkedin.md`; never automate edits on linkedin.com (its User Agreement bans automation).

## Content notes

- Aligned (formerly Squadformers) start date is 2022-08-25. Keep the two titles as LinkedIn shows them: Lead Software Engineer (Aug 2022 – Jun 2023) and Staff Software Engineer (Jun 2023 – present).
- LinkedIn has no About section yet, and `info.brief` in `src/default.yml` is intentionally stale. Gabe will write the About; don't draft one unasked.
- The resume starts in 2011. Lockheed Martin (2007–2011) and Harmony House (1999–2007) appear only on LinkedIn.
- HomeLight and RetailMeNot keep month-level dates where LinkedIn shows only years.
