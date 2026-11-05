# Skill 02 — Tracking audit

No campaign launches on tracking we haven't verified. Most "bad campaigns" are bad measurement.

## Output
`analysis/tracking-audit.md` — checklist with pass / fail / fix for each item.

## Checklist
1. **GTM:** container published; tags for GA4, Google Ads conversion + conversion linker, LinkedIn Insight Tag, Meta Pixel (if used).
2. **Conversions defined:** primary (demo / trial) and secondary (pricing view, content download), with values. Primary conversions are marked primary in each ad platform.
3. **Test fire:** submit a test form, then confirm it appears in GTM preview, GA4 DebugView, Google Ads (diagnostics) and LinkedIn conversion status.
4. **Consent mode:** check the consent tool doesn't block `gclid`, `li_fat_id` or `fbclid` storage (a known cause of zero LinkedIn conversions), and that Consent Mode v2 is configured.
5. **UTMs & click IDs** reach the CRM: hidden form fields capture UTM source/medium/campaign, gclid and li_fat_id.
6. **CRM loop:** lead source is set automatically; lifecycle stages (Lead → MQL → SQL → Opportunity → Won) exist; offline conversion import (Google Ads) or CAPI/CRM sync (LinkedIn) is planned.
7. **Enhanced conversions** (Google) and the LinkedIn Conversions API where possible.
8. **Cross-domain / thank-you pages:** no double counting; thank-you pages are excluded from remarketing audiences as needed.

## Rules
- Never change the client's GTM or CRM without approval. Write the fix as a change request.
- Re-run monthly, and immediately when the daily monitor flags a conversion drop.
