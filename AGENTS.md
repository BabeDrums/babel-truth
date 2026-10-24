# Babel Truth — Repository Rules

This repository stores cross-app Babel truth only.

## Before writing

1. Read `START_HERE.md`.
2. Inspect the active Continuity Buffer (Issue #1) for relevant unresolved deltas, including newer comments not yet consolidated into the body.
3. Check whether the proposed rule is actually global. If it belongs to one app, write it there instead.
4. Check whether an open PR already owns the same rule/surface.

## Never do these

- Do not copy entire app specs into Babel Truth.
- Do not make Babel Truth a runtime dependency that silently controls production apps.
- Do not promote a Lab experiment merely because it exists.
- Do not preserve two contradictory current rules side-by-side.
- Do not create universal UI/components before reuse is proven.
- Do not use this repo as a transcript archive.
- Do not use full Issue #1 body replacement for routine persist-before-reply capture.

## Change workflow

Normal durable change:

**classify → shape → branch → edit → reconcile contradictions → review diff → PR → merge → update adopters deliberately**

Babel has standing permission to merge Truth PRs once the diff is reviewed, the scope is genuinely cross-app, no important semantic conflict remains unresolved, and downstream adoption implications are understood.

## Persist-before-reply

For Babel conversations, if a new piece of information is both durable and unresolved, and losing the chat before consolidation would change future work, persist it to Issue #1 before relying on another turn.

### Normal write path

Append a **new Issue #1 comment** for routine capture. Comments are the concurrency-safe intake log for parallel chats.

The Issue #1 body is the consolidated unresolved snapshot. Rewrite the body only during an explicit consolidation pass, after first reading the latest body and all newer comments. This avoids two parallel chats overwriting one another.

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

## Parallel work

Parallel chats are safe when they own different repositories or independent durable surfaces.

Before writing to a repo/branch/file/PR, re-read its current state and relevant open PRs. If another chat already owns the same durable surface, do not write from stale state; reconcile first or let the owning lane finish.

Truth updates do not automatically mutate adopters. Apps stay pinned to their reconciled Truth commit until an explicit adoption pass.

## Promotion and cleanup

When an unresolved item matures:

- global rule → promote to the correct Truth authority
- app-local rule → promote to the owning app authority
- experiment → retain in Lab with explicit experimental status
- rejected/superseded → remove from active buffer

During consolidation, resolve relevant new buffer comments into one of those outcomes, then refresh the Issue #1 body to the current unresolved snapshot. After promotion, remove duplicated active wording from the body and from any old current-authority location. Git/GitHub history remains the archive.

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
- Issue #1 body — consolidated unresolved snapshot
- Issue #1 comments — append-only unresolved intake from parallel chats

## Definition of done

A Truth change is not done until:
- its ownership is correct
- active contradictions are removed or explicitly scoped
- affected app/Lab adoption needs are identified
- the Continuity Buffer is reconciled when appropriate
- the handoff/read order remains coherent
