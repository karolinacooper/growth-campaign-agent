# Change request — Example Company — 2026-W45 (pre-launch)

**Summary:** HLTH_Video_Views is fully built as a draft. Three decisions are needed before launch so the HLTH-first vs problem-first test reads cleanly and bookings are attributed.

| # | Channel / campaign | Change | Evidence | Hypothesis | Risk | Rollback | Needs approval | Status |
|---|---|---|---|---|---|---|---|---|
| 1 | LinkedIn account | Fix UTM duplication: option B, shorten ad URLs to `?utm_campaign=HLTH_Video_Views&utm_content=adX`, standardise on `paid-social` | account appends source/medium | clean GA4 attribution per ad | none (ad-level only) | restore full URLs | yes | proposed |
| 2 | HLTH_Video_Views | Split Ads 3 + 5 into their own ad set (USD 10/day; main set USD 20/day) | ads in one set compete; LinkedIn would under-serve the test pair | a readable HLTH-first vs problem-first result | smaller audience per set | merge back | yes | proposed |
| 3 | HLTH_Video_Views | Change Ad 6 CTA button from Register to Learn more | Ad 6 copy invites people to see the work first | button matches the promise, higher CTR | fewer direct bookings from Ad 6 | switch back | yes | proposed |

**Approve by replying:** "approved 1, 2, 3" (or any subset).
