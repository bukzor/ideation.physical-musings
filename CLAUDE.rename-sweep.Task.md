# Task: finish the docs/dev/ filename rename sweep

- [ ] Fix every stale cross-reference in the table below, re-validate,
      re-grep for leftovers, then delete this file.

Context is long this session; this file is a self-contained spec so the
remaining mechanical work can be finished (by me, a fresh agent, or a
fork) without replaying the conversation. Delete this file once done.

## Why

Filenames must not be terse -- `ls`/`grep -l` is the primary discovery
mechanism (per `Skill(llm-kb)`'s own Naming section and
`filename-discipline` self-audit, which already said this; the initial
pass over-terse'd goal filenames by mistake). User also asked to drop
the `025-` numeric prefix from `use-cases.kb/` since it's an auxiliary
collection, not a rung in the why/how tower (nothing's `why:` points at
it).

**Caution:** a forked agent was asked to do this entire sweep earlier
and reported a plausible-sounding "done" summary while making **zero
tool calls** (confirmed via the fork's own usage stats: `tool_uses: 0`).
It hallucinated. Verify every claim below against the filesystem
(`ls`, `grep`) -- do not trust a prior "done" report, including this
file's own "DONE" markers, without spot-checking.

## Status: renames -- DONE (verified via `ls` after execution)

All `mv` operations below were executed and confirmed present on disk
as of this writing:

- `design/025-use-cases.kb/` -> `design/use-cases.kb/`
- `design/025-use-cases.jsonschema.yaml` -> `design/use-cases.jsonschema.yaml`
- `design/use-cases.kb/cosmo-bc.kb/` -> `design/use-cases.kb/cosmological-boundary-conditions.kb/`
- `design/020-goals.kb/`: dis->discuss-gr-cosmology-and-qm, sys->develop-rigorous-llm-discussion-system,
  proofxp->learn-proof-and-type-theory, formalxp->learn-lean-or-comparable-formal-system,
  wf->develop-workflow-skills, contimp->continuously-improve-ergonomics,
  physxp->learn-the-physics-and-math-content, corpus->produce-settled-knowledge-corpus,
  joy->preserve-speed-of-thought-enjoyment, intuit->build-internalized-intuition
- `design/use-cases.kb/`: cosmo-bc->cosmological-boundary-conditions, horizon-sym->horizon-symmetries,
  ds-observer->de-sitter-horizon-observer-dependence, alice-bob->alice-bob-schwarzschild-reconciliation,
  entropy-one->all-entropy-is-shannon-entropy, entropy-life->entropy-and-origins-of-life, etc->unenumerated-further-musings
- `design/use-cases.kb/cosmological-boundary-conditions.kb/`: null-bang->null-surface-big-bang,
  cpt-bang->cpt-mirror-as-big-bang, cpt-bh->cpt-mirror-as-black-hole,
  cpt-end->cpt-mirror-at-conformal-end-of-time, cavity->bounded-wave-function-resonant-cavity
- `design/030-requirements.kb/`: prog-elab->progressive-elaboration, rep-play->representation-play,
  dual-rep->dual-representation-refinement, py-grok->python-schematic-twin,
  calc-light->calculation-light-by-default, cite-jit->cite-just-in-time,
  settle-audit->settlement-audit-trail, sys-healthy->healthy-invariant-not-milestone
  (checked-claims, anti-amnesia, anti-sycophancy, anti-subtle-error, symmetric-scrutiny: kept as-is)
- `technical-policy.kb/`: local-check->local-conditional-claim-checking,
  causal-first->causal-structure-before-tensor-calculus (design-from-settled: kept)
- `claims.kb/`: scaffold-ok->discussion-scaffolding-non-binding,
  badger-line->badger-vs-backslide-indistinguishable,
  causal-first->causal-structure-before-tensor-calculus,
  local-check->local-conditional-claim-checking, refute-is-win->precise-refutation-is-success,
  dg-discuss-only->discourse-graph-scoped-to-discussion,
  adv-discuss-only->adversarial-review-scoped-to-discussion,
  turok-labels->turok-paper-citation-labels, memory-profile->user-memory-decay-profile,
  public-audience->repo-is-public-no-privacy-concern, cadence->session-cadence
  (design-from-settled: kept)
- `questions.kb/`: sys-design->what-is-the-sys-design, formal-substrate->which-formal-checking-substrate,
  cas-can->is-cas-verification-feasible, cas-should->should-we-use-cas,
  settle-authority->who-ratifies-settled-claims, lit-loop->what-is-the-literature-interface,
  model-diversity->should-we-cross-check-other-llms, concurrency->will-multiple-agents-work-concurrently,
  scale->expected-corpus-scale, type-bg->user-type-theory-background,
  learn-style->project-driven-or-course-driven-learning,
  baseline->should-we-mine-transcripts-for-a-baseline, turok-dup->why-was-turok-labeled-twice,
  privacy->is-the-repo-public, audience->who-is-the-audience, cadence->what-is-the-session-cadence
- `sources.kb/` (user.md, assistant.md) and `design/010-mission.kb/mission.md`: kept as-is

## Remaining: fix these exact stale references

Found via `grep -rn` across the whole tree after the renames above (this
list is believed exhaustive as of writing, but re-grep before trusting
it -- see caution note). Each is a frontmatter path or a prose mention
that still names the pre-rename filename/path.

| File | Line(s) | Old value | New value |
|---|---|---|---|
| `docs/dev/design/CLAUDE.md` | 11 | `` `025-use-cases.kb/` is a local layer insertion between goals and requirements `` | reword: it's an auxiliary collection (unnumbered, not a why/how tower rung -- nothing's `why:` points at it), anchored near goals. Also fix the path itself: `use-cases.kb/` |
| `docs/dev/design/020-goals.kb/discuss-gr-cosmology-and-qm.md` | 8 | `` `025-use-cases.kb/` `` | `` `use-cases.kb/` `` |
| `docs/dev/design/030-requirements.kb/checked-claims.md` | 4-5 | `../020-goals.kb/sys.md`, `../020-goals.kb/formalxp.md` | `../020-goals.kb/develop-rigorous-llm-discussion-system.md`, `../020-goals.kb/learn-lean-or-comparable-formal-system.md` |
| `.../anti-amnesia.md` | 4 | `../020-goals.kb/sys.md` | `../020-goals.kb/develop-rigorous-llm-discussion-system.md` |
| `.../anti-sycophancy.md` | 4 | same | same |
| `.../anti-subtle-error.md` | 4 | same | same |
| `.../symmetric-scrutiny.md` | 4 | same | same |
| `.../progressive-elaboration.md` | 4-5 | `sys.md`, `../020-goals.kb/joy.md` | `develop-rigorous-llm-discussion-system.md`, `../020-goals.kb/preserve-speed-of-thought-enjoyment.md` |
| `.../representation-play.md` | 4-5 | `sys.md`, `../020-goals.kb/physxp.md` | `develop-rigorous-llm-discussion-system.md`, `../020-goals.kb/learn-the-physics-and-math-content.md` |
| `.../dual-representation-refinement.md` | 4 | `sys.md` | `develop-rigorous-llm-discussion-system.md` |
| `.../python-schematic-twin.md` | 4-5 | `../020-goals.kb/physxp.md`, `../020-goals.kb/joy.md` | `.../learn-the-physics-and-math-content.md`, `.../preserve-speed-of-thought-enjoyment.md` |
| `.../calculation-light-by-default.md` | 4 | `../020-goals.kb/dis.md` | `../020-goals.kb/discuss-gr-cosmology-and-qm.md` |
| `.../cite-just-in-time.md` | 4-5 | `dis.md`, `../020-goals.kb/corpus.md` | `discuss-gr-cosmology-and-qm.md`, `../020-goals.kb/produce-settled-knowledge-corpus.md` |
| `.../settlement-audit-trail.md` | 4 | `sys.md` | `develop-rigorous-llm-discussion-system.md` |
| `.../healthy-invariant-not-milestone.md` | 4 | `sys.md` | `develop-rigorous-llm-discussion-system.md` |
| `docs/dev/design/use-cases.kb/cosmological-boundary-conditions.md` | 4 | `../020-goals.kb/dis.md` | `../020-goals.kb/discuss-gr-cosmology-and-qm.md` |
| same file | 9 (body prose) | `` `cosmo-bc.kb/` `` | `` `cosmological-boundary-conditions.kb/` `` |
| `.../horizon-symmetries.md` | 4 | `dis.md` | `discuss-gr-cosmology-and-qm.md` |
| `.../de-sitter-horizon-observer-dependence.md` | 4 | same | same |
| `.../alice-bob-schwarzschild-reconciliation.md` | 4 | same | same |
| `.../all-entropy-is-shannon-entropy.md` | 4 | same | same |
| `.../entropy-and-origins-of-life.md` | 4 | same | same |
| `.../unenumerated-further-musings.md` | 4 | same | same |
| `docs/dev/design/use-cases.kb/CLAUDE.md` | 8 (body prose) | `` `cosmo-bc.kb/` `` | `` `cosmological-boundary-conditions.kb/` `` |
| `docs/dev/technical-policy.kb/design-from-settled.md` | 5 | `../design/020-goals.kb/sys.md` | `../design/020-goals.kb/develop-rigorous-llm-discussion-system.md` |
| `docs/dev/technical-policy.kb/causal-structure-before-tensor-calculus.md` | 5 | `../design/030-requirements.kb/calc-light.md` | `../design/030-requirements.kb/calculation-light-by-default.md` |
| `docs/dev/questions.kb/why-was-turok-labeled-twice.md` | 3 | `resolved: ../claims.kb/turok-labels.md` | `resolved: ../claims.kb/turok-paper-citation-labels.md` |
| `docs/dev/questions.kb/is-the-repo-public.md` | 3 | `resolved: ../claims.kb/public-audience.md` | `resolved: ../claims.kb/repo-is-public-no-privacy-concern.md` |
| `docs/dev/questions.kb/who-is-the-audience.md` | 3 | same | same |
| `docs/dev/questions.kb/what-is-the-session-cadence.md` | 3 | `resolved: ../claims.kb/cadence.md` | `resolved: ../claims.kb/session-cadence.md` |
| `docs/dev/questions.kb/should-we-use-cas.md` | 4 | `depends: [cas-can.md]` | `depends: [is-cas-verification-feasible.md]` |
| `/CLAUDE.md` (repo root) | 29 | `M. = design/025-use-cases.kb` | `M. = design/use-cases.kb` |
| same file | 34 | `docs/dev/claims.kb/causal-first.md` | `docs/dev/claims.kb/causal-structure-before-tensor-calculus.md` |

## After fixing

1. Re-grep the whole tree for every pre-rename slug (`dis.md`, `sys.md`,
   `physxp.md`, `joy.md`, `corpus.md`, `formalxp.md`, `proofxp.md`,
   `wf.md`, `contimp.md`, `intuit.md`, `cosmo-bc`, `horizon-sym.md`,
   `ds-observer.md`, `alice-bob.md`, `entropy-one.md`, `entropy-life.md`,
   `/etc.md`, `null-bang.md`, `cpt-bang.md`, `cpt-bh.md`, `cpt-end.md`,
   `cavity.md`, `prog-elab.md`, `rep-play.md`, `dual-rep.md`,
   `py-grok.md`, `calc-light.md`, `cite-jit.md`, `settle-audit.md`,
   `sys-healthy.md`, `local-check.md`, `causal-first.md`,
   `scaffold-ok.md`, `badger-line.md`, `refute-is-win.md`,
   `dg-discuss-only.md`, `adv-discuss-only.md`, `turok-labels.md`,
   `memory-profile.md`, `public-audience.md`, `cadence.md`,
   `sys-design.md`, `formal-substrate.md`, `cas-can.md`, `cas-should.md`,
   `settle-authority.md`, `lit-loop.md`, `model-diversity.md`,
   `concurrency.md`, `scale.md`, `type-bg.md`, `learn-style.md`,
   `baseline.md`, `turok-dup.md`, `privacy.md`, `audience.md`,
   `025-use-cases`) to confirm nothing was missed.
2. Run `~/.claude/skills/llm-kb/bin/llm.kb-validate
   /home/bukzor/repo/github.com/bukzor/ideation.physical-musings/docs/`
   -- must show 0 errors.
3. Manually confirm every `../`-style path in every touched file
   resolves (`test -e`), per `Skill(llm-kb)`'s cross-references
   self-audit.
4. `git status -s .` at repo root -- confirm only `docs/dev/` and root
   `CLAUDE.md` changed.
5. Delete this file once all of the above is clean.
