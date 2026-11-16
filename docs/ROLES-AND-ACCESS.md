# Human Roles and Access
**Status: proposed. Selected member invitations have not yet been issued.**

## Roles

**Founding coordinator:** maintains founding mission, selects priorities, oversees organisation administration and records decisions. Not an exception to security review.

**Organisation owners (minimum ideally two trusted humans):** control GitHub membership, billing and application installation. Keep numbers small, use MFA/passkeys and audit permissions. Never appoint an AI as an organisation owner.

**Project maintainer:** owns project scope, code review, issue triage, dependencies, security response, testing and releases. Must be a named human and understand the project's risk.

**Reviewer/triager:** may help with issues, docs, testing and review without unrestricted write permissions. A review comment is not formal approval unless authorised.

**Contributor:** proposes ideas or code via issues, forks and PRs. Public participation does not require membership; access to private source is invited and separately reviewed.

**AI tools and builders:** service identities or tools that act only within explicitly scoped permissions. Do not give them human role titles or independent policy authority.

## Membership ladder (proposal)

| Level | How to join | Access |
| --- | --- | --- |
| Public participant | Anyone | Read public projects, issues/PRs and contribute via forks |
| Trusted triager | Selected and invited after demonstrated participation | Triage named repositories, no secrets |
| Project contributor | Invited for a named project | Write to specified branches/repos only when needed |
| Project maintainer | Explicitly appointed after review | Maintain/review/release specific project per policy |
| Organisation owner | Rare, explicit trust decision | GitHub administration; not routine implementation |

## Invitation and offboarding process

1. Contributor participates publicly, agrees to conduct/privacy rules, and nominates a project.
2. Maintainer documents role, repository scope, permissions, training, review owner and expiration/review date.
3. Organisation owner sends GitHub invite with the **minimum** required team permissions; no blanket access to all repositories.
4. Onboarding covers 2FA/MFA, confidentiality, source licensing, use of AI and safe incident reporting.
5. Review membership regularly; revoke stale access quickly. On exit, remove credentials, app tokens and privileges and rotate secrets if exposed.

## Decision rights

- Founder/coordinator: initial scope and priority proposals.
- Maintainers: day-to-day project decisions under published rules.
- Community: public consultation and feedback on significant changes.
- AI: may provide options but **cannot cast votes or satisfy human approval**.
- Releases: named human maintainer; high-risk projects require independent qualified review per the proposed AI policy.

Governance PR #1 is still pending. **This document is a suggested implementation, not enacted membership policy.**