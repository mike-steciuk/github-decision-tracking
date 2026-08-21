# Instructions for coding agents

This repository's accepted decision records are binding engineering
constraints.

Before planning or changing code:

1. Read `decisions/README.md`.
2. From its Decision sources table, read each reachable decision index whose
   scope may apply to the requested work.
3. Read every `accepted` decision from those indexes whose scope applies.
4. Follow those decisions even when another implementation seems preferable.
5. Do not treat `proposed`, `rejected`, `deprecated`, or `superseded` records as
   current direction.
6. If accepted decisions conflict, apply a narrower decision only when it
   explicitly lists the broader decision in `overrides`. An override is limited
   to the narrower decision's declared scope; it does not supersede the broader
   decision.
7. If a required decision source cannot be read, or a conflict has no explicit
   override, stop and clearly report:
   the decision ID, the conflict, and the smallest viable resolution.
8. Do not silently replace or weaken a decision. Use `supersedes` when replacing
   direction in the same decision set, or `overrides` for a narrower exception
   to a broader decision.
9. In pull requests, list applied decision IDs under `Decisions applied`, using
   qualified references for non-local decisions (for example `org:DEC-0042`).

When a decision is ambiguous, preserve existing behavior and ask for
clarification. Repository-specific instructions closer to the changed code may
add constraints but may not override accepted decisions without an accepted,
explicitly scoped override decision.
