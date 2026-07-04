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
  (`design/`), cross-cutting policy (`technical-policy.kb/`),
  environment facts (`background.kb/`), meta discourse (`claims.kb/`,
  `questions.kb/`, `sources.kb/` -- live-discussion provenance, not
  literature).
- repo root -- reserved for the physics discourse itself (goal
  G.CORPUS): per-musing scopes with their own collections (incl.
  `sources.kb/`), opened as musings open.
- `.claude/` -- session workflow (todo.kb, ideas.kb); not corpus
  content.

## Conventions

- Filenames are the identifier: kebab-case, descriptive enough that `ls`
  is itself a form of discovery. Cross-references are relative-path
  markdown links; display text is the target's filename stem, with the
  parent collection dir prepended only when a stem collides across
  collections (currently the three claims.kb entries that pair with a
  same-named technical-policy.kb counterpart:
  causal-structure-before-tensor-calculus, design-from-settled,
  local-conditional-claim-checking). No separate "decisions" collection:
  process/scope decisions are claims (e.g.
  [discourse-graph-scoped-to-discussion]); binding rules for the
  eventual design are technical-policy (e.g.
  [technical-policy.kb/design-from-settled]).
- Settlement ([settlement-authority-convention]): either party proposes;
  the user ratifies. `ratified:` date in frontmatter marks settlement;
  absence = proposed. Grounds live in the node body
  ([settlement-audit-trail]). Reopening a ratified node requires
  something new -- evidence, a flaw in prior reasoning, or a clarified
  misunderstanding.

[discourse-graph-scoped-to-discussion]: docs/dev/claims.kb/discourse-graph-scoped-to-discussion.md
[technical-policy.kb/design-from-settled]: docs/dev/technical-policy.kb/design-from-settled.md
[settlement-authority-convention]: docs/dev/claims.kb/settlement-authority-convention.md
[settlement-audit-trail]: docs/dev/design/030-requirements.kb/settlement-audit-trail.md
