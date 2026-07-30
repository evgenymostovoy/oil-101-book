# Notes

Working notes and learner preferences for this workspace. Durable facts
and preferences live in the top sections; per-session events go in the
session log at the bottom.

## Learner profile

- Drilling & completion engineer. D&C is professional ground; everything
  else in the book — geology, reservoir, production, refining, products,
  markets, trading — is new territory and gets full treatment.
- Dual goal, equally weighted (MISSION.md): commercial fluency at work
  and independent macro understanding of the oil market, building
  optionality toward commercial/markets-adjacent roles.
- No personal trading positions — transfer tasks target understanding
  and work-relevant decisions, never trade calls.
- Target is storage strength — objectives at instant recall on spaced
  retrieval. A same-session quiz score is evidence of fluency only;
  "known" requires a correct spaced retrieval on a later day.
- Sessions are 30–40 minutes, sometimes from a phone via cloud sessions.

## Standing preferences

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
single source of truth for promotion: a term is promoted into
GLOSSARY.md only when its objective achieves a **spaced retrieval
pass** — a pass on a later date than the objective's previous
REVIEW.md entry, never from a same-session quiz. Candidate terms live
on each objective's `key-terms` list in SYLLABUS.md.

## Session log

One entry per session: date, mode, unit, results summary, carried-over
objectives, next-session target.

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
