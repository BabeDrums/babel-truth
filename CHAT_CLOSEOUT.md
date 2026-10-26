# Babel Conversation Closeout Protocol

Use this when Babel asks to close out a chat, prepare a handoff, move work into a fresh chat, or otherwise make the current conversation safely disposable.

The goal is **not** to create a giant transcript summary. The goal is to make the repositories and Continuity Buffer sufficient for the next chat to reconstruct the real project state with minimal prompt-only context.

## Core rule

> **If losing the current chat would materially change future work, the important state must be persisted before the chat is abandoned.**

A handoff prompt is routing/context, not a substitute for durable project state.

## 1. Refresh reality first

Before deciding what is missing, re-read the current state that can supersede chat memory:

1. Babel Truth `main`, relevant open PRs, and the current Continuity Buffer body + newer relevant comments
2. the owning app/Lab `main`, relevant authority/handoff files, and relevant open PRs
3. any adjacent repo whose current state materially affects the lane
4. current CI/deploy state when an unverified merge or physical-review gate matters

If another chat/lane is actively writing, identify its branch/PR and avoid editing the same durable surface until the overlap is reconciled.

## 2. Sweep the current conversation

Review the conversation for materially important state that may not yet be durable. Do not assume every memorable discussion deserves storage.

Classify each candidate into exactly one primary bucket:

- **Global/cross-app accepted** → Babel Truth authority
- **App-local accepted** → owning app authority
- **Experimental accepted-for-the-experiment** → Babel Lab / experiment authority
- **Durable unresolved** → a new Babel Truth Issue #1 comment
- **Handoff-only context** → final handoff prompt only
- **Transient/history** → do not persist; Git/chat history is enough

Examples of handoff-only context include a small collaboration nuance, current review emphasis, or temporary framing that helps the next chat work effectively but would be wrong to canonize as product authority.

## 3. Persist only what is genuinely missing

Before writing, check whether the information is already captured well enough.

Do not duplicate the same rule into several repos merely to make it easier to find. Prefer the owning source and pointers/read order.

When writing:

- update accepted rules in the correct authority rather than leaving them only as unresolved notes
- append durable unresolved findings as a **new Issue #1 comment**
- do not rewrite the Issue #1 body during routine closeout; body rewrite is an explicit consolidation task
- remove or rewrite active contradictions when a new accepted rule supersedes an old one
- update tests/guards/handoff text when the accepted rule they protect changes
- preserve historical PR/commit evidence; do not keep obsolete active docs just for history

Do not persist:

- jokes or emotional reactions that do not change work
- every brainstorm alternative
- already-canonical rules
- immediately rejected ideas
- low-level implementation detail already preserved in code/tests/PR history
- long chat summaries whose only purpose is archival duplication

## 4. Preserve unfinished work explicitly

A closeout must make unmerged or provisional work legible.

Record, where relevant:

- open PR number/title/state (`Draft` vs merge-ready)
- whether the branch is seed material, blocked, superseded, awaiting physical review, or safe to merge
- the exact next validation gate
- important non-goals / “do not accidentally promote this” boundaries

Never make an unresolved PR look canonical merely because it contains substantial work.

## 5. Concurrency-safe closeout

Parallel chats are allowed when their write scopes are disjoint.

Before any durable write during closeout:

1. refresh the current target branch
2. inspect relevant open PRs and, when needed, changed filenames
3. confirm the current lane owns the target surface
4. if another lane overlaps, serialize/reconcile that shared change instead of racing it

Append-only Issue #1 comments are the preferred concurrency-safe place for unresolved cross-lane continuity.

Before merging a closeout PR, repeat the refresh/open-PR check. A branch that was safe when created may no longer be safe at merge time.

## 6. Do not start a new product pass during closeout

Closeout is for continuity repair, contradiction cleanup, and handoff readiness.

Do not use it as an excuse to begin a new feature/design pass unless that change is strictly necessary to make current state truthful or recoverable.

If implementation work remains, preserve the next executable step instead of completing it opportunistically.

## 7. Closeout report

After persistence is complete, report concisely:

- what important state was already safely captured
- what was newly persisted and where
- what was intentionally left out and why
- current open PR/branch/physical-review gates that matter
- the exact best next executable step
- whether the lane is now safe to continue from repositories alone

If it is **not** safe, say exactly what remains chat-only and why it could not be persisted.

## 8. Generate the next-chat handoff only after closeout

A fresh-chat prompt should be a **routing layer**, not another authority file.

Prefer a compact prompt that tells the next chat:

- project-facing name (`Babel`)
- which lane it owns
- repo/read order
- to trust newer repo state over stale hashes in the prompt
- current write-scope / concurrency rails
- current immediate gate or next executable question
- any truly necessary handoff-only context that did not belong in authority

Do not copy large canonical sections into the prompt when the next chat can read them directly from the repos.

If exact hashes are included, treat them as last-known anchors only and explicitly instruct the next chat to follow newer documented state.

## Definition of closeout done

A conversation is safely closed when:

- accepted durable state has a correct owner
- unresolved durable state is captured
- open/provisional work is accurately labeled
- active contradictions relevant to the lane are removed or explicitly scoped
- concurrency/ownership hazards are known
- the next executable gate is clear
- a fresh chat can reconstruct the work from repositories + Continuity Buffer, with only a small amount of handoff-only context if needed

At that point, the old conversation is useful history—not required operational memory.
