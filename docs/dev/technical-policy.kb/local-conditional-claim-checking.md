---
label: TP.LOCAL-CHECK
force: must
why:
  - ../design/030-requirements.kb/checked-claims.md
---

Any claim-checker must verify deductions as conditionals in their own
local context (premises |- conclusion); epistemic status (contested,
believed, refuted) stays outside the logic as metadata -- the corpus
will contain mutually contradictory claims, and a global assertion of
all of them lets one contradiction prove anything (ex falso quodlibet).
Grounds: `C.LOCAL-CHECK`.
