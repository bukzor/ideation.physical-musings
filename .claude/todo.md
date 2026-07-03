---
managed-by: Skill(llm-subtask)
---

- [~] Goals discussion (2026-07-03): shared understanding reached and
      instantiated as `docs/dev/` design tower + discourse graph.
      Remaining from the original ask: "choose what to do" -- pick a
      concrete next action (pilot a musing, e.g. M.ENTROPY-ONE which
      needs no tensor-calculus on-ramp; or resolve
      `Q.FORMAL-SUBSTRATE`/`Q.CAS-CAN`). One proposed goal,
      `G.INTUIT`, awaits ratify/veto.
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
