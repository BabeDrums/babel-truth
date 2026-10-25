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

## Current cross-app sequence

1. **FIRE:** continue local G7 shell certification/physical review. V6 remains production. FIRE Core stays blocked until FIRE explicitly satisfies its shell freeze gate.
2. **After FIRE shell freeze:** promote only the proven transferable shell rules into Truth.
3. **Then parallelize:** FIRE may begin FIRE Core breadboarding while Lab independently adopts the promoted Truth and reconciles its generic chrome. Lab reconciliation does not block FIRE Core.
4. **Lab:** otherwise remain a bounded-experiment sandbox; do not maintain a parallel full FIRE shell.

The owning repo's current handoff always controls its exact build/PR/next-step state.
