# Oil 101 — Learning Workspace

## What this is

This is a structured study workspace for working through _Oil 101_ by
Morgan Downey (2nd edition, free online at
https://oil101.morgandowney.com/chapters), driven by the `oil-101-book`
skill in `.claude/skills/oil-101-book/`. The book is the spine:
`SYLLABUS.md` maps its chapters to units, `REVIEW.md` schedules spaced
retrieval, and all artifacts deep-link to chapter URLs instead of
storing book text.

## Standing rules

These apply to every session in this repo, whether or not the skill is
invoked.

### 1. Always commit and push at the end of every session

At the end of EVERY session, commit all changes and push to GitHub
**without being asked**. Never leave work unpushed. The user accesses
this material from other devices (including their phone), so unpushed
work is effectively lost to them.

### 2. Keep index.html up to date

`index.html` at the repo root is the homepage. Whenever a new file is
created in `reference/` or `lessons/`, add a link to it in
`index.html`, **newest first**, using relative links (e.g.
`reference/<filename>.html`) — they work when opened locally and
resolve on GitHub Pages at
`https://evgenymostovoy.github.io/oil-101-book/…`.

### 3. The user is a learner, not a developer

Explain all technical matters (git, GitHub, files, errors) in plain
language. Never assume programming knowledge. Check with the user
before doing anything irreversible.
