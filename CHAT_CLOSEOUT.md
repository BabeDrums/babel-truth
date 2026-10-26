# Babel Conversation Closeout Protocol

Use this when Babel asks to close a chat, prepare a fresh-chat handoff, or make the current conversation safely disposable.

> **If losing the current chat would materially change future work, persist the important state before leaving it.**

The goal is durable continuity, not a transcript summary. A handoff prompt is routing/context, never a substitute for repository authority.

## 1. Refresh current reality

Before deciding what is missing, re-read:
- Babel Truth `main`, relevant open PRs, and Issue #1 body + newer relevant comments
- the owning app/Lab `main`, current handoff/authority, and relevant open PRs
- adjacent repos only when they materially affect this lane
- CI/deploy/physical-review state when it changes the next gate

If another lane is writing, identify its branch/PR and avoid overlapping durable surfaces until reconciled.

## 2. Sweep and classify the conversation

Only capture material state that is not already durable. Give each item one primary home:
- **Global/cross-app accepted** → Babel Truth
- **Product-local accepted** → owning product
- **Experiment-local accepted** → Babel Lab / experiment authority
- **Durable unresolved** → new Issue #1 comment
- **Handoff-only context** → final prompt only
- **Transient/history** → do not persist

Handoff-only context is useful collaboration framing that should travel once but would be wrong to canonize.

## 3. Persist only what is missing

Before writing, verify the information is not already captured well enough.

- update accepted rules in their owning authority
- append unresolved durable findings as new Issue #1 comments
- rewrite the Issue #1 body only during explicit consolidation
- remove active contradictions when a new rule replaces an old one
- keep tests/guards/handoff text aligned with accepted rules
- preserve historical evidence in Git/PR history instead of duplicate active docs

Do **not** persist jokes, every brainstorm, rejected options, already-canonical rules, low-level details already preserved by code/tests/PRs, or archival chat summaries.

## 4. Make unfinished work legible

Record only what the next chat actually needs to know about provisional work:
- PR/branch and state (`Draft`, merge-ready, blocked, superseded, seed/history)
- exact validation/physical-review gate
- important non-goals or “do not promote yet” boundaries

Substantial code does not become canonical merely because it exists.

## 5. Recheck concurrency before merge

Before every closeout write—and again before merge—refresh current `main` and relevant open PRs/changed files. Parallel lanes may continue when disjoint; serialize shared-surface overlap.

Issue #1 comments are the preferred append-only mechanism for unresolved cross-lane continuity.

## 6. Stop at continuity

Do not start a new feature/design pass during closeout unless it is strictly necessary to make current state truthful or recoverable. Preserve the next executable step instead.

After persistence, report concisely:
- what was already captured
- what was newly persisted and where
- what was intentionally omitted
- open/provisional/physical-review gates
- best next executable step
- whether repositories + Issue #1 are sufficient without the old chat

If not, say exactly what remains chat-only and why.

## Fresh-chat handoff

Generate the handoff only **after** closeout is complete. Keep it small:
- project-facing name (`Babel`)
- lane ownership
- repo/read order
- instruction to trust newer repo state over prompt hashes/details
- write-scope/concurrency rails
- immediate gate or next executable question
- only truly necessary handoff-only context

Do not paste canonical product doctrine into the prompt when the next chat can read it from the repos.

## Done

A chat is safely disposable when accepted state has the right owner, unresolved state is captured, provisional work is accurately labeled, concurrency hazards are known, the next gate is clear, and a fresh chat can reconstruct the work from repositories + Issue #1 with at most a small handoff prompt.
