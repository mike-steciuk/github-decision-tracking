# Decision index

This is the agent-readable index of engineering decisions. Update it in the
same pull request that adds or changes a decision.

## Active

| ID | Decision | Scope | Accepted |
| --- | --- | --- | --- |
| [DEC-0001](0001-record-decisions-as-versioned-markdown.md) | Record decisions as versioned Markdown | repository-wide | 2026-07-31 |
| [DEC-0002](0002-link-decision-sets-and-record-scoped-overrides.md) | Link decision sets and record scoped overrides | repository-wide | 2026-08-21 |

## Decision sources

Register decision sets that can apply to this repository. Use a stable,
lowercase namespace in qualified references such as `org:DEC-0042`. Order does
not imply precedence: scope determines applicability, and a narrower decision
departs from a broader one only when it declares an explicit override.

| Namespace | Level | Scope | Decision index |
| --- | --- | --- | --- |
| local | project | this repository | [Local decisions](README.md) |

Add rows for applicable organization, department, team, project, or service
indexes. Link to a stable, agent-readable Markdown file rather than a general
documentation home page.

## Proposed

None.

## Deprecated or superseded

None.

## Rejected

None.
