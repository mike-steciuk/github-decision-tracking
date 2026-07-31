# Engineering Decision Log

This repository is a proof of concept for discussing, recording, and enforcing
engineering decisions.

## Workflow

1. Open a **Decision proposal** issue. Describe the problem, proposal,
   alternatives, impacts, and decisions it may replace.
2. Discuss the proposal in the issue. Record important constraints and links.
3. When the team decides, copy the issue into `decisions/` using the decision
   template and open a pull request.
4. Merge the decision record after approval.
5. Close the proposal issue with a link to the merged decision.
6. If a later decision replaces it, mark the old record `superseded` and link
   both records in their `supersedes` / `superseded_by` fields.

Issues hold the conversation; versioned decision records hold the durable
outcome. Pull requests provide an auditable approval trail.

## Decision states

- `proposed`: under discussion; agents must not treat it as direction.
- `accepted`: active engineering direction.
- `deprecated`: still present, but should not be used for new work.
- `superseded`: replaced by another decision.
- `rejected`: considered and declined.

## For AI coding agents

Start with [AGENTS.md](AGENTS.md). Active decisions are listed in
[decisions/README.md](decisions/README.md). Agents should apply accepted
decisions to work in this repository, surface conflicts before coding, and cite
the applicable decision IDs in pull requests.

## Naming

Decision files use `NNNN-short-kebab-title.md`, for example
`0001-use-postgresql-for-system-of-record.md`. IDs never change or get reused.

