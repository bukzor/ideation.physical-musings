---
why:
  - ../020-goals.kb/develop-rigorous-llm-discussion-system.md
  - ../020-goals.kb/learn-lean-or-comparable-formal-system.md
---

Claims need a machine-checkable representation. The checker always
verifies the *discourse structure* (does this arrow follow from these
premises); any node may additionally elaborate, per
[progressive-elaboration], down to a level of detail where sign errors
and index slips become mechanically visible -- this is
[anti-subtle-error]'s intended mechanism. Interior semantics are as
nebulous or as rigorous as elaboration has reached. See
[technical-policy.kb/local-conditional-claim-checking] for why the check
must be local rather than global.

[anti-subtle-error]: anti-subtle-error.md
[progressive-elaboration]: progressive-elaboration.md
[technical-policy.kb/local-conditional-claim-checking]: ../../technical-policy.kb/local-conditional-claim-checking.md
