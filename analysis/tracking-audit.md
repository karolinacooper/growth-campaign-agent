# Tracking audit — Example Company — status 5 Nov 2026

| # | Item | Status | Notes / fix |
|---|---|---|---|
| 1 | GTM container on site | ✅ live from 1 Nov | |
| 2 | GA4 key events: form submit, calendar booking, email click | ✅ defined in plan / verify firing | test-fire a booking on /hlth before HLTH flight goes live |
| 3 | LinkedIn Insight Tag | ⚠️ verify | needed for remarketing to site visitors from 15 Nov |
| 4 | Consent tool vs click IDs | ⚠️ check | make sure the consent banner doesn't block `li_fat_id` (known cause of 0 LinkedIn conversions on another account) |
| 5 | UTM convention | ❌ open decision | LinkedIn account-level tracking parameters already append `utm_source=linkedin&utm_medium=paid-social`. Ad URLs also carry `utm_medium=paid_social`, so source/medium are duplicated. **Option A:** remove account-level params (account-wide change, needs approval). **Option B:** shorten ad URLs to `?utm_campaign=HLTH_Video_Views&utm_content=adX` and standardise on `paid-social`. |
| 6 | UTMs in ABM messages | ✅ in plan | one `utm_campaign` per sequence, `utm_content` per step |
| 7 | Pipedrive: lead source + segment + signal | ✅ in place | add "HLTH meeting" and "paid channel" sources |
| 8 | Bot traffic filtering | ⚠️ | 34% of users (Singapore, China, "(not set)") look like bots: exclude in GA4 reporting views |
| 9 | Google Ads conversions imported from GA4 | ⏳ when the account is created | |
