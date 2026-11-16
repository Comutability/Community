# End-to-End Project Lifecycle
**Status: proposed operating process.**

## 0. Discover

A user, founder or contributor raises a real problem. ChatGPT may help research, but validate the premise through interviews and existing open-source alternatives. Issues stay labelled `idea` until human triage.

## 1. Propose

Use the [project proposal template](../templates/PROJECT-PROPOSAL.md): problem, users, competitor/upstream alternatives, value, requirements, non-goals, privacy/accessibility risks, licence implications and target maintainers. No prototype required to suggest an idea.

## 2. Select

A human maintainer/coordinator records the decision with status, conditions and a linked issue. Selection is not a delivery promise. **FileGuide remains the first new application selected for discovery**, not an implementation-ready release.

## 3. Design and plan

Draft a tested specification, UI acceptance criteria, architecture, dependency risk, data handling and release tests. Scope a small vertical slice. For high-risk/authentication/medical/payments/data-deletion changes, require threat modelling and specialist review plans before coding.

## 4. Build with Claude or a human

- Link approved issue to a feature branch.
- Read project `CLAUDE.md` and `AGENTS.md`.
- Make limited, reviewable changes and explain significant AI assistance.
- Run actual tests, record commands/results and describe missing tests.
- Generate documentation, licences/attributions and migration notes as needed.

## 5. Review in GitHub

PR requires human review of code, test evidence, security and licensing; a responsible person checks accessibility and usability. CI is supporting evidence, not permission. Reviewers must not simply approve an AI-generated summary.

## 6. Release gate

Verify version and change log, reproducible/reviewed artifacts, dependency scan, vulnerability contact, install instructions, supported-platform testing, rollback/withdrawal procedure and named human release approval. Higher-risk features need appropriately independent qualified review. Do not claim certification not earned.

## 7. Maintain

Record bugs and vulnerabilities, publish security updates safely, document deprecations, track accessibility improvements, reassess dependencies and plan maintainer succession.

## 8. Archive or transfer

If abandoned, archive honestly rather than implying active support. Transfer community projects only with a documented licence/IP review, governance decision and operational continuity plan.

## Change types

- **Documentation-only:** small scoped checks, human review.
- **Normal code:** tests + security/dependency review relevant to impact.
- **High-risk:** independent qualified human review, threat model and release evidence.
- **Base44-linked:** also verify builder sync and actual deploy state.

**Stop conditions:** missing rights, unsafe data handling, unverified production security, AI overreach, unavailable high-risk reviewer or absent rollback plan. Record why work was deferred.

See [AI policy draft](https://github.com/Comutability/Community/pull/3).