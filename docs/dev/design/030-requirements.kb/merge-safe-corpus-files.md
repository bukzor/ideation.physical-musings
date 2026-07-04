---
why:
  - ../020-goals.kb/develop-rigorous-llm-discussion-system.md
---

Corpus files stay small, write-once ("all-at-once"), and git-mergeable,
so concurrent agents/sessions compose without conflict. Grounded in
[concurrent-sessions-expected]; the existing file-per-node convention is
the current mechanism. The shape of the concurrency (subagents, parallel
sessions, clones) is deliberately unspecified -- the file convention is
safe under all of them.

[concurrent-sessions-expected]: ../../claims.kb/concurrent-sessions-expected.md
