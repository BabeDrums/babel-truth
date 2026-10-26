# Babel Truth — Start Here

Use **Babel** as the project-facing name.

This repository is the first read for **cross-app Babel authority**. It does not replace app-local authority.

## Minimal read order

1. `START_HERE.md` — this authority/routing map
2. `AGENTS.md` — shared operating rules, including research-first feedback interpretation
3. `FOUNDATIONS.md` — shared product/design/interaction defaults when relevant
4. `registry/apps.json` and relevant accepted `decisions/` only when the task needs them
5. Babel Continuity Buffer Issue #1 body + newer comments for relevant unresolved durable findings
6. then the owning app/Lab handoff and code

Do not read every historical file by default. Pull deeper context only when the task needs it.

## Authority model

Babel Truth owns only what genuinely needs to transfer across products.

When sources conflict:
1. settled Babel Truth wins for cross-app semantics/process/foundations
2. the owning app's canonical authority wins for app-local behavior
3. an intentional Lab experiment may diverge while explicitly testing an alternative
4. the Continuity Buffer is unresolved evidence, not authority
5. old prototypes, PRs, and Git history are history/evidence, not current authority

Classify durable information before storing it:
- **Global** → Babel Truth
- **App-local** → owning app repository
- **Experimental** → Babel Lab
- **Unresolved** → Babel Continuity Buffer

> **One current truth. Clear ownership. History stays in Git.**

## Repo roles

- `BabeDrums/babel-truth` — cross-app truth/control plane; no product runtime
- `BabeDrums/babel-fire` — FIRE product; production + successor work
- `BabeDrums/babel-lab` — experimental sandbox/incubator using fake/prototype state by default
- future real products earn their own repos when a real product job exists

A World prototype may live in Lab. Lab itself is not the World product.

## Lab boundary

> **Lab is evidence, never authority.**

Lab may contain contradictory styles, interactions, and hypotheses. Another product does not inherit a design merely because it exists in Lab.

Default evidence path when a Lab experiment is useful:

**bounded experiment → owning-product candidate → owning-product physical/real-use validation → genuinely transferable rule promoted to Truth**

A Lab step is optional.

## Adoption model

Truth changes do **not** silently mutate product repos. Apps/Lab explicitly compare and adopt a newer immutable Truth commit, then update their local pointer.

`registry/apps.json` records adoption refs/status. Do not duplicate exact adoption SHAs in prose files.

## Continuity

Issue #1 is the unresolved durable buffer.

Normal persist-before-reply capture is append-only through **new comments**. The issue body is the consolidated current snapshot and is rewritten only during explicit consolidation after reading the body and all newer comments.

Do not use it as a transcript archive.

## Shared-system boundary

Do not build a speculative universal component library. Share validated semantics, principles, small foundation tokens, and contracts first. Extract shared implementation only after multiple real products prove the same code and meaning genuinely need reuse.

ADR 0005 owns the initial cross-app context/handoff contract. Specialist products remain independently useful; context may follow the work across products without copying specialist internals or re-asking settled decisions. Prove the semantic fields through real flows before designing a universal Babel data model or backend.

## Current cross-app sequence

1. **FIRE G7 shell is frozen.** The owning-product runtime that received final explicit Babel approval is FIRE commit `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489`. The ten-category certification gate is complete; V6 remains production until a separate deliberate promotion decision.
2. **The validated generic shell is now shared Truth.** `FOUNDATIONS.md` owns the transferable Babel shell baseline; ADR 0004 records why it was promoted. FIRE fixture workflow/copy and FIRE Core product architecture remain local and were not promoted.
3. **FIRE Core is unblocked.** FIRE may begin end-to-end breadboarding from `FIRE_CORE.md`, then build the thinnest believable spine and validate it on real projects. As that journey is shaped, identify what FIRE must know to guide each decision and which resulting facts genuinely matter outside FIRE; do not design World inside FIRE.
4. **Cross-app context is now an explicit architecture concern, not an implementation prerequisite.** ADR 0005 defines the boundary. A future bounded experiment should prove one real FIRE → World → FIRE context loop before shared storage/schema infrastructure is standardized.
5. **Lab reconciliation is a separate parallel lane.** Lab may adopt this newer Truth and reconcile its provisional generic chrome to the shared shell while preserving Fire/World experiment identity. Lab reconciliation does not block FIRE Core.
6. **World remains an experiment/concept until its product job earns a real product repo.** Do not create ecosystem products to fill conceptual slots.

The owning repo's current handoff always controls its exact build/PR/next-step state.
