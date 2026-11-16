# Repository Migration Acceptance Checklist (Draft)

Use this checklist **per project**. Do not place sensitive values in public issues.

## Before migration

- [ ] GitHub repository/App source identified and owned by an authorised contributor
- [ ] Current GitHub visibility and Base44 sync status recorded
- [ ] Base44 backup/checkpoint created
- [ ] Secrets and sensitive assets checked; no accidental public exposure
- [ ] Dependencies, licences and intellectual-property rights reviewed
- [ ] Base44 Builder GitHub App installed/approved on Comutability
- [ ] No existing repository-name collision under Comutability

## Transfer/import

- [ ] Transfer existing repository via GitHub, or connect the unlinked app to a new **private** Comutability repository
- [ ] Preserve original history, branches, issues and tags when transferring
- [ ] Confirm new repository owner, expected name and visibility
- [ ] Verify Base44's reported GitHub repository, connection health and webhook status
- [ ] Check integrations, CI, deploy credentials, repository rules and collaborators
- [ ] After backup and verification, exercise a harmless documentation-only sync in a controlled manner
- [ ] Confirm production domain and existing user workflows still operate

## Before community adoption/public source

- [ ] Classify product maturity accurately: idea, prototype, alpha, beta, maintained
- [ ] Appoint accountable human maintainer(s)
- [ ] Choose a compatible recognised open-source licence
- [ ] Replace accidental secrets and address historical exposure; rotate credentials if needed
- [ ] Audit generated and third-party assets, including media rights
- [ ] Publish README, contribution guidance, security reporting contact and limitations
- [ ] Perform security and accessibility reviews proportionate to actual risks
- [ ] Record explicit decision to make source public and accept community contributions
- [ ] Link the approved entry from Comutability's public GitHub profile

Do not mark the project open source until the licence and public source are actually available.
