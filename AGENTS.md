# Babel Truth — Repository Rules

This repository stores cross-app Babel truth only.

## Before writing

1. Read `START_HERE.md`.
2. Inspect the active Continuity Buffer (Issue #1) for relevant unresolved deltas.
3. Check whether the proposed rule is actually global. If it belongs to one app, write it there instead.
4. Check whether an open PR already owns the same rule/surface.

## Never do these

- Do not copy entire app specs into Babel Truth.
- Do not make Babel Truth a runtime dependency that silently controls production apps.
- Do not promote a Lab experiment merely because it exists.
- Do not preserve two contradictory current rules side-by-side.
- Do not create universal UI/components before reuse is proven.
- Do not use this repo as a transcript archive.

## Change workflow

Normal durable change:

**classify → shape → branch → edit → reconcile contradictions → review diff → PR → merge → update adopters deliberately**

Babel has standing permission to merge Truth PRs once the diff is reviewed, the scope is genuinely cross-app, no important semantic conflict remains unresolved, and downstream adoption implications are understood.

## Persist-before-reply

For Babel conversations, if a new piece of information is both durable and unresolved, and losing the chat before consolidation would change future work, persist it to Issue #1 before relying on another turn.

Good candidates:
- a newly discovered real-device defect/pattern
- a new cross-app constraint
- a durable process/architecture decision not yet promoted
- a meaningful conflict between Lab and an accepted standard
- a product-boundary decision that affects future repos

Do not persist:
- jokes
- every brainstorm option
- already-canonical rules
- immediately rejected ideas
- low-level implementation details already committed/tested

## Promotion and cleanup

When an unresolved item matures:

- global rule → promote to the correct Truth authority
- app-local rule → promote to the owning app authority
- experiment → retain in Lab with explicit experimental status
- rejected/superseded → remove from active buffer

After promotion, remove duplicated active wording from the buffer and from any old current-authority location. Git/GitHub history remains the archive.

## Conflict reconciliation

When an app/Lab rule conflicts with Truth, classify before changing anything:

1. **Stale divergence** — adopter should update to Truth.
2. **Intentional experiment** — divergence remains because the experiment is testing an alternative.
3. **Potential upstream improvement** — do not overwrite; surface the conflict and decide whether Truth should change first.
4. **App-local exception** — Truth is not actually the right owner; preserve local behavior and clarify the boundary.

## Scope ownership

- `PRODUCT_PRINCIPLES.md` — cross-app product philosophy and boundaries
- `DESIGN.md` — transferable interaction/design foundations
- `PROCESS.md` — iteration, continuity, adoption, contradiction workflow
- `registry/apps.json` — current repo/app roles and reconciliation metadata
- `decisions/` — major architectural decisions only
- Issue #1 — unresolved durable deltas only

## Definition of done

A Truth change is not done until:
- its ownership is correct
- active contradictions are removed or explicitly scoped
- affected app/Lab adoption needs are identified
- the Continuity Buffer is reconciled
- the handoff/read order remains coherent
