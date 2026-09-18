# styl3s — Skin Retouching for Portraits: 30-Day Training Plan

This repository (Ben's GitHub profile repo, `styl3s/styl3s`) also hosts a
self-paced, 30-day training plan for learning skin retouching for portraits.

## Structure

- `SCHEDULE/` — the training plan.
  - `SCHEDULE/OUTLINE.md` — the master map of all 30 days to learning
    objectives, weighted toward Ben's identified weak areas. Written after
    the initial interview + diagnostic quiz(zes).
  - `SCHEDULE/Day 01/` … `SCHEDULE/Day 30/` — one folder per day. Each
    contains that day's session file, generated just-in-time (not all
    pre-written), so it can reflect what's been learned about Ben's
    progress since the outline was written.

## Session generation workflow

1. `OUTLINE.md` is written once, up front, after the interview and
   diagnostic quiz(zes) establish Ben's current skill level per domain.
2. At the start of each day, that day's session file is generated from:
   - the relevant objectives in `OUTLINE.md` for that day, and
   - anything learned about Ben's understanding/progress in prior sessions
     (quiz answers, mistakes, questions asked, topics that needed repeating).
3. Every session file ends with:
   - a summary of what was learned/covered that day, and
   - the exact line: `You have completed DAY N of your 30 day training plan!`

## Conventions

- Day folder names use two-digit, space-separated numbering: `Day 01`
  through `Day 30`, so they sort correctly.
- Session files live at `SCHEDULE/Day NN/session.md` unless a day needs
  supporting assets, in which case those live alongside it in the same
  day folder.
