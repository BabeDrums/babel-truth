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

Read `CHAT_CLOSEOUT.md` when Babel asks to close out a conversation, prepare a fresh-chat handoff, or make the current chat safely disposable.

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

A real product may also use a clearly bounded Lab lane to audition **unproven interaction behavior** without moving product ownership. ADR 0006 governs that boundary: doctrine, canonical behavior, runtime/data, and promoted implementation remain in the owning product; Lab owns only the disposable specimen until deliberate promotion.

## Lab boundary

> **Lab is evidence, never authority.**

Lab may contain contradictory styles, interactions, and hypotheses. Another product does not inherit a design merely because it exists in Lab.

Default evidence path when a Lab experiment is useful:

**owning-product doctrine/question → bounded Lab experiment → physical/real-use validation → owning-product candidate/promotion → genuinely transferable rule promoted to Truth**

A Lab step is optional. If the question already depends on real owning-product runtime/data/navigation relationships, work in the owning product instead.

The Lab **Shell Gallery** is a living visual/device-testable proving environment for generic shared-UI roles and candidates. It is distinct from an owning product's historical certification environment, such as FIRE's frozen G7 Shell Test. Presence in the Gallery does not make a pattern canonical; Truth owns cross-app promotion.

## Adoption model

Truth changes do **not** silently mutate product repos. Apps/Lab explicitly compare and adopt a newer immutable Truth commit, then update their local pointer.

`registry/apps.json` records adoption refs/status. Do not duplicate exact adoption SHAs in prose files.

## Continuity

Issue #1 is the unresolved durable buffer.

Normal persist-before-reply capture is append-only through **new comments**. The issue body is the consolidated current snapshot and is rewritten only during explicit consolidation after reading the body and all newer comments.

Do not use it as a transcript archive.

For conversation migration, use `CHAT_CLOSEOUT.md`: persist missing durable state first, then make the handoff prompt a small routing layer rather than a second authority store.

## Shared-system boundary

Do not build a speculative universal component library. Share validated semantics, principles, small foundation tokens, and contracts first. Extract shared implementation only after multiple real products prove the same code and meaning genuinely need reuse.

ADR 0005 owns the initial cross-app context/handoff contract. Specialist products remain independently useful; context may follow the work across products without copying specialist internals or re-asking settled decisions. Prove the semantic fields through real flows before designing a universal Babel data model or backend.

ADR 0006 owns bounded Lab incubation for existing products. It permits cheap/disposable interaction auditions while preserving one real product owner and defines concurrency expectations for shared Lab surfaces.

## Current cross-app sequence

1. **FIRE G7 shell is frozen.** The owning-product runtime that received final explicit Babel approval is FIRE commit `4a258c5170dd1d96dcbc0f2b0a9c35b283cec489`. The ten-category certification gate is complete; V6 remains production until a separate deliberate promotion decision.
2. **The validated generic shell is shared Truth.** `FOUNDATIONS.md` owns the transferable Babel shell baseline; ADR 0004 records why it was promoted. FIRE fixture workflow/copy and FIRE Core product architecture remain FIRE-local and were not promoted.
3. **FIRE Core remains owned by FIRE.** FIRE doctrine, canonical behavior, runtime/data, and promoted implementation stay in `babel-fire`. Genuinely unproven FIRE Core interaction slices may be auditioned under a clearly labeled `babel-lab/fire/core/**` lane with fake/local state, then deliberately promoted back into FIRE only after physical/real-use evidence. FIRE's historical G7 Shell Test remains frozen certification evidence and is not moved to Lab.
4. **Cross-app context is an explicit architecture concern, not an implementation prerequisite.** ADR 0005 defines the boundary. A future bounded experiment should prove one real FIRE → World → FIRE context loop before shared storage/schema infrastructure is standardized.
5. **Lab has a separate shared-UI proving role.** Its Shell Gallery may evolve generic candidates under explicit Proven/Candidate/Experimental status while Truth remains canonical and no universal shared runtime/package is assumed.
6. **Parallel product lanes must respect ownership.** FIRE- and WORLD-specific Lab paths may advance independently when disjoint; root/shared/shell/Truth-pointer/cross-cutting-CI surfaces are shared and require current-state/open-PR reconciliation before writes. Do not let one lane silently rewrite another lane's product logic.
7. **World remains an experiment/concept until its product job earns a real product repo.** Do not create ecosystem products to fill conceptual slots.

The owning repo's current handoff always controls its exact build/PR/next-step state.
