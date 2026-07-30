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

Expanding intervals, in days: **1 → 3 → 7 → 21**.

- First pass: next-due = last-tested + 1 day.
- Each consecutive pass moves one step right (3, then 7, then 21 days).
- After the 21-day step, further passes stay at 21-day intervals.
- Any fail resets the objective to the start: next-due =
  last-tested + 1 day.
- All dates are YYYY-MM-DD.

## Worked example

```
- 02-api-gravity · last-tested: 2026-08-04 · result: pass · next-due: 2026-08-07
```

This objective was first tested (pass) on 2026-08-03 with next-due
2026-08-04; it passed again on 2026-08-04 — its second consecutive pass —
so the interval advanced to 3 days and next-due is 2026-08-07. If the
2026-08-07 attempt fails, the line becomes
`last-tested: 2026-08-07 · result: fail · next-due: 2026-08-08`.
