# Growth Campaign Agent

A Claude-based operating system for running B2B paid acquisition end to end: market analysis → tracking audit → campaign build → daily monitoring → weekly optimisation → approved implementation → reporting.

Built and used by Karolina Cooper (0101marketing) for B2B client work. The worked example in this repo is a real deployment, anonymised as **Example Company**: a data and AI services firm for healthcare and medtech, targeting US AI medtech companies, with a LinkedIn campaign around the HLTH 2026 conference and a Google Ads purchase-intent plan.

**Live example in this repo:** [market analysis](analysis/market-analysis.md) · [tracking audit](analysis/tracking-audit.md) · [LinkedIn HLTH campaign](campaigns/linkedin/plan.md) · [Google Ads plan](campaigns/google-ads/plan.md) · [first change request](changes/2026-W45/change-request.md) · [change log](memory/change-log.md) · [learnings](memory/learnings.md)

## Why
Most campaign "optimisation" is ad hoc: someone logs in, eyeballs numbers, changes things, forgets why. This repo turns that into a repeatable loop with:
- **Written hypotheses** before every change
- **Decision rules and guardrails** so the agent never makes a risky move on its own
- **A human approval gate** between "recommend" and "implement"
- **A change log and learnings file** so every week builds on the last
- **Pipeline-level reporting**, not just clicks and CPL

## How it works

```
 ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
 │ 1. Market    │──▶│ 2. Tracking  │──▶│ 3. Campaign  │
 │    analysis  │   │    audit     │   │    build     │
 └──────────────┘   └──────────────┘   └──────┬───────┘
                                              ▼
 ┌──────────────┐   ┌──────────────┐   ┌──────────────┐
 │ 7. Reporting │◀──│ 6. Implement │◀──│ 5. Weekly    │◀── 4. Daily monitoring
 │   (pipeline) │   │  (approved)  │   │  optimisation│      (scheduled)
 └──────┬───────┘   └──────────────┘   └──────────────┘
        └────────── learnings feed back into 1, 3 and 5 ──────────┘
```

| Stage | Skill | Trigger | Output |
|---|---|---|---|
| 1 | `skills/01-market-analysis.md` | Once per client / quarterly refresh | `analysis/market-analysis.md` |
| 2 | `skills/02-tracking-audit.md` | Before launch, then monthly | `analysis/tracking-audit.md` |
| 3 | `skills/03-campaign-build.md` | After 1 + 2 approved | `campaigns/<channel>/plan.md` + build in-platform |
| 4 | `skills/04-daily-monitoring.md` | Scheduled, weekdays 9:00 | `monitoring/YYYY-MM-DD.md` + alerts |
| 5 | `skills/05-weekly-optimisation.md` | Scheduled, Monday 9:30 | `changes/YYYY-Www/change-request.md` |
| 6 | `skills/06-implement-changes.md` | Only after human approval | Platform changes + `memory/change-log.md` |
| 7 | `skills/07-reporting.md` | Weekly + monthly | `reports/` |
| + | `skills/08-creative-testing.md` | Continuous, called by 3 and 5 | Test briefs + results |

## Repo layout
- **Behaviour** (replaceable instructions): `CLAUDE.md`, `skills/`, `scheduled/`, `templates/`
- **Configuration** (per client): `config/`
- **Knowledge / state** (permanent record): `analysis/`, `campaigns/`, `monitoring/`, `changes/`, `reports/`, `memory/`

Hard rule: knowledge never goes into `skills/`. Swap the config and the same system runs for a new client.

## Tools
Claude (skills + scheduled tasks), Claude in Chrome (for ad platforms without an API connector), Google Ads, LinkedIn Campaign Manager, GA4, GTM, CRM (HubSpot/Pipedrive), Google Sheets for exports.

## Running it
1. Fill in `config/client.md`, `config/kpis.md`, `config/brand-voice.md`.
2. Open a Claude session in this folder: "Run stage 1 for Example Company."
3. Review and approve each stage's output before moving on.
4. Set up the three scheduled tasks using the prompts in `scheduled/`.
