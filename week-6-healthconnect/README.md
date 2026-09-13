# Week 6 – HealthConnect Clinic: Proving the Week 5 Findings

In Week 5 I found out *why* patients miss appointments. In Week 6 my job was three things: prove those findings are real, improve the dashboard instead of rebuilding it, and actually connect my work to the Data Science track

## What I researched into, and what I found

1. **Do reminders work the same for every booking?**
   Reminders cut no-shows by about 3–5 points at every lead time, but they cannot fix early bookings: a reminded appointment booked 30+ days ahead still misses about 59% of the time (vs 63% without a reminder). So the fix for early bookings is not more reminders — it is a re-confirmation step.
2. **How big is the repeat-misser group?**
   Patients with 2 or more past no-shows hold only 16.4% of appointments but cause about 23.2% of all no-shows. A small group doing big damage — worth a personal phone call.
3. **Can far-away no-shows be handled remotely?**
   About 70.6% of no-shows from patients 20+ km away are Follow-ups or General Consultations — appointments that could be done by phone or video. The distance problem is partly a telehealth problem.
4. **Is the headline number stable?**
   I split the 18 months into two halves: 48.1% vs 48.9% no-show. The 48.5% rate is chronic, not seasonal — so the clinic can safely track it month by month.

## What changed from Week 5

- KPI 1 (No-Show Rate) now excludes cancellations, matching the Data Science track's binary target.
- Reminder effectiveness is now reported per lead-time band, not as one average that hides the truth.
- Two new measures added: repeat-misser concentration and telehealth-eligibility rate.
- Dashboard: the six Week 5 charts stay, three new ones added (Charts 7–9).

## Working with the Data Science track 

- **I sent:** the cleaned data with lead-time, distance and history bands, my five KPI formulas, and my ranked driver list.
- **They sent:** their Week 6 questionnaire — they dropped the 3-class model for a binary one (Attended vs No-Show) because Cancelled was unpredictable; they weight recall highest because a missed no-show is the costliest error; and their features include `is_long_distance` and `no_show_rate`, which are my distance and history findings turned into model inputs.
- **What changed for me:** my headline KPI now matches their target definition; their leakage note on waiting time moved into my limitations; my recommendations now cite their recall-first metric as the technical version of my cost argument.

## Tools

Python

## What comes next (Week 7)

Re-run the KPI cuts on a held-out slice of the data, test the dashboard filters, confirm my band definitions match the Data Science feature code, and re-check the small subgroups before the clinic acts on any of them.