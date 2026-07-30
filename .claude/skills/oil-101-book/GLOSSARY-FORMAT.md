# GLOSSARY.md Format

`GLOSSARY.md` is the canonical language for this teaching workspace. All artifacts, exercises, and learning records should adhere to its terminology. Building it is itself part of learning: compressing a concept into a tight definition is evidence the user understands it.

## Structure

```md
# {Topic} Glossary

{One or two sentence description of the topic this glossary covers.}

## Terms

**Spare capacity**:
Production that can be brought online quickly and sustained, held idle as a buffer — whoever controls it sets the marginal price.
_Avoid_: Idle capacity, headroom

**Backwardation**:
A forward curve with near-dated contracts priced above later-dated ones, signalling tight prompt supply.
_Avoid_: Inverted curve, downward-sloping market

**Sweet crude**:
Crude oil low enough in sulfur to need less processing — the "sweet/sour" line is a quality and price boundary.
_Avoid_: Low-sulfur oil, clean crude
```

## Rules

- **Promotion is governed by the workspace glossary policy** (NOTES.md, "Glossary policy", the single source of truth): a term enters only when its objective has a spaced retrieval pass in REVIEW.md. The glossary is a record of compressed knowledge, not a dictionary the user reads to learn.
- **Be opinionated.** When several words exist for the same concept, pick the best one and list the rest as aliases to avoid. This is how language compresses.
- **Keep definitions tight.** One or two sentences. Define what the term IS, not what it does or how to do it.
- **Use the glossary's own terms inside definitions.** Once a term is in the glossary, prefer it everywhere — including inside other definitions. This is what makes complex terms easier to grasp later.
- **Group under subheadings** when natural clusters emerge (e.g. `## Anatomy`, `## Programming`). A flat list is fine when terms cohere.
- **Flag ambiguities explicitly.** If a term is used loosely in the wider field, note the resolution: "In this workspace, 'set' always means a working set — warm-ups are tracked separately."
- **Revise as understanding deepens.** A definition the user wrote in week one may be wrong by week six. Update in place; do not leave stale entries.
