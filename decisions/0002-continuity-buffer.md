# Decision 0002 — Lightweight Continuity Buffer

**Status:** Accepted

## Context

Important product/design information can emerge between code commits. Requiring a PR or repository-file commit for every durable chat finding would create noise, but relying on chat context alone risks losing important unresolved information when a conversation ends.

## Decision

Use one rolling GitHub Issue in Babel Truth as the lightweight **Babel Continuity Buffer**.

Apply **persist-before-reply** when a new unresolved durable fact would materially change future work if the chat ended before consolidation.

The buffer is low-authority. It never silently overrides accepted Babel Truth or app-local authority.

## Promotion lifecycle

Each active item eventually becomes:

- promoted to Babel Truth
- promoted to an app-local authority
- retained explicitly as a Lab experiment
- intentionally deferred and left active
- rejected/superseded and removed from the active buffer

GitHub issue history preserves prior edits; the active body should remain useful current unresolved state rather than a transcript archive.

## Consequences

- A conversation can end after an important discovery without requiring an immediate code PR.
- New chats have one place to inspect unresolved durable deltas after reading authority.
- Canonical docs stay cleaner because unresolved thoughts do not become doctrine prematurely.
