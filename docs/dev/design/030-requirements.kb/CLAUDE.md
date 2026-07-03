# Requirements

`R.*`: verifiable conditions for achieving `G.SYS`. Two origins, both
valid:

- **desiderata** -- stated directly by the user (e.g. R.PROG-ELAB)
- **failure-mode negations** -- a `F.*` failure mode, reworded as its
  negation (e.g. F.AMNESIA -> R.ANTI-AMNESIA). Keep the negation
  explicit in the body for traceability; don't retain a separate
  failure-modes collection.

`ratified:` marks a requirement as settled (per R.SETTLE-AUDIT itself);
absence means asserted but not yet through the ratification ritual.
Goals belong in `../020-goals.kb/`; binding rules for the eventual
design belong in `../../technical-policy.kb/` -- not here.
