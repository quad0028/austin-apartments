# Working rules for this fleet

Ross Quade's apartment-locator sites: austinapartments.com, sanmarcosapartments,
newbraunfelsapartments, kyleapartments, budaapartments. Each site's own repo
carries its CLAUDE.md and TEMPLATE.md; those govern the code. This file
governs how the session itself works.

## Model routing (standing rule, set by Ross on 2026-09-12)

The session model (Fable) stays in the architect seat: design, review,
anything a renter reads, root-cause work, and the final word on what ships.

Mechanical work goes to subagents on cheaper models, pinned per task:

- Opus 5 for implementation that needs judgment across files: porting a
  change to the sibling repos, a refactor with a clear spec, a fix whose
  cause is already known.
- Sonnet for routine, well-specified work: running walls and sweeps,
  applying a scripted patch to five repos, syntax and gate checks, log
  reading, data counts, transcript searches.
- The built-in Explore agent for locating code.

Never hand a subagent copy that a renter will read, a decision about
accuracy, or a review. Verify a subagent's result before reporting it.

## Standing directives that never change

- Never cross-reference sibling sites.
- Every fact, price, name and phone on a site must be real. No invented
  content.
- The QA wall runs before anything ships; re-gate only what changed.
- Community pages are created one at a time from a supplied URL, never
  generated from the directory.
- Street View imagery is never stored or cached. Pano IDs may be.
- Ross says "merge"; only then merge.
