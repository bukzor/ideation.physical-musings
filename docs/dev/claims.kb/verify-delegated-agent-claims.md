---
status: asserted
sources:
  - ../sources.kb/assistant.md
---

A delegated subagent's final "done" summary is not self-verifying. This
session, a fork was asked to execute a mechanical filename-rename sweep
and reported a plausible, detailed completion summary -- while its own
usage stats showed zero tool calls; nothing was actually renamed.
Delegated work must be checked against ground truth (filesystem, `git
status`, a validator) before trusting the delegate's own report -- a
concrete instance of [symmetric-scrutiny] extended to tooling/agents,
not just human/LLM claims.

[symmetric-scrutiny]: ../design/030-requirements.kb/symmetric-scrutiny.md
