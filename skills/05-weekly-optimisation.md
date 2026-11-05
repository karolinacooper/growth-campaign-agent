# Skill 05 — Weekly optimisation (scheduled, Mondays)

Analyse last week, decide what to change, and write it up as a change request for approval.

## Inputs
Last 7 and 28 days of platform data, GA4 landing page data, CRM lead quality (SQL status by source/campaign), `monitoring/` files from the week, `memory/change-log.md`, `memory/learnings.md`.

## Output
`changes/YYYY-Www/analysis.md` + `changes/YYYY-Www/change-request.md` (from `templates/change-request.md`).

## Steps
1. **Review last week's changes.** For each change in the log from 7–21 days ago, did the hypothesis hold? Write the verdict to `memory/learnings.md`.
2. **Funnel view per campaign:** impressions → clicks → leads → SQLs → pipeline €. Find the weakest step.
3. **Google Ads deep-dive:** search terms (new negatives, new exact keywords), keyword-level cost per conversion, quality score components, impression share lost to budget vs. rank, ad strength, asset performance, device / location / time-of-day splits.
4. **LinkedIn deep-dive:** audience/company-level performance (demographics report), frequency, creative fatigue (CTR decay), cost per lead vs. lead quality by campaign.
5. **Landing pages:** conversion rate by page and device; bounce/engagement; form drop-off.
6. **Lead quality:** join CRM SQL status to campaign/keyword/audience. Optimise toward cost per SQL.
7. **Decide 3–5 changes**, ranked by expected impact on pipeline. Each item: what, why (data), hypothesis, expected effect, risk, rollback plan, approval needed (yes/no).
8. **Creative:** confirm one test is running per channel; propose the next one via skill 08.
9. Post a 5-line summary to chat with a link to the change request and ask for approval.

## Rules
- Apply the decision rules and minimum-data thresholds in `config/kpis.md`.
- Don't re-propose a change that failed in `memory/learnings.md` without new evidence.
- If tracking is suspect, the only change this week is fixing tracking.
