---
id: DEC-0002
title: Link decision sets and record scoped overrides
status: accepted
date: 2026-08-21
scope:
  - repository-wide
owners:
  - engineering
supersedes: []
superseded_by: null
related_decisions:
  - local:DEC-0001
overrides: []
discussion: null
---

# DEC-0002: Link decision sets and record scoped overrides

## Problem statement

Engineering direction may be established at organization, department, team,
project, or service scope. A repository needs to make applicable decision sets
discoverable to people and agents while allowing a conscious local exception
without invalidating the broader direction.

## Proposal

Register applicable decision indexes in a Decision sources table in
`decisions/README.md`. Give each source a stable namespace and use qualified
references such as `org:DEC-0042` when referring to decisions outside the local
set.

Add `related_decisions` and `overrides` metadata to decision records. An
override must name the broader decision and explain the narrower scope and
rationale in the record body.

## Decision

Accepted. Decision sets may be linked across organizational scopes through the
local decision index. Scope determines which accepted decisions apply. A
narrower accepted decision takes precedence over a conflicting broader
decision only when it explicitly declares that decision as an override.

An override is an exception limited to the narrower record's scope. It does not
change the status or authority of the broader decision elsewhere.

## Short-term impact

- Decision indexes must register each applicable external decision source.
- Agents must read reachable, applicable decision indexes before planning work.
- Local exceptions require an explicit accepted decision instead of an
  undocumented departure.
- Cross-set references must use registered namespaces to avoid ambiguous IDs.

## Long-term impact

- Organization-wide direction can remain authoritative without preventing
  justified project or service exceptions.
- Repositories retain a locally discoverable map of their governing decisions.
- Broken or unavailable decision-source links can block work that depends on
  them and must be maintained like other engineering dependencies.

## Alternatives considered

- Copy broader decisions into each repository: rejected because copies drift
  and obscure the authoritative source.
- Treat the closest decision as automatically authoritative: rejected because
  an accidental conflict could silently weaken broader direction.
- Use supersession for local exceptions: rejected because supersession would
  incorrectly imply that the broader decision is no longer active.

## Replaces

None.

## Related decisions

- `local:DEC-0001` establishes versioned Markdown and decision indexes as the
  authoritative, agent-readable mechanism.

## Scoped overrides

None.

## Consequences and follow-up

Validate the source-table and qualified-reference conventions with a real
multi-level project. Consider automation for link and reference validation once
the conventions have been exercised across multiple repositories.
