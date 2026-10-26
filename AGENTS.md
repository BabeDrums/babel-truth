# Babel Truth — Agent Rules

This repository owns **cross-app Babel rules only**. Use **Babel** as the project-facing name.

## Entry

Before substantive Babel work:
1. read `START_HERE.md`
2. read this file
3. read `FOUNDATIONS.md` when product/design decisions matter
4. inspect relevant accepted records in `decisions/` and current adoption metadata in `registry/apps.json` when needed
5. inspect Babel Continuity Buffer Issue #1 body + newer comments for relevant unresolved durable findings
6. then read the owning app/Lab handoff and code

Do not copy app-local specs into Truth just to make them easier to find.

## Interpret feedback before implementing it

**User feedback is evidence and desired outcome, not automatically a literal implementation command.**

Unless Babel explicitly locks an exact implementation, treat observations, proposed fixes, screenshots, and recommendations as inputs to diagnose:
- what problem is actually being experienced
- whether the cause is system-level, component-level, local composition, behavior, copy, data, or environment
- whether the proposed direction is the best solution or only one possible solution

For nontrivial design/technical/product decisions, inspect current repo/product reality and use current authoritative research when it can materially improve the decision. Prefer elegant shared fixes over page-specific compensation.

If Babel's proposed direction conflicts with stronger evidence, product goals, safety, or current authority, say so clearly and recommend the better direction rather than following it mechanically.

At meaningful decision/review boundaries, automatically surface any **material questions, recommendations, comments, or concerns** that would change the next step. Do not manufacture a list when none exist; say the path is clear and proceed.

## Shared operating loop

Use:

> **Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate**

- **Observe:** current behavior, user/device evidence, repo state, open PRs, relevant research.
- **Diagnose:** find the root class of problem before changing code.
- **Shape:** choose the smallest coherent solution; prefer deleting complexity over compensating around it.
- **Contract:** for nontrivial work, state the problem, success conditions, non-goals, ownership, and validation needed in the working PR/issue/plan. Do not create a permanent spec for every pass.
- **Build:** change the shared primitive/rule first when the defect is shared; avoid scattered cosmetic patches.
- **Verify:** static/behavior tests, representative responsive checks, physical-device validation where visual/mobile behavior matters, and real-project validation where product logic matters.
- **Consolidate:** move durable conclusions to the correct authority, remove superseded active wording/code, and leave unresolved durable items in the Continuity Buffer.

Automated browser checks do not equal physical-device approval.

## Information ownership

Classify durable information before storing it:
- **Global** → Babel Truth
- **App-local** → owning app repo
- **Experimental** → Babel Lab / experiment authority
- **Unresolved** → Babel Continuity Buffer

Truth owns cross-app foundations, shared process, repo roles, semantic contracts, and major architectural decisions. App repos own their product behavior/runtime/data/specs. Lab owns experiments only.

> **Lab is evidence, never authority.**

ADR 0006 permits a bounded Lab experiment for an existing real product without transferring product ownership. The owning app still owns doctrine, canonical behavior, runtime/data, and promoted implementation. Prototype behavior/code must be deliberately promoted; it is never canonical merely because it exists in Lab.

## Conflict classification

When an app/Lab rule differs from Truth, classify it before editing:
1. **stale divergence** — adopter should update to Truth
2. **intentional experiment** — keep the deviation and label the hypothesis
3. **potential upstream improvement** — stop and decide whether Truth should change first
4. **app-local exception** — keep it local and clarify ownership

## Contradictions

Active authority should contain **one current truth**.

When rule B replaces rule A:
1. update current authority to B
2. remove/rewrite A anywhere it still presents as current
3. update tests/guards that protect A
4. leave Git history alone
5. create/supersede a decision record only when the architectural reasoning is important enough to preserve explicitly

Do not solve contradiction by accumulating qualifiers forever.

## Continuity

Use Issue #1 as the lightweight unresolved buffer.

Persist before reply when a new fact is both durable and unresolved and losing the chat would change future work. Normal capture is a **new Issue #1 comment**. The issue body is the consolidated unresolved snapshot and is rewritten only during an explicit consolidation after reading the body and all newer comments.

