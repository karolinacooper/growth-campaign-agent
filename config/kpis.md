# KPIs, guardrails and decision rules — Example Company

## North star
**Booked meetings with ICP companies → qualified opportunities in Pipedrive**, at a known cost per meeting.

## Targets
| Metric | Target | Source |
|---|---|---|
| HLTH meetings booked | 15 (most before 15 Nov) | calendar + Pipedrive |
| Meetings from paid channels (Dec onwards) | set with sales after HLTH | GA4 + Pipedrive |
| Cost per booked meeting | baseline from November | spend + Pipedrive |
| LinkedIn video view rate (HLTH) | baseline in first 3 days | Campaign Manager |
| Landing page → booking rate (/hlth) | baseline in first 3 days | GA4 |
| Outreach reply rate | > 2% (previous outbound baseline) | Pipedrive |
| Engaged listed companies | tracked weekly | UTMs + Pipedrive |

## Minimum data before calling a result
- LinkedIn ad test: ≥ 1,000 impressions per ad, or 5 days in a short flight
- HLTH-first vs problem-first copy test: compare at ad-group level after ≥ 3,000 impressions per group
- Google keyword: spend ≥ 2× target cost per meeting with no conversion → candidate to pause
- Landing page: ≥ 100 sessions per variant

## Guardrails (daily monitor alerts)
- Daily spend > 130% or < 50% of daily budget
- Matched audience falls below 300 (LinkedIn stops serving)
- Frequency > 6 in the HLTH flight (small audience, fatigue risk)
- 0 bookings for 3 days on /hlth while clicks continue → check calendar embed and GA4 event
- UTMs: duplicated or inconsistent `utm_medium` (see open issue in `analysis/tracking-audit.md`)
- Disapproved ads, payment or account warnings

## Auto-actions (no approval)
- Add obviously irrelevant search terms as negatives (Google)
- Pause a single disapproved ad
- Nothing else

## Approval thresholds
- Any budget change > 20% per campaign per week
- Pausing a campaign, or any ad with bookings
- New campaigns, audiences, bid strategies
- Any copy or creative change (copy approval rests with Karolina; CEO voice approval with the CEO)
- Account-level settings (e.g. account tracking parameters)
- Anything in the live dashboard when Karolina has said "no more dashboard changes"

## Decision rules
1. Tracking first: if bookings aren't attributed, fix that before optimising.
2. Shift budget toward the lowest cost per booked meeting, not the cheapest view or click.
3. Max 3–5 changes per week; in short flights (HLTH) max 2 changes per review.
4. Always keep one copy or creative test running per channel.
