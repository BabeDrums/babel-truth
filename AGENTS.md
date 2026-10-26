# Babel Truth — Agent Rules

Use **Babel** as the project-facing name.

This file owns shared operating behavior only. Product rules belong to the owning product; experiment rules belong to Lab.

## Entry

Before substantive Babel work:
1. read `START_HERE.md`
2. read this file
3. read `FOUNDATIONS.md` when product/design/interaction decisions matter
4. inspect relevant ADRs/registry/Issue #1 only when the task needs them
5. then read the owning app/Lab handoff and code

Do not copy product-local specs into Truth for convenience.

## Interpret feedback before implementation

**Babel's feedback is evidence and desired outcome, not automatically a literal implementation command.**

Unless an exact implementation is explicitly locked:
- diagnose the actual problem first
- distinguish shared-system, component, local composition, behavior, copy, data, and environment causes
- inspect current repo/product reality and current research when it can materially change the decision
- prefer the smallest coherent/systemic fix over page-specific compensation
- push back when stronger evidence points to a better direction

At meaningful decision/review boundaries, surface only questions or concerns that would change the next step.

## Operating loop

> **Observe → Diagnose → Shape → Contract → Build → Verify → Consolidate**

- **Observe:** repo state, open PRs, real-device/user evidence, relevant research
- **Diagnose:** identify the root class of problem
- **Shape:** choose the smallest coherent solution; delete complexity before styling around it
- **Contract:** state success, non-goals, ownership, and validation for nontrivial work
- **Build:** fix the owning primitive/rule first when the defect is shared
- **Verify:** tests + representative widths + physical-device/real-project validation when relevant
- **Consolidate:** move accepted conclusions to authority, remove superseded active wording/code, leave only durable unresolved state in Issue #1

Automation does not replace physical-device approval for visual/mobile behavior.

## Information ownership

Classify before storing:
- **Global/cross-app accepted** → Babel Truth
- **Product-local accepted** → owning product
- **Experimental** → Babel Lab / experiment authority
- **Durable unresolved** → Issue #1
- **Historical/transient** → Git/PR/chat history; do not promote it into active docs

> **Lab is evidence, never authority.**

ADR 0006 permits bounded product auditions in Lab without transferring ownership. Prototype code/behavior is promoted deliberately; it is never canonical merely because it exists.

## Conflicts and contradictions

When an app/Lab rule differs from Truth, classify it as:
1. stale divergence
2. intentional experiment
3. potential upstream improvement
4. product-local exception

Active authority should contain **one current truth**. When a rule changes, update current authority and its tests/guards; remove superseded active wording. Preserve history in Git rather than carrying contradictory prose forward.

## Continuity and closeout

Issue #1 is the lightweight unresolved buffer. Persist before reply only when a new fact is both durable and unresolved and losing the chat would materially change future work.

Routine capture uses a new Issue #1 comment. Rewrite the issue body only during an explicit consolidation after reading the body and all newer comments.

When closing/migrating a chat, follow `CHAT_CLOSEOUT.md`. A handoff prompt is routing/context, not authority.

## Parallel work

Parallel lanes are allowed when write scopes are genuinely disjoint.

Before any durable write—and again before merge:
1. refresh the current target `main`
2. inspect relevant open PRs/changed files
3. confirm ownership of the target surface
4. serialize/reconcile overlap on shared surfaces instead of racing another lane

Truth changes do not silently mutate adopters. Each app/Lab stays pinned to the Truth commit it last reconciled against until an explicit adoption pass.

For Lab-specific shared-surface details, follow ADR 0006 and Lab's own `AGENTS.md` rather than duplicating path lists here.

## Durable change workflow

**classify → shape → branch → edit → remove contradictions → review diff → PR → merge → deliberately update affected adopters**

Babel has standing permission to merge when scope/ownership are clear, required checks are satisfied, no material semantic conflict remains, and downstream implications are understood. Stop when product meaning, safety, or ownership is genuinely unresolved.

## Major decisions and history

Use `decisions/` only for architecture/process decisions important enough to preserve explicitly. Accepted ADRs remain historical decision records; supersede them rather than rewriting their history.

Git/PR history is the archive. Do not maintain duplicate ledgers, transcript summaries, or dead docs as active authority.

## Definition of done

A Babel change is done when:
- ownership is correct
- active contradictions are removed or intentionally scoped
- evidence/research was considered when material
- implementation/tests/handoff agree with the current rule
- adopter implications are understood
- durable unresolved findings are captured
- dead/replaced active documentation/code is removed
