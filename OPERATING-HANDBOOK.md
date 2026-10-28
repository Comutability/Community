# Comutability Operating Handbook
**Community + Usability · Built together. Open to everyone.**

**Version:** 0.1 | **Status:** PROPOSED, not ratified | **Date:** 28 October 2026

This is the **single starting point** for everyone, including human contributors, the founder, ChatGPT-assisted planning, Claude-assisted implementation, and Base44 project teams.

> **Authority:** The [approved Founding Charter v1.1](FOUNDING-CHARTER.md) is binding community direction. This proposed handbook, its templates, and open draft PRs are **not approved governance or release policy** until accepted by a recorded decision. No AI tool gains permissions merely because a document names it.

## 1. Community map

- [Comutability GitHub organisation](https://github.com/Comutability): owns member access, repositories, teams and any future public code.
- [Community repository](https://github.com/Comutability/Community): **canonical home** for the charter, proposals, decisions, operating handbook and project register.
- [Organisation-wide `.github` repository](https://github.com/Comutability/.github): public-facing profile, reusable contribution guidance and GitHub forms. Shared files become defaults after merging to `main`.
- **Independent project repositories:** each application gets its own code, licence, README, tests, `CLAUDE.md` / `AGENTS.md`, maintainers and versioning. GitHub has no nested repositories: they live **under the organisation**, not physically inside `Community`.
- **External services:** ChatGPT, Claude and Base44 are separate services/tools, not Comutability-owned model source code, maintainers or policy authorities.

## 2. Who does what?

| Actor / system | Primary role | May propose? | May approve production release? |
| --- | --- | --- | --- |
| Founder / initial coordinator | Mission, intake, priorities, delegated permissions and decisions | Yes | Only as accountable human maintainer, following project risk gates |
| ChatGPT | **Ideas engine:** brainstorm, research, compare, specify, draft issues/docs | Yes, where connected/authorised | **No** |
| Claude / Claude Code | **Creative implementation agent:** UX, code, testing, refactors, documentation, PR drafts | Yes, with scoped repository access | **No** |
| Base44 | App builder/host and GitHub sync for designated Base44 projects | Yes, within project-specific owner controls | **No** |
| Selected community contributors | Ideas, documentation, design, QA, code and reviews | Yes | Only if explicitly appointed to a responsible human maintainer/release role |
| GitHub and CI | Source-of-truth, PRs, checks, decisions, releases, permissions/audit | Runs deterministic checks | **No**, CI success is not approval |

For more, see [roles and access](docs/ROLES-AND-ACCESS.md), [AI tools](docs/AI-TOOLCHAIN.md) and [delivery process](docs/DELIVERY-LIFECYCLE.md).

## 3. A change's complete journey

```text
Human idea / user problem
  ↓
ChatGPT creates a structured idea brief (advisory)
  ↓
Community issue → discussion → human prioritisation
  ↓
Approved project brief, acceptance criteria and risk classification
  ↓
Claude / selected human contributor creates feature branch
  ↓
Implementation, automated tests, docs, security/accessibility review
  ↓
Pull request with AI disclosure and evidence
  ↓
Human maintainer review → merge (subject to branch controls)
  ↓
Release candidate, security/quality checks, named human approval
  ↓
Public release, support, issue response and maintenance
```

Base44 projects run an additional **Base44 ↔ GitHub sync verification** step; changes can originate from the Base44 editor and must still be brought under the same review/release process as far as the platform supports.

## 4. Essential handbook chapters

1. [Architecture and repository map](docs/ARCHITECTURE.md)
2. [Roles, memberships and permissions](docs/ROLES-AND-ACCESS.md)
3. [ChatGPT, Claude, Base44 and GitHub workflow](docs/AI-TOOLCHAIN.md)
4. [Ideas-to-release delivery lifecycle](docs/DELIVERY-LIFECYCLE.md)
5. [Open-source licensing and proprietary AI boundaries](docs/LICENSING.md)
6. [Adding projects and migrating Base44 apps](docs/PROJECT-ONBOARDING.md)
7. [Security, data handling and release controls](docs/SECURITY-AND-RELEASE.md)
8. [How newcomers contribute](docs/GETTING-STARTED.md)
9. [Existing projects and intake status](docs/EXISTING-PROJECTS.md)
10. [Status and decisions register](docs/STATUS-AND-DECISIONS.md)

## 5. First-time contributor routes

- **I have an idea:** open a public issue using the proposal form after searching for duplicates; don't reveal secrets or private user information.
- **I want to use a tool:** follow the individual project's README, release status and installation instructions; do not assume a product exists just because it is listed.
- **I want to develop:** request a scoped issue, fork or create a feature branch, read local `CLAUDE.md`, show your tests and open a PR.
- **I want to use AI:** allowed, disclosed and reviewable; respect the project's approved risk/permissions. Never paste secrets into a model.
- **I want membership:** participation is open, but **write, maintain and admin access are invitation-only**, granted to selected people after trust and role checks.

## 6. Decision and project status

Approved: founding mission/ten principles, FileGuide selected **for discovery only**, establishment of GitHub organisation.

Still under review: [Governance PR #1](https://github.com/Comutability/Community/pull/1), [AI release policy PR #3](https://github.com/Comutability/Community/pull/3), [Existing project migration PR #4](https://github.com/Comutability/Community/pull/4). This unified handbook is a separate proposal, not a replacement for those decisions.

**Do not announce** community policies as ratified or unverified projects as open-source releases.

## 7. Immediate rollout

1. Review/ratify governance and this handbook with a public decision; establish private security reporting.
2. Enable default contributor files and issue templates in `.github` after review.
3. Set repository teams, rulesets, CODEOWNERS, private secret handling and human approval roles.
4. Invite a small number of trusted contributors with least-privilege access.
5. Select one pilot project; test the ChatGPT → issue → Claude → PR → human-review loop **without granting deploy/secrets permissions**.
6. Onboard existing Base44 projects only after ownership, licensing, backups and sync checks.
7. Publish the public website as an additional guide linked back to GitHub.

**Nothing in this guide installs or authorises ChatGPT, Claude, Base44 or external AI accounts automatically.**