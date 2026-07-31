---
id: DEC-0001
title: Record decisions as versioned Markdown
status: accepted
date: 2026-07-31
scope:
  - repository-wide
owners:
  - engineering
supersedes: []
superseded_by: null
discussion: null
---

# DEC-0001: Record decisions as versioned Markdown

## Problem statement

Engineering discussions can produce decisions that are difficult for people
and coding agents to discover later. A durable, reviewable source of truth is
needed.

## Proposal

Use GitHub issues for discussion and store finalized decisions as Markdown in
`decisions/`. Maintain a compact index in `decisions/README.md` and point coding
agents to it from the root `AGENTS.md`.

## Decision

Accepted. Issues are the deliberation surface. A merged decision record is the
authoritative artifact. Only records with `status: accepted` are active
engineering direction.

## Short-term impact

- Contributors must create and review a decision file after discussion.
- Pull requests can cite stable decision IDs.
- Coding agents have a deterministic place to discover constraints.

## Long-term impact

- Decisions and their evolution remain in version history.
- Replacements form an explicit chain instead of erasing prior context.
- The decision index requires routine maintenance.

## Alternatives considered

- Keep decisions only in issues: rejected because issue state and comments do
  not provide a concise, versioned source of truth.
- Use an external wiki: rejected for the POC because it separates decisions
  from the code review and agent context.

## Replaces

None.

## Consequences and follow-up

Review the workflow after the first five decisions and adjust required fields
or automation based on actual use.

