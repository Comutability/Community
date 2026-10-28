# Existing Projects: Proposed Comutability Adoption

**Status:** Draft for discussion, not an adopted project roster  
**Prepared:** 28 October 2026  
**Purpose:** Assess existing Base44 projects for transfer of their GitHub code into Comutability while preserving working deployments and personal ownership rights until explicitly agreed.

Comutability's **first newly selected application concept** remains [FileGuide](projects/001-fileguide/PROJECT-BRIEF.md), in discovery. The projects below are **pre-existing candidates for community stewardship**, not automatically approved, audited, open-source or production-ready.

## Proposed intake

| Project | Community category | Repository situation | Intended initial treatment |
| --- | --- | --- | --- |
| **Commonveil** | Privacy and communication | Base44 app; not connected to GitHub | Export to a new **private** Comutability repository after reviewing code and permissions |
| **Monster Realm: Social Quest** | Games and creativity | Base44 app connected to a personal GitHub repository | Transfer existing private repository without renaming during initial migration; preserve history |
| **Lantern OS** | Systems, education and accessibility | Base44 app; not connected to GitHub | Export to a new **private** Comutability repository; distinguish website/concept from tested OS |
| **Veil Social** | Privacy and communication | Base44 app connected to a personal GitHub repository | Transfer existing private repository without renaming; review security and relationships to Commonveil |
| **Mandatera** | AI, agents and automation | Base44 app connected to a personal GitHub repository | Transfer existing private repository without renaming; scrutinise authorisation, payments and agent permissions |

**Explicit exclusions:** FAMLIOGRAPH/Familograph and RetroOS Portfolio are not part of this intake. Do not copy their code, accounts or branding.

## Relationship to the community

- Community collaboration must be **opt-in and transparent**. A repository under Comutability does not transfer copyright or guarantee that a project is safe or ready for general use.
- Do not represent existing Base44 landing pages or prototypes as independently tested production releases.
- Keep project-specific names and URLs at first. Do not automatically merge projects or conflate **Commonveil** and **Veil Social**.
- Clarify the current distinction between **Monster Realm: Social Quest** in Base44 and the **Neon Frontier** branding shown on its preview before publishing its identity in a public catalogue.
- A project becomes **community-maintained** only after a maintainer, scope, open-source licence, contributor rules, security contact and support status are recorded.

## Migration prerequisites

1. Verify the founder is authorised to transfer each repository and that its code and assets may be contributed.
2. Install/approve the **Base44 Builder GitHub App** for the Comutability organisation. ChatGPT's GitHub App is a **separate** installation.
3. Review the exact repository contents for secrets, personal information, sensitive configuration, generated content and third-party licences.
4. Capture a Base44 checkpoint/backup and record the current functioning published site and integration state.
5. Preserve existing GitHub history and visibility. Do **not** make repositories public during the transfer.
6. Migrate **one project at a time**; record repository owner, current Base44 connection, webhook state and an acceptance checklist.
7. Transfer existing personal repositories using GitHub's repository **Settings → Danger Zone → Transfer**, then verify GitHub and Base44 connections on the new owner. Do not assume sync survives the change.
8. For Base44-only projects, use Base44's official **Connect to GitHub** function to create a new private Comutability repository after the organisation is available in Base44.
9. Recheck CI, branch protection, team permissions, GitHub App permissions, domains, deployment secrets and webhook configuration. Ensure future updates are pushed to the **correct** new repository.
10. After a licence, data and asset audit, decide separately whether/when each repository can be made **public open source**, with documented limitations and a named maintainer.

## Risk gates by project

- **Commonveil / Veil Social:** authentication, encryption, account recovery, device trust, user privacy and secure vulnerability disclosure require qualified external review before public security claims or release promotion.
- **Mandatera:** agent authority, secrets, financial actions, integrations and human approval controls require a threat model and independent security review.
- **Lantern OS:** avoid claiming an independently bootable or tested Linux distribution until actual device/VM verification exists.
- **Monster Realm:** confirm ownership/licensing of code, artwork, music, names and character designs; verify whether any third-party trademarks or assets require changes.

## Current status and next actions

**No repository transfer, disclosure of private source, change of code ownership or live deployment changes have been performed by this draft.**

- [ ] Comutability installed and authorised in **Base44 Builder** as a GitHub destination.
- [ ] Transfer and verify Monster Realm: Social Quest.
- [ ] Transfer and verify Veil Social.
- [ ] Transfer and verify Mandatera.
- [ ] Create and verify Commonveil source repository.
- [ ] Create and verify Lantern OS source repository.
- [ ] Review licences, secrets and community-maintainer requirements project by project.
- [ ] Decide whether to merge this proposal and publish a community portfolio.

## References

- [Comutability Founding Charter](FOUNDING-CHARTER.md)
- [Draft AI Development & Release Policy, PR #3](https://github.com/Comutability/Community/pull/3)
- [GitHub repository transfer guidance](https://docs.github.com/en/repositories/creating-and-managing-repositories/transferring-a-repository)
- [Base44 GitHub integration overview](https://base44.com/blog/base44-github-integration)
