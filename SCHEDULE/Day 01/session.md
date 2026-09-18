# Day 01 — Workflow Architecture & Personal Template

**Time budget:** 60 minutes
**Where this fits:** Week 1 — Foundations & Non-Destructive Fluency

## Why today looks like this

The diagnostic showed you already understand *why* non-destructive editing
and the Lightroom-to-Photoshop handoff matter — you correctly identified
global-then-local-then-Photoshop as the right order, and know what a Smart
Object is for. What you don't have yet is a **repeatable, fast personal
ritual** for setting it up under time pressure. Today builds that ritual
once, properly, so every later day (and every future gallery) starts from
the same fast, non-destructive foundation instead of being rebuilt from
scratch each time.

## Objectives

1. Establish your standard Lightroom → Photoshop handoff for a portrait.
2. Build a reusable, non-destructive Photoshop layer-group template.
3. Get a first honest timing baseline for "setup," separate from retouching
   time — you'll compare against this on Day 09 and Day 29.

## Agenda

### 0:00–0:05 — Setup
Pick one RAW portrait from your own library — ideally a straightforward,
well-lit headshot/portrait (save trickier lighting for Day 05). Open it in
Lightroom.

### 0:05–0:20 — Lightroom base pass
Do only global adjustments, in this order:
1. White balance
2. Exposure
3. Contrast / tone curve basics (blacks, whites, highlights, shadows)
4. Any obvious lens correction (profile correction, chromatic aberration)

Do **not** spot-heal or locally brush anything yet — that's Photoshop's job
starting Day 02. This keeps the line between "global correction" (Lightroom)
and "detail retouching" (Photoshop) clean, which matters later when you're
syncing base edits across a 20-photo gallery.

Right-click the photo → **Edit In → Open as Smart Object in Photoshop**.
(Using "Open as Smart Object," not a flat "Edit In," is the point — it's
what keeps your Lightroom edits re-editable later without round-tripping.)

### 0:20–0:45 — Build your template layer structure
In Photoshop, with the image open as a Smart Object as your base layer,
create this layer group structure (empty for now — you'll fill groups 2-4
on Days 04, 06/07, and 11-12):

```
📁 05 Color Grade        (empty — Day 13)
📁 04 Details            (empty — Days 11-12: eyes/teeth/hair)
📁 03 Dodge & Burn        (empty — Days 06-07)
📁 02 Frequency Separation (empty — Days 04-05)
🖼 01 Base (Smart Object)
```

Use exactly this naming and stacking order every time — the numbering
keeps retouching steps in the correct visual order (you always want D&B
and detail work sitting *above* frequency separation, and color grade on
top of everything). Save this as a **Photoshop template file**
(`portrait-template.psd` or `.psdt`) somewhere you'll reuse it — you'll
turn the *creation* of this structure into an Action on Day 18, but for
now, do it by hand so the structure itself becomes familiar.

### 0:45–0:55 — Repeat for speed
Pick a second RAW photo. Repeat the entire process — Lightroom global pass,
open as Smart Object, build the same layer group structure — but this time,
time yourself. Don't rush recklessly; just note how long the *scaffold*
(not retouching) takes with no tutorial in front of you.

### 0:55–1:00 — Wrap-up
Write down (in this file or a notes app) your scaffold time from the second
pass. This is your Day 01 baseline — it should get faster by Day 09 once
frequency separation and D&B are in the mix and you're used to the rhythm.

## What today covered

- The clean handoff point between Lightroom (global correction) and
  Photoshop (detail retouching), and why "Open as Smart Object" matters.
- A standard, repeatable non-destructive layer-group structure you'll reuse
  and build on for the rest of the program:
  `01 Base → 02 Frequency Separation → 03 Dodge & Burn → 04 Details → 05 Color Grade`.
- A first real timing baseline for your setup ritual, separate from actual
  retouching time — useful context once speed drills start in Week 2.

**Carrying forward to Day 02:** you'll use this exact template as the
starting point for blemish-removal tool drills — no new setup needed,
just open the template and go straight to work.

---

You have completed DAY 1 of your 30 day training plan!
