---
label: R.DUAL-REP
why:
  - ../020-goals.kb/develop-rigorous-llm-discussion-system.md
---

A conventional-and-definitely-correct implementation, plus an
unconventional-highly-ergonomic implementation, plus a check that they
agree -- the formal-methods pattern of *refinement*. Realization grade
is per-case and JIT: proof-flavored (equivalence proof, ITP-native) where
cheap, test-flavored (property-based testing) where proof is dear, bare
assertion where neither pays yet (per `R.PROG-ELAB`).
