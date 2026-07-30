# SYLLABUS.md Format

`SYLLABUS.md` at the workspace root is the course map: one unit per book
chapter/appendix (or sub-unit after a split), grouped under the book's part
headings. The book's chapter order drives sequencing — units are never
invented or reordered.

## Header

The file starts with the ToC URL, the book edition, and the generation date
(YYYY-MM-DD), so a future session can detect edition changes by re-fetching
the ToC and diffing.

## Example entry

```md
### 02 — A Crude Oil Assay
- url: https://oil101.morgandowney.com/chapters/crude-oil-assay
- duration: 18:41
- may-split: false
- status: objectives-extracted
- applied-pass: false
- objectives:
  - 02-api-gravity: State what API gravity measures and place light/medium/heavy cutoffs on the scale · key-terms: API gravity, light/heavy crude
  - 02-sweet-sour: Explain the sulfur cutoff between sweet and sour crude and why refiners price it · key-terms: sweet crude, sour crude
- records:
  - [LR-0002](learning-records/0002-assay-baseline.md)
```

## Fields

- `url` — the chapter's canonical page. Sub-units created by a split share
  the parent chapter's URL.
- `duration` — the listed reading duration from the ToC (`mm:ss`), or
  `not listed`.
- `may-split` — `true` when the listed duration exceeds ~20 minutes. At
  first contact with such a unit (during the objectives pass, when the
  chapter is being fetched anyway), the skill splits it into 2–3 sub-units
  named after the chapter's major sections (e.g. `06a — Exploration`,
  `06b — Drilling and Completion`), each with the full field set, replacing
  the single entry. After a split, each sub-unit has `may-split: false`.
- `status` — one of:
  - `not-started` — no objectives extracted yet.
  - `objectives-extracted` — objectives distilled from the fetched chapter
    into the entry; unit not yet studied.
  - `in-progress` — at least one study session has touched the unit.
  - `mastered` — see transition rules.
- `applied-pass` — `true` once the unit has at least one passed
  transfer/application task.
- `objectives` — empty at setup. Filled by the skill's objectives pass:
  4–6 objectives distilled from the live chapter, weighted by MISSION.md.
  Each line is
  `<unit>-<short-slug>: <objective text> · key-terms: <term>, <term>`;
  the id is the same id used in REVIEW.md, and the key terms are the
  candidate GLOSSARY.md entries promoted when the objective earns a
  spaced pass.
- `records` — links to related learning records, relative to the
  workspace root where SYLLABUS.md lives (e.g.
  `learning-records/0002-assay-baseline.md`); empty until one exists.

## Transition rules

- `not-started → objectives-extracted`: requires a non-empty `objectives`
  list distilled from a fetch of the chapter URL.
- `objectives-extracted → in-progress`: a study session attempted at least
  one of the unit's objectives.
- `in-progress → mastered`: requires BOTH (a) every objective in the entry
  has a **spaced pass** recorded in REVIEW.md (canonical definition:
  REVIEW-FORMAT.md), and (b) `applied-pass: true`.
- A failed spaced review never demotes `status`; it only resets that
  objective's interval in REVIEW.md.
