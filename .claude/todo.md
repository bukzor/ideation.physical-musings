---
managed-by: Skill(llm-subtask)
cost-benefit-sweh:
  timebox:
    '@value': 0.5
    rationale: 'residual is a decision: pick the concrete next action (pilot all-entropy-is-shannon-entropy, or resolve which-formal-checking-substrate/is-cas-verification-feasible) + ratify/veto build-internalized-intuition'
    confidence: unsure
  benefit-2w:
    '@value': 0.5
    rationale: unblocks the project's direction
    confidence: tentative
  cost-of-delay-2w:
    '@value': 0.3
    rationale: context from the 2026-07-03 goals discussion is hot; decays over weeks
    confidence: tentative
---

- [~] Goals discussion (2026-07-03): shared understanding reached and
      instantiated as `docs/dev/` design tower + discourse graph.
      Remaining from the original ask: "choose what to do" -- pick a
      concrete next action (pilot a musing, e.g.
      [all-entropy-is-shannon-entropy] which needs no tensor-calculus
      on-ramp; or resolve
      [which-formal-checking-substrate]/[is-cas-verification-feasible]).
      [build-internalized-intuition] ratified 2026-07-03.
- [x] Filename rename sweep: fixed. Root cause of the earlier "done but
      not done" confusion -- the sweep had actually already landed in
      the sole commit (`8879c47`); a later uncommitted step reverted
      every file back to its terse name. Undone (`git mv` back to the
      verbose names) and the stale cross-references fixed; validated
      clean via `llm.kb-validate` (71 files, 0 errors) and a full `../`
      path-resolution check.

## Later

We haven't (yet) decided where to place these in the task queue.
Please read and consider slotting them.

- [ ] [todo.kb/2026-07-03-000-transcript-drawdown-fetch-select-clean-prior-physics-discussions.md](todo.kb/2026-07-03-000-transcript-drawdown-fetch-select-clean-prior-physics-discussions.md)

[all-entropy-is-shannon-entropy]: ../docs/dev/design/use-cases.kb/all-entropy-is-shannon-entropy.md
[which-formal-checking-substrate]: ../docs/dev/questions.kb/which-formal-checking-substrate.md
[is-cas-verification-feasible]: ../docs/dev/questions.kb/is-cas-verification-feasible.md
[build-internalized-intuition]: ../docs/dev/design/020-goals.kb/build-internalized-intuition.md
