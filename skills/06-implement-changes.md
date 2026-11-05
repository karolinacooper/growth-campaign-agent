# Skill 06 — Implement approved changes

## Precondition
`changes/YYYY-Www/change-request.md` with items marked **approved** by the user (in the file or in chat: "approved 1, 3, 4").

## Steps
1. Re-read the approved items. Implement only those; skip and note anything not approved.
2. For each item:
   - Screenshot / export the "before" state.
   - Make the change (API connector if available, otherwise Claude in Chrome).
   - Verify it saved: reload and check.
   - Screenshot the "after" state.
3. Append one line per change to `memory/change-log.md`:
   `YYYY-MM-DD | channel | campaign | change | hypothesis | metric to check | review date`
4. Mark each item in the change request as `done` / `skipped (reason)` / `failed (reason)`.
5. Post a summary to chat: what changed, what was skipped, when we'll review.

## Rules
- Never exceed what was approved (e.g. approved +15% budget means +15%, not +20%).
- Never touch billing, payment methods, account access or conversion settings outside an approved item.
- If the platform UI differs from expected or something looks wrong, stop and ask.
- Rollback: if a change causes a guardrail breach within 48h, propose the rollback immediately (it still needs approval).
