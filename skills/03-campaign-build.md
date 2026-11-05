# Skill 03 — Campaign build

Turn the approved market analysis into live, well-structured campaigns.

## Preconditions
`analysis/market-analysis.md` approved · `analysis/tracking-audit.md` all critical items pass.

## Output
`campaigns/<channel>/plan.md` (from `templates/campaign-plan.md`), then the build in-platform, then `campaigns/<channel>/build-log.md` with screenshots/links.

## Google Ads (Search)
1. Structure by intent: Brand · Competitor · Solution/category · Problem. Separate campaigns per market/language.
2. Keywords: exact + phrase from the analysis clusters; shared negative list (jobs, free, tutorial, irrelevant industries…).
3. RSAs: 2 per ad group, 15 headlines / 4 descriptions, pinned only where needed, built from the messaging angles.
4. Assets: sitelinks, callouts, structured snippets, image assets.
5. Bidding: start with Maximise Conversions (or Manual CPC if there's no conversion history); move to tCPA after ~30 conversions in 30 days.
6. Settings: location = "presence", networks = Search only (no Display/partners), ad schedule matching the client's sales hours if relevant.

## LinkedIn Ads
1. Audiences: company list (ABM) and/or firmographic + job-function/seniority targeting. Exclude existing customers, competitors and employees.
2. Funnel: awareness (video / thought leadership) → consideration (document ads / case studies) → conversion (lead gen forms or website conversions) for retargeted engagers.
3. Creative: 3–4 variants per campaign from different angles.
4. Bidding: start on manual or cost cap to control CPC; check the audience is ≥ 50k for prospecting.
5. Lead gen forms: sync to the CRM, hidden fields for campaign tagging.

## Launch checklist
- [ ] Conversion actions attached and verified
- [ ] UTMs on every final URL (tracking template)
- [ ] Budgets match the approved plan
- [ ] Ads approved by the platform
- [ ] Client sign-off on copy
- [ ] Entry added to `memory/change-log.md`: "Launch"

## Rule
Build drafts in-platform **paused**. Enable only after the user approves the launch checklist.
