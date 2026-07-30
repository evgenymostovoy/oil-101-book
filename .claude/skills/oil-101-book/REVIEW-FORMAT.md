# REVIEW.md Format

`REVIEW.md` at the workspace root is the spaced-review ledger — the
single normative source for what is due when. Sessions read what is due;
they do not improvise scheduling.

## Entry format

One line per tested objective:

```
- <objective-id> · last-tested: YYYY-MM-DD · result: pass|fail · next-due: YYYY-MM-DD
```

- `objective-id` — unit number plus short slug, identical to the id in
  the unit's SYLLABUS.md `objectives` list (e.g. `02-api-gravity`).
- `last-tested` — the date of the most recent retrieval attempt.
- `result` — the outcome of that attempt.
- `next-due` — `last-tested` plus the current interval.

An objective enters the ledger the first time it is actually tested
(a real retrieval attempt by the learner), never at extraction time.

## Interval rules

Expanding intervals, in days: **1 → 3 → 7 → 21 → 60 → 120**.

- First pass: next-due = last-tested + 1 day.
- Each consecutive pass moves one step right (3, 7, 21, 60, then 120
  days).
- After the 120-day step, further passes stay at 120-day intervals.
- Any fail resets the objective to the start: next-due =
  last-tested + 1 day.
- All dates are YYYY-MM-DD.
- The governing principle: **a pass advances one step right from the
  gap just demonstrated**. The objective's current gap is always
  derivable from its own line (`next-due − last-tested`); no history
  beyond the line itself is needed. This also settles the post-fail
  case: a fail schedules a 1-day gap, so the pass that clears it
  demonstrated 1-day retention and advances to 3 days — the recovery
  ladder is identical to the initial one.

## Spaced pass (canonical definition)

A **spaced pass** is a pass recorded on a later date than the
objective's previous ledger entry. Same-session results are never
spaced passes. This definition is the single source of truth — it
governs glossary promotion (NOTES.md, "Glossary policy") and the
`mastered` transition (SYLLABUS-FORMAT.md).

## Worked example

```
- 02-api-gravity · last-tested: 2026-08-04 · result: pass · next-due: 2026-08-07
```

This objective was first tested (pass) on 2026-08-03 with next-due
2026-08-04; it passed again on 2026-08-04 — its second consecutive pass —
so the interval advanced to 3 days and next-due is 2026-08-07. If the
2026-08-07 attempt fails, the line becomes
`last-tested: 2026-08-07 · result: fail · next-due: 2026-08-08`.
