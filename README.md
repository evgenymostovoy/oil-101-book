# Oil 101 — Study Workspace

A personal study workspace for working through [_Oil 101_ by Morgan
Downey](https://oil101.morgandowney.com/chapters) (2nd edition, free
online) — from the wellsite to the market.

**📖 Study site:** https://evgenymostovoy.github.io/oil-101-book/

## How it works

Study sessions run in [Claude Code](https://claude.com/claude-code)
via the `/oil-101-book` skill (in `.claude/skills/oil-101-book/`):
short, time-boxed sessions of retrieval practice, explain-back, and
applied tasks grounded in the live book text and real market data.
Spaced review keeps everything at instant recall.

## What's in here

| File / folder | Purpose |
|---|---|
| `SYLLABUS.md` | Course map — one unit per book chapter, with objectives and status |
| `REVIEW.md` | Spaced-review ledger — what's due for retrieval, when |
| `MISSION.md` | Why this course: commercial fluency + independent market view |
| `GLOSSARY.md` | Canonical terminology, earned through spaced recall |
| `NOTES.md` | Learner profile, preferences, session log |
| `RESOURCES.md` | The book plus vetted supplements (EIA, JODI, …) |
| `reference/` | Compressed cheat sheets (published on the study site) |
| `learning-records/` | Non-obvious insights that steer future sessions |

No book text is stored here — every artifact links back to the
chapter it came from.

## Workflow note

Cloud sessions push to a `claude/...` side branch and merge to `main`
by pull request; the study site serves `main`.
