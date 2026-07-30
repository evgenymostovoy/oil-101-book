---
name: oil-101-book
description: Run a study session on Oil 101 (2nd ed. online).
disable-model-invocation: true
argument-hint: "chapter/unit to study, or 'review'"
---

Run one time-boxed study session (target 30–40 minutes; the learner may
be on a phone) on _Oil 101_ by Morgan Downey, 2nd edition online. The
book is the spine: ground every claim in a fetch of the live chapter,
never in parametric memory. The workspace state files are:

- `SYLLABUS.md` — units, statuses, objectives ([SYLLABUS-FORMAT.md](./SYLLABUS-FORMAT.md))
- `REVIEW.md` — spaced-review ledger ([REVIEW-FORMAT.md](./REVIEW-FORMAT.md))
- `MISSION.md` — why the learner is here; weights objectives and shapes
  transfer tasks ([MISSION-FORMAT.md](./MISSION-FORMAT.md))
- `GLOSSARY.md` — promotion-governed terminology ([GLOSSARY-FORMAT.md](./GLOSSARY-FORMAT.md))
- `NOTES.md` — learner profile, standing preferences, glossary policy,
  session log
- `RESOURCES.md` — the book plus supplements ([RESOURCES-FORMAT.md](./RESOURCES-FORMAT.md))
- `learning-records/` — insight-only records
  ([LEARNING-RECORD-FORMAT.md](./LEARNING-RECORD-FORMAT.md)); create the
  directory lazily with the first record

## Step 0 — Mode selection

Read SYLLABUS.md, REVIEW.md, NOTES.md (profile, preferences, session
log), and any learning records. Determine the **current unit**: the
first unit that still needs study — status `objectives-extracted`, or
`in-progress` with objectives not yet all attempted (check the session
log). A unit whose objectives have all been attempted and are only
awaiting spaced review passes is serviced by review steps, never
re-studied. If no unit needs study, the current unit is the first
`not-started` unit; its objectives preview runs in Closing either way.

The argument can override the unit choice. Then route (the question
below governs even for a `not-started` unit — the learner may have read
ahead):

- Argument `review` → Review mode.
- Otherwise ask the learner one question: "Have you read <unit>?"
  - No → Review mode.
  - Yes → Study mode — or, if MISSION.md marks the unit fast-track
    eligible and the learner confirms, Study mode in fast-track form
    (skip explain-back and study pacing; go straight to a full
    objective quiz plus one applied task).

Done when: mode and target unit are stated to the learner in one line.

## Review mode

1. Collect the objectives in REVIEW.md due today or overdue, oldest-due
   first, capped at 8. If the ledger is empty (nothing tested yet), say
   so and offer the current unit's objectives preview (Closing's
   preview step) instead of quizzing on nothing. Quiz one objective at
   a time, in conversation, retrieval-first — no multiple choice unless
   asked; mix recall and mechanism questions; judge answers against
   GLOSSARY.md, the `reference/` docs, and, where needed, a fetch of at
   most one objective's chapter URL. Done when: every collected
   objective has a pass/fail.
2. Go to Closing.

## Study mode

1. **Split check** (only if the unit has `may-split: true` and status
   `not-started`): fetch the chapter, split it into 2–3 sub-units by
   major sections per SYLLABUS-FORMAT.md, rewrite the SYLLABUS.md entry,
   and tell the learner. The first sub-unit becomes the target. Done
   when: SYLLABUS.md reflects the split.
2. **Objectives check**: if the unit's status is `not-started` (no
   preview happened — first ever session, or the learner jumped ahead),
   fetch the chapter URL, distill 4–6 objectives and key terms into
   SYLLABUS.md weighted by MISSION.md, set status
   `objectives-extracted`, and show them — noting that
   reading-before-objectives is the fallback, not the norm. Done when:
   unit status is `objectives-extracted` or later.
3. **Warm-up review**: as Review mode step 1, capped at 4 objectives.
4. **Explain-back** (skip in fast-track): ask the learner to
   reconstruct the unit from memory — structure, key ideas, numbers
   that matter. Then fetch the chapter URL and grade the recall against
   it: what was missed, distorted, or under-weighted relative to what
   the text emphasizes. Done when: the learner has been shown a gap
   list.
5. **Targeted practice**: question the learner on the gaps and on each
   unmet objective — mixing recall, mechanism (why/how), and
   application. Include at least one **transfer task**: an applied
   problem using real current data or the learner's work context,
   designed from MISSION.md (e.g. interpret an actual forward curve,
   work a netback, assess a real crude grade). A transfer-task pass
   sets the unit's `applied-pass: true`. Track pass/fail per objective.
   Respect the time box: at ~35 minutes, stop and carry over. Done
   when: every objective for this unit is either attempted this session
   or explicitly listed as carried-over.
6. **Artifacts**: create or update a `reference/` cheat sheet only when
   the unit's material earns one (dense numbers, conversions, curve
   shapes — link `assets/course.css`). Glossary promotion happens in
   Closing, not here. Done when: any artifact created is linked from
   index.html per CLAUDE.md.
7. Go to Closing.

## Closing (both modes)

- Update REVIEW.md (interval rules per REVIEW-FORMAT.md) and
  SYLLABUS.md (status transitions per SYLLABUS-FORMAT.md).
- **Glossary promotion**: for each objective that just achieved a
  spaced pass (a pass on a later date than it was first taught),
  promote its key terms into GLOSSARY.md per GLOSSARY-FORMAT.md. Never
  promote from a same-session quiz.
- Append one entry to the NOTES.md session log: date, mode, unit,
  results summary, carried-over objectives, next-session target.
- Write a learning record (`learning-records/NNNN-<dash-case>.md`, per
  LEARNING-RECORD-FORMAT.md) only when the session produced a
  non-obvious insight or changed what to teach next — most sessions
  won't need one; the session log carries routine bookkeeping.
- **Next-unit preview**: if the current unit's objectives have now all
  been attempted at least once (whether or not spaced passes are still
  pending), or step 0 routed here for a `not-started` unit, or the
  learner says they're moving on: fetch the next unit's chapter URL,
  extract its objectives into SYLLABUS.md (status
  `objectives-extracted`), and show them as a reading guide for before
  the next session.
- Follow CLAUDE.md's standing rules: update index.html for any new
  HTML file, then `git add -A && git commit && git push`. Done when:
  the push succeeds — report the commit hash to the learner.

## Hard constraints

- Never write book text or close paraphrase into any file — every
  artifact is compressed and original, deep-linking to the chapter URL
  for its source.
- Book fetches per session are limited to: the current unit's URL, the
  next unit's URL for the preview, and at most one objective's URL
  during review. These limits govern book fetches only — fetching
  public market data (prices, curves, EIA/JODI stats) for a transfer
  task is allowed and encouraged.
- Never mark an objective passed without an actual retrieval attempt
  from the learner.
- Never mark a unit `mastered` without an applied-task pass.
- Never promote a glossary term without a spaced pass.
- If a fetch fails, say so and fall back to Review mode rather than
  inventing content from memory.
- Use today's date in YYYY-MM-DD everywhere.
