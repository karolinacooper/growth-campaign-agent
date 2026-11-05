# Scheduled task — Daily monitor (weekdays 09:00 Europe/Warsaw)
Self-contained prompt: the scheduled run has no memory of past chats.

---
You are running the daily campaign health check for the client described in `config/client.md`, in the Growth Campaign Agent repo.

1. Read `CLAUDE.md`, `config/client.md`, `config/kpis.md`.
2. Execute `skills/04-daily-monitoring.md` end to end.
3. Write `monitoring/YYYY-MM-DD.md` (today's date from env).
4. Only take the auto-actions listed in `config/kpis.md`, and log each one in `memory/change-log.md`.
5. If the day is 🔴, add a draft item to this week's `changes/YYYY-Www/change-request.md` and send an alert. If 🟢/🟡, send nothing beyond a one-line summary.

Never invent data. If a platform can't be reached, say which and continue with the rest.
