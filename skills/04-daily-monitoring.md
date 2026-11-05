# Skill 04 — Daily monitoring (scheduled, weekdays)

A 5-minute health check, not an optimisation session.

## Output
`monitoring/YYYY-MM-DD.md` + a short chat/Slack/email alert **only if something needs attention**.

## Steps
1. Pull yesterday's and the rolling 7-day data per campaign: spend, impressions, clicks, CTR, CPC, conversions, CPL; budget pacing vs. month-to-date plan.
2. Check every guardrail in `config/kpis.md`.
3. Scan the account for disapproved ads, policy limits, billing warnings and tracking diagnostics.
4. Google: review yesterday's search terms; add clearly irrelevant ones as negatives (auto-action, log each).
5. Classify the day: 🟢 on track · 🟡 watch (trend worth noting) · 🔴 action needed (guardrail breached).
6. For 🔴, write a draft change request item in `changes/YYYY-Www/change-request.md` and alert the user. Don't fix it yourself unless it's an auto-action.

## Output format
```
# Daily monitor — YYYY-MM-DD  [🟢/🟡/🔴]
Spend: €X (Y% of pace) · Conv: N · CPL: €X (7d: €X vs target €X)
Alerts: …
Auto-actions taken: …
Watch list: …
```

## Rules
- No structural changes. Monitoring ≠ optimising.
- If all three platforms show zero conversions, suspect tracking first (run the skill 02 checks).
