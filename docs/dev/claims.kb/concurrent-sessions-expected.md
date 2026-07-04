---
status: asserted
sources:
  - ../sources.kb/user.md
---

Some concurrent agent/session activity is expected. This is why the
user's designs emphasize small all-at-once (write-once) files over
larger files that get edited: merge-safety by construction. Resolves
[will-multiple-agents-work-concurrently]; grounds the proposed
[merge-safe-corpus-files].

[merge-safe-corpus-files]: ../design/030-requirements.kb/merge-safe-corpus-files.md
[will-multiple-agents-work-concurrently]: ../questions.kb/will-multiple-agents-work-concurrently.md
