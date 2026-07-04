---
why:
  - ../020-goals.kb/develop-rigorous-llm-discussion-system.md
  - ../020-goals.kb/build-internalized-intuition.md
---

A generic methodology for co-writing anything that must be at once
extremely rigorous (state-of-the-art methodology) and fully understood
by the user: an implementation in the user's intuition-language (see
[python-schematic-twin]) plus the newfangled-tech implementation, plus a
check that they agree -- the formal-methods pattern of *refinement*.
Serves double duty: builds the user's intuition, and lets the user
discuss and give concrete feedback on developments in unfamiliar
environments. Realization grade is per-case and JIT: proof-flavored
(equivalence proof, ITP-native) where cheap, test-flavored
(property-based testing) where proof is dear, bare assertion where
neither pays yet (per [progressive-elaboration]).

[progressive-elaboration]: progressive-elaboration.md
[python-schematic-twin]: python-schematic-twin.md
