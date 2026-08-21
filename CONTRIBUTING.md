# Contributing

For a material or hard-to-reverse engineering choice, start with a
**Decision proposal** issue before implementation.

A decision pull request must:

- use `decisions/0000-template.md`;
- have a unique, permanent decision ID;
- link the discussion issue;
- state problem, proposal, decision, short- and long-term impacts;
- name any decisions it supersedes;
- use qualified references for related decisions from linked decision sets;
- identify every broader decision it overrides and state the exact exception
  scope and rationale;
- update `decisions/README.md`;
- update both sides of any supersession relationship.

Decision records are historical artifacts. Amend minor errors in place, but use
a new decision to change engineering direction.

Do not use `supersedes` for a local exception to a broader decision. Use
`overrides`; the broader decision remains active outside the narrower scope.
