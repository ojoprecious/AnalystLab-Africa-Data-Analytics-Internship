# Week 5 – HealthConnect Clinic: Why Do Patients Miss Appointments?

## The problem

HealthConnect Clinic keeps losing appointment slots because patients don't show up, and the clinic doesn't know why. My job this week was to go through the clinic's appointment records, find the patterns behind the missed visits, and turn them into advice the clinic can actually use.

## The data I worked with

One table, 5,000 appointments. Each row tells me: who the patient is (age group, gender), what they booked (type, day, time of day), how far in advance they booked, whether they were reminded (and by what channel — SMS, WhatsApp or email), how far they live from the clinic, and whether they showed up.

Before trusting any of it, I checked it for problems:
- 90 rows had no distance and 60 had no waiting time. I did not invent values — I simply left those rows out of the distance and waiting-time counts.
- Dates arrived in a messy format (like 2/6/2025), so I converted them to proper dates before doing anything time-related.
- "No reminder channel" is not an error — it just means no reminder was sent, so I treated it that way.

Why this matters: if you don't check your data first, you can end up making decisions on top of mistakes.

## What I found

- **Almost half of all appointments end in a no-show (48.5%).** This is not a small problem — it is the clinic's biggest one.
- **The earlier you book, the more likely you are to miss.** Booked within a week: 28% miss. Booked 1–2 months ahead: 60% miss. People simply forget.
- **Past behaviour repeats.** Patients who missed before missed again at 55.4%, against 43.5% for patients with a clean record.
- **Distance matters.** The miss rate climbs from 46.5% (under 10 km) to 68.1% (over 30 km).
- **Reminders help, but only a little.** 47.4% miss with a reminder vs 51.4% without. SMS works best of the three channels.
- **Day of week, time of day and appointment type make almost no difference** — so rearranging the schedule would not fix much.

I count cancellations separately from no-shows. A patient who cancels gives the clinic a chance to fill the slot; a no-show wastes it. Mixing the two would hide the real problem.

## What I would tell the clinic to do

1. Re-confirm early bookings — a message at the two-week mark and again 72 hours before the visit.
2. Call (not just text) patients who have missed before.
3. Offer phone/video consultations or rescheduling to patients who live far away.
4. Keep SMS as the default reminder channel.

## Tools

Python

## Author

Ojo Precious