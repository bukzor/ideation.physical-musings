---
requires:
  - Skill(llm-kb)
  - Skill(llm-discourse-graph)
depends:
  - Skill(llm-design-kb)
git-caution: personal
---

# ideation.physical-musings

Original physics musings (GR, cosmology, some QM) developed and
stress-tested in collaboration with LLMs -- plus the system that makes
such collaboration rigorous and durable. Public repo.

## Scopes

- `docs/dev/` -- meta scope: everything *about the system*. Design tower
  (`design/`), cross-cutting policy (`technical-policy.kb/`), environment
  facts (`background.kb/`), meta discourse (`claims.kb/`, `questions.kb/`,
  `sources.kb/` -- live-discussion provenance, not literature).
- repo root -- reserved for the physics discourse itself (goal G.CORPUS):
  per-musing scopes with their own collections (incl. `sources.kb/`),
  opened as musings open.
- `.claude/` -- session workflow (todo.kb, ideas.kb); not corpus content.

## Conventions

- Labels map to paths: prefix = collection, name = kebab-case filename.
  G. = design/020-goals.kb, M. = design/use-cases.kb,
  R. = design/030-requirements.kb, TP. = technical-policy.kb,
  C. = claims.kb, Q. = questions.kb, S. = sources.kb. Background
  entries are unprefixed (small, environmental, not part of the
  discourse).
  E.g. C.CAUSAL-FIRST = docs/dev/claims.kb/causal-structure-before-tensor-calculus.md.
  The `label:` frontmatter field is authoritative and grep-able. No
  separate "decisions" collection: process/scope decisions are claims
  (e.g. C.DG-DISCUSS-ONLY); binding rules for the eventual design are
  technical-policy (e.g. TP.DESIGN-FROM-SETTLED).
- Settlement (working convention, pending Q.SETTLE-AUTHORITY): either
  party proposes; the user ratifies. `ratified:` date in frontmatter
  marks settlement; absence = proposed. Grounds live in the node body
  (R.SETTLE-AUDIT). Reopening a ratified node requires something new --
  evidence, a flaw in prior reasoning, or a clarified misunderstanding.
