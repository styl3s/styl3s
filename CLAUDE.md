# CCNA Training Plan

This project is a 45-day, self-paced study plan for the Cisco CCNA exam
(200-301), built for Ben (@styl3s).

## Structure

- `SCHEDULE/` — one folder per training day, `Day 01` through `Day 45`
  (two-digit, zero-padded names so they sort correctly).
- `SCHEDULE/OUTLINE.md` — the master map of all 45 days to CCNA exam
  objectives, weighted toward Ben's weak areas as identified by the
  initial interview and quiz assessment.
- `SCHEDULE/Day NN/` — each day's session file is generated at the start
  of that day from the outline plus everything learned about Ben's
  progress since. Every session ends with a recap of what was covered
  and the line: "You have completed DAY N of your 45 day training plan!"

## Workflow

1. Interview Ben about background, timeline, study habits, and lab
   access before building the outline.
2. Run a diagnostic quiz (20 questions spanning the CCNA domains), and
   follow up with more targeted questions if his level isn't clear yet.
3. Write `SCHEDULE/OUTLINE.md` mapping all 45 days once his strengths
   and weaknesses are known.
4. Generate each day's session file just-in-time (not all 45 in advance)
   so later days can adapt to how earlier days went.

## CCNA 200-301 Domains (exam blueprint weighting)

1. Network Fundamentals (~20%)
2. Network Access (~20%)
3. IP Connectivity (~25%)
4. IP Services (~10%)
5. Security Fundamentals (~15%)
6. Automation and Programmability (~10%)
