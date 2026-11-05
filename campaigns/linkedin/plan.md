# LinkedIn campaign — HLTH_Video_Views

**Goal:** book meetings with ICP contacts at HLTH Las Vegas (15–18 Nov 2026), with an online meeting as the fallback.
**Status (5 Nov 2026):** all 7 ads built in Campaign Manager. Ad set is a draft, switched off, not launched (Karolina reviews and launches).

## Setup
| Setting | Value | Why |
|---|---|---|
| Objective | Video views | 7 short CEO videos (20–33s, 1:1); warm the list before the event |
| Audience | Matched audience: HLTH 2026 contact list (1,832 contacts → 1,400+ matched) | contacts picked by name for HLTH and Example Company fit; contact list chosen over company list to avoid paying for interns and sales reps |
| Backup audience | Company list (799 companies) + seniority Owner/Partner/CXO/VP/Director, excluding the contact list | use if contact match < ~500 |
| Locations | US + Europe, Canada, Mexico, South America, Asia, Oceania, Africa | ~80% of country-matched contacts are US, the rest across 21 countries; the list already limits reach, so wide locations only stop LinkedIn dropping list members (matched audience 1,200+ → 1,400+) |
| Language | English | |
| Audience Expansion / LAN | Off / Off | tiny list; keep delivery on-list and on LinkedIn |
| Bidding | Maximum delivery | |
| Budget / dates | USD 30/day, 4–18 Nov 2026 (max USD 450) | stops when HLTH ends |
| CTA button | Register (Ads 1–5, 7); Learn more suggested for Ad 6 | LinkedIn has no "Book" button |
| Destination | example.com/hlth with UTMs (see tracking audit #5) | |

## Data prep (done)
- Converted the HLTH spreadsheet ("Linkedin Ads list" tab) to LinkedIn's matched-audience CSV format; removed 1 duplicate email.
- Upload failed on first try: 4 rows had an email address in the job-title column (error in source sheet). Cleared those titles, re-uploaded.
- Contact files are client data and are **not** stored in this repo.

## UTMs
`https://example.com/hlth?utm_source=linkedin&utm_medium=paid_social&utm_campaign=HLTH_Video_Views&utm_content=ad1` … `ad7`
Open issue: duplicated source/medium from account-level parameters (see `analysis/tracking-audit.md` #5).

## Test design
- **HLTH-first** opening: Ads 1, 2, 4, 6, 7 · **Problem-first** opening (HLTH at the end): Ads 3, 5
- For a clean read, the two groups should sit in separate ad sets. Otherwise LinkedIn will barely serve the test pair (logged as a change-request item).

## Ads
All headlines mention HLTH. Intro text ≤ 600 characters.

### Ad 1 — HLTH intro
**Headline:** Let's meet at HLTH. Book your 20-minute slot
> Heading to HLTH Las Vegas? If your team is facing any of these challenges, I'd like to help:
> ✅ Your AI model works in a notebook, but never makes it into production
> ✅ Your data is spread across silos, so your models never see the full picture
> ✅ A hospital security review is ahead, and your AI setup has to pass it
>
> At Example Company, this is what we do every day for healthcare and medtech teams: taking AI from prototype to production and making it secure.
>
> Book a 20-minute slot below and let's talk about your needs in person at HLTH. You can also visit our booth from November 15 to 18.

### Ad 2 — FDA from the inside
**Headline:** From notebook to FDA-ready. Book 20 minutes at HLTH
> Heading to HLTH Las Vegas with an AI model that hits 0.94 in the notebook? The FDA reviewer will ask about everything else:
> ✅ Which data trained this exact version?
> ✅ How was it validated?
> ✅ What happens when you retrain?
> ✅ Who can see what?
> ✅ How will you know when it drifts?
>
> I've been on the other side of that table. In 20 minutes, you'll leave with a list of what's missing between your notebook and an actual submission.
>
> Book a 20-minute slot below and let's meet at HLTH Las Vegas, November 15 to 18. Not going to Vegas? Click the link below and book an online meeting instead.

### Ad 3 — Data before AI (problem-first test)
**Headline:** Your data could pay for itself. Let's talk at HLTH
> Does every analysis take weeks? That's almost never an analytics problem.
>
> It's imaging in one system, device data in another, EHR and claims somewhere else, and every export is a favor.
>
> Before you buy another AI tool, let's spend 30 minutes on the first number you actually need and the data foundations to get it.
>
> At Example Company, we build data and AI for healthcare and medtech teams.
>
> Book a slot below and let's meet at HLTH Las Vegas, November 15 to 18. Not going to Vegas? Click the link below and book an online meeting instead.

### Ad 4 — Hospital security review
**Headline:** Hospital security review ahead? Meet us at HLTH
> Meeting hospitals at HLTH Las Vegas? Their security review will ask five things about your AI:
> ✅ Where does the patient data live?
> ✅ Who can access it?
> ✅ Does your BAA match your actual architecture?
> ✅ Which model and data version produced this output?
> ✅ What happens on a breach?
>
> If those answers live in people's heads, the review takes weeks. If they live in a system, it takes a day.
>
> In a 30-minute session, we'll assess where your setup stands. Book a slot below and let's meet at HLTH, November 15 to 18. Not going to Vegas? Click the link below and book an online meeting instead.

### Ad 5 — Healthcare only (problem-first test)
**Headline:** Book a 30-minute slot with us at HLTH 2026
> Example Company is the data and AI team for healthcare and medtech sectors.
>
> We work only in healthcare, because in this industry the model is just 30% of the work. The other 70% is:
> ✅ Data you're allowed to use
> ✅ An architecture that passes an audit
> ✅ A business case someone will sign
>
> That's why we have engineers who specialise in healthcare and physicians on the team. I run the first conversation myself and stay on as your architect.
>
> Let's meet at HLTH Las Vegas, November 15 to 18. Book a slot below and let's talk about your project.

### Ad 6 — Meet us + see our work
**Headline:** Meet Example Company at HLTH. See our work, book a slot
> Going to HLTH Las Vegas? Let's meet in person, November 15 to 18.
>
> Example Company is the data and AI team for healthcare and medtech. If you'd like to know more about us before we meet, visit our website to see our case studies and what we've already delivered for healthcare teams.
>
> Then book a 30-minute slot at HLTH and let's talk about your project 👉 example.com/hlth

### Ad 7 — See you in Vegas
**Headline:** AI and data in healthcare? Let's talk in person at HLTH. Book a slot
> Heading to HLTH Las Vegas? I'll be at the Example Company booth all four days, November 15 to 18.
>
> If you're at HLTH, grab 30 minutes with me. Let's talk about the challenges and best practices of AI and data projects in healthcare and medtech: what's blocking yours and how to move it forward.
>
> Book your slot below. See you in Las Vegas!

## Pre-launch checks
- [ ] Slot length on example.com/hlth matches each ad (Ads 1–2 say 20 min; 3–7 say 30)
- [ ] UTM decision made (tracking audit #5) and Ad 1's destination URL updated to the full UTM link
- [ ] Video previews checked: LinkedIn has no custom thumbnail for video ads; check AD1, AD3, V5, V6 first frames
- [ ] Ad 6 video still announces the new website: swap video or accept mismatch
- [ ] V7 copy checked against the re-cut video
- [ ] Booking event fires in GA4
- [ ] Karolina clicks Review & Launch

## After HLTH
- Retarget video viewers (≥ 50%) and /hlth visitors with follow-up and online-meeting ads until 15 Dec
- Feed learnings (HLTH-first vs problem-first, best-performing pain point) into the Trust Generation campaign
