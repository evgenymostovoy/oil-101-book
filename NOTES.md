# Notes

Working notes and learner preferences for this workspace. Durable facts
and preferences live in the top sections; per-session events go in the
session log at the bottom.

## Learner profile

- Drilling & completion engineer. D&C is professional ground; everything
  else in the book — geology, reservoir, production, refining, products,
  markets, trading — is new territory and gets full treatment.
- Work context (for transfer-task design): ~15 years of D&C practice on
  the Norwegian Continental Shelf; current company operates on the NCS
  plus two deepwater pre-salt projects in Brazil. Natural anchors for
  applied tasks: Brent as the home benchmark, NCS crude grades (e.g.
  Johan Sverdrup, Ekofisk), Brazilian pre-salt grades and their export
  flows, North Sea and Santos/Campos logistics.
- Goals, success bar, and scope boundaries: MISSION.md. This file owns
  how sessions run.

## Standing preferences

- **Time box.** Study sessions are **25–30 minutes** for now (set
  2026-07-30). Checkpoint at ~25 minutes: stop, carry over what's
  left. Sessions may run from a phone via cloud sessions.
- **Units.** Market-standard first: bbl, $/bbl, Mbpd, API gravity, with
  SI/metric equivalents as parenthetical notes where useful. (Deliberate
  contrast with the SI-first sibling engineering workspace.)
- **Fast-track.** Decided unit by unit — the learner flags a unit as
  known ground when it comes up; never assume eligibility from the
  chapter title.
- **Retrieval in conversation.** All quizzing happens in chat, no
  interactive HTML widgets — must work from a phone.
- **Transfer tasks.** Draw from real, current market data (public
  prices, forward curves, EIA/JODI statistics) and from the learner's
  work context as a D&C engineer.

## Glossary policy

GLOSSARY.md (workspace root) is canonical oil markets & industry
terminology; adhere to its terms in every artifact. This section is the
single source of truth for *when to promote*: a term is promoted into
GLOSSARY.md only when its objective achieves a spaced pass (canonical
definition: REVIEW-FORMAT.md), never from a same-session quiz.
Candidate terms live on each objective's `key-terms` list in
SYLLABUS.md.

Seeding exception: vocabulary that is practice-known from the
learner's D&C profession (per the learner profile above) may be seeded
directly into GLOSSARY.md when it first comes up in a unit, without a
spaced pass — it is already demonstrably known from daily use. Seeding
applies only to practice-known D&C vocabulary, never to newly taught
market, refining, or trading terms; those always earn their way in via
spaced pass.

## Session log

One entry per session: date, mode, unit, results summary, carried-over
objectives, next-session target. To keep this log scrollable, when a
book Part completes, collapse that Part's per-session entries into one
summary entry (units covered, date range, anything still carried).

- **2026-07-30 — Study (attempted) — 01 A Brief History of Oil.**
  Learner confirmed the chapter was read, but the session environment's
  network policy blocked all fetches of oil101.morgandowney.com (and
  archive.org), so no objectives could be extracted and no grounded
  quizzing was possible. No objectives attempted; nothing carried over
  beyond the whole unit. Fix before next session: allow the domain
  `oil101.morgandowney.com` in the Claude Code environment's network
  settings. Next-session target: Unit 01, full study session
  (objectives extraction → explain-back → practice).
- **2026-07-30 (later) — Maintenance — skill audit.** Network access
  restored (learner allowed the book site and eia.gov); Unit 01
  objectives extracted with key terms. Audited the workspace against
  skill-writing conventions and fixed: fetch-failure dead end (added
  terminal fallback), unsatisfiable fast-track condition, key-terms
  field added to SYLLABUS format, broken example link, spaced-pass
  definition made deterministic and glossary promotion reordered
  before ledger updates, unit-preview wording for not-started units,
  mastery bar tightened to spaced passes, glossary policy consolidated
  to a single source (this file), inherited fitness examples replaced
  with oil-domain ones, dead CSS pruned. Note: cloud sessions push to
  a `claude/...` branch — merge into `main` for the phone-visible
  site to update. Next-session target: Unit 01 study
  (explain-back → practice).