Persist useful things such as:
- real-device findings that change the next contract
- new architecture/process/product boundaries
- meaningful conflicts between experiment and authority
- durable unresolved questions

Do not persist jokes, every brainstorm option, already-canonical rules, immediately rejected ideas, or low-level implementation detail already preserved in code/tests/PR history.

## Conversation closeout / handoff

When Babel asks to close out a chat, prepare a fresh-chat handoff, or make the current conversation safely disposable, follow `CHAT_CLOSEOUT.md`.

The closeout goal is **durable continuity, not a transcript summary**:
- refresh current Truth / owning-repo state first
- sweep the conversation for materially important state not yet persisted
- classify it by correct owner
- persist only what is genuinely missing
- label unfinished PR/branch/physical-review state accurately
- avoid starting new product work during closeout unless continuity repair requires it
- only then generate a compact next-chat handoff

A handoff prompt is a routing layer, not authority. Canonical product/process state belongs in the repos; durable unresolved state belongs in the Continuity Buffer. Small **handoff-only context** may remain in the prompt when it materially helps the next chat but would be wrong to canonize.

A closeout is not complete if the next chat would still need the old chat to know what materially happened.

## Parallel work

Before any durable write, re-read current target state and relevant open PRs. If another chat already owns the same branch/file/PR/surface, reconcile current state before writing.

Product-specific lanes may proceed in parallel when their owned files/surfaces are genuinely disjoint. Shared surfaces are a stricter concurrency boundary: one lane must not silently reinterpret or overwrite a shared surface while another lane is changing it.

For Babel Lab, treat root/shared shell/Truth-pointer/cross-cutting CI surfaces as shared unless current Lab authority says otherwise. FIRE-specific and WORLD-specific experiment paths may advance independently when disjoint, but changes to shared Lab chrome, `shared/**`, `shell/**`, root navigation, adoption pointers, or tests spanning multiple experiments require a fresh main/open-PR reconciliation first.

If a product-specific experiment discovers a shared need, classify it instead of reaching across ownership casually: owning-product behavior returns to the owning app; generic shared semantics become a Truth candidate; unresolved cross-lane conflicts go to Issue #1.

Append-only Issue #1 comments are the preferred concurrency-safe mechanism for unresolved cross-lane continuity. Do not rewrite the Issue #1 body from routine parallel work.

Before merging, repeat the current-main/open-PR overlap check. A branch that was safe when created may no longer be safe at merge time.

Truth changes do not silently mutate adopters. Each app/Lab remains pinned to the immutable Truth commit it last reconciled against until an explicit adoption pass.

## Change workflow

Normal durable Truth change:

**classify → shape → branch → edit → remove contradictions → review diff → PR → merge → deliberately update adopters**

Babel has standing permission to merge a Truth PR when the diff has been reviewed, the scope is genuinely cross-app, no important semantic conflict remains unresolved, and downstream adoption implications are understood. Stop instead when ownership or product meaning is genuinely unresolved.

## Major decisions

`decisions/` is for architecturally significant decisions only. Accepted decision records remain historical evidence; if a decision changes, supersede it rather than rewriting history.

## Repository map

- `START_HERE.md` — authority/routing/current cross-app sequence
- `AGENTS.md` — these operating rules
- `CHAT_CLOSEOUT.md` — reusable conversation-closeout / fresh-chat handoff protocol
- `FOUNDATIONS.md` — shared product/design/interaction defaults
- `registry/apps.json` — current repo roles and explicit Truth adoption refs
- `decisions/` — major architectural decision history
- `templates/BABEL_TRUTH.md` — adopter pointer template
- Issue #1 — unresolved durable continuity

Git/GitHub history is the archive. Do not keep dead documentation active merely for history.

## Definition of done

A Babel change is not done until:
- ownership is correct
- current contradictions are removed or intentionally scoped
- relevant research/evidence has been considered when material
- tests/guards and handoff agree with the new rule
- affected adopter implications are understood
- unresolved durable findings are captured or resolved
- dead/replaced active documentation is removed rather than left to drift
