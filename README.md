# Take-Home Exercise: GI Trigger-Food Review Tool

## Context
Ayble's care team (ie, doctors and dietitians) wants a simple internal tool to
review a patient's meals and GI symptoms over time, so they can make
observations/correlations between the food the patient is eating and their
symptoms. This will allow them to prepare for meetings with the patient.

Data for this tool comes from a few different systems, and the exports in
`data/` reflect that — they weren't produced by one team with one convention.

## Time Expectation
Aim for **2 hours or less**. Use any AI tools you'd like — we're evaluating
your judgment and understanding, not whether you typed every line by hand.

## What You're Building
A full-stack internal tool with three parts:

### A. Data layer
Design and populate database tables from the four source files. You
don't need to preserve their shapes — design your schema however you think
is appropriate.

### B. API
Build endpoints to:
1. List a patient's meals and symptom logs, merged into a single chronological
   timeline
2. Let a care team member add a short prep note to a patient (e.g. "ask about
   dairy intake before next visit") — this is the one write path in the tool

### C. UI
Build a simple internal-tool UI with:
1. A patient timeline view mixing meals and symptoms
2. A way to view and add prep notes for a patient

### Bonus
Put on your product cap. Is there anything else you'd add to help the care
team accomplish what's described in the Context section above? Use your
judgment on scope — we'd rather see one thoughtful addition than several
half-finished ones.

## Stack
Use whatever you're fastest in. We use **React / React Native, Python
(FastAPI), PostgreSQL** — bonus points for working in that stack, not required.

## Data
| File | Contents |
|---|---|
| `patients.csv` | One row per patient: ID, name, date of birth, and home timezone |
| `foods.csv` | Food catalog: ID, name, and one or more categories (e.g. dairy, gluten, high-fodmap) |
| `meals.json` | Meal log export from our mobile app. Each meal belongs to a patient and references one or more foods |
| `symptoms.csv` | Symptom log: patient, time logged, symptom type, severity, and optional notes |

## What We're Evaluating
- Whether your schema and endpoints make sense given the four sources
- How your solution holds up when the underlying data doesn't perfectly
  cooperate
- Code organization and reuse
- **Your ability to explain every decision** — including ones an AI tool made
  for you. We'll ask you to walk through your schema, your API and UI, and any product judgment behind what you chose to
  build. We'd love to hear your ideas for how you could expand or improve this
  if you had an entire sprint to work on it.

## What to Submit
- A link to a repo
- A short `NOTES.md`: assumptions you made, anything that affected your
  approach, and what you'd do differently with more time
- Instructions to run it locally
