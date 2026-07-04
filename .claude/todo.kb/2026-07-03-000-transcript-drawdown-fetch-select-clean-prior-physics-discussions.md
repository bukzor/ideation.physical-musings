---
managed-by: Skill(llm-subtask)
status: deferred
cost-benefit-sweh:
  timebox:
    '@value': 4
    rationale: fetch export + shortlist + tag/clean/annotate; bounded first pass, structure TBD
    confidence: tentative
  benefit-2w:
    '@value': 0.5
    rationale: explicitly deferred from the G.SYS discussion; value materializes when physics work resumes
    confidence: tentative
  cost-of-delay-2w:
    '@value': 0.1
    rationale: claude.ai history persists; low decay
    confidence: unsure
---

# Transcript drawdown: fetch, select, clean prior physics discussions

**Priority:** Medium
**Complexity:** Medium
**Context:** Deferred from the 2026-07-03 goals discussion (G.SYS). Tooling: `~/repo/github.com/bukzor/prototype.claude-export-cli`.

## Problem Statement

Prior LLM physics discussions exist ("more than a few") and are dual-purpose:

1. **Seed material** — they contain the musings (M.*) already partially developed.
2. **Regression corpus** — they contain the failure modes G.SYS must defeat
   (backsliding, sycophancy, subtle errors). A candidate system design can be
   evaluated against them: would it have caught/prevented these?

A known hazard recorded verbatim from the user: in those transcripts "I walk
the line between badgering the LLM to accept my claims and insisting they
don't backslide on well-litigated claims, and I can't tell which side of the
line I'm on." Selection/cleaning must preserve that ambiguity rather than
resolve it flatteringly — which side of the line each episode falls on is
itself data (Symmetric-error failure mode).

## Current Situation

Transcripts live in claude.ai history; `prototype.claude-export-cli` can fetch
them. Nothing imported yet. Repo is otherwise empty.

## Proposed Solution

Mini-sub-project, run when we return to it:

## Implementation Steps

- [ ] Verify `prototype.claude-export-cli` still works; fetch full export
- [ ] Skim + shortlist physics-relevant conversations (titles/first-lines pass)
- [ ] Select: tag each shortlisted transcript with musing labels (M.*) it touches
- [ ] Clean: strip noise, keep claims/arguments/corrections; preserve
      chronology of corrections (that IS the regression data)
- [ ] Annotate candidate failure-mode episodes (backslide / sycophancy /
      subtle-error / badgering-ambiguity) without adjudicating them yet
- [ ] Land results in repo under a dedicated directory (structure TBD by
      then-current conventions)

## Open Questions

- Where do cleaned transcripts live — `sources.kb/` (they are provenance) or a
  dedicated `transcripts/` area?
- Privacy: any transcripts to exclude from a public repo?
- How much cleaning is too much — when does "cleaning" become editing the
  evidence?

## Success Criteria

- [ ] Every physics-relevant prior conversation is fetched and tagged with M.* labels
- [ ] Failure-mode episodes are annotated and locatable
- [ ] Seed claims are extractable without re-reading raw exports

## Notes

Set aside deliberately on 2026-07-03; do not start without user go-ahead.
