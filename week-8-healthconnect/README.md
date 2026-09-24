# Week 8 – HealthConnect Clinic: Final Integration, Presentation and Project Close

Part of my AnalystLab Africa Data Analytics internship. The final week of the HealthConnect project.

## What this week was about

Weeks 4 to 7 were about finding, deepening and proving why patients miss appointments. Week 8 was about turning all of that into one clear story the clinic can act on: a final dashboard, a final report with an executive summary, a short slide deck, and a recorded presentation of my own contribution.

## The final answer to the project question

HealthConnect can cut missed appointments by acting on three proven drivers instead of reminding everyone:

1. **Early bookings** miss at 60.5% (31–60 days ahead) → re-confirm at two weeks and again 72 hours before.
2. **Repeat missers** — 16.4% of appointments cause 23.2% of all no-shows → phone-call them, don't just text.
3. **Far-away patients** miss at 68.1% (30+ km), and 70.6% of their no-shows are visit types that can be done by video → offer video visits.

On top of that, the Data Science track's model — built using my distance and history bands — flags high-risk appointments automatically, so the clinic knows who to call before the slot is wasted.

## How the pieces connect

- **Data Analytics (me):** measured the problem, proved the drivers, built the dashboard and the recommendations.
- **Data Science:** turned my bands into model features; we locked one shared definition of a no-show (cancellations excluded); their risk score automates my phone-call list.
- **Project Management:** sequenced the final deck and confirmed readiness.

One number everywhere: 51.2% no-show rate excluding cancellations — the same figure in the report, on the dashboard and inside the model.

## What five weeks taught me

- Check the data before you trust it: missing values, duplicates, and "None" meaning "no reminder sent".
- A finding is only worth acting on once it survives a second method — Excel against Python, a random sample, both halves of the period.
- The hardest skill is deciding what **not** to act on: day, time, type and waiting time made no difference, so I left them alone.
- Stating your limitations plainly makes the work stronger, not weaker.
