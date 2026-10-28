# Comutability Release Checklist

**Status:** Proposed template; not adopted until the AI Development & Release Policy is ratified.  
**Use:** Copy into an issue or release pull request. Fill in evidence and a named human approver.

## Identity

- [ ] Product/repository and release version are identified.
- [ ] A named **human** maintainer owns the release decision.
- [ ] Changes and supported platforms are listed.
- [ ] AI involvement in this release is summarised accurately.

## Review and security

- [ ] Feature risk classifications have been reviewed and documented.
- [ ] Any high-risk feature has **qualified independent human review**; otherwise the feature remains unreleased.
- [ ] Relevant pull requests have human-reviewed diffs and no unresolved blocking concerns.
- [ ] Branch rules, CI workflow changes and permissions have been checked.
- [ ] Threat assessment, privacy review and required security tests have been completed.
- [ ] Serious known vulnerabilities and dependencies have been assessed.
- [ ] Sensitive details and credentials are absent from builds and logs.

## Functional and human testing

- [ ] Automated tests and checks ran successfully; record links or reproducible commands.
- [ ] Critical failure and error paths were tested.
- [ ] Accessibility and usability were reviewed on actual supported platforms.
- [ ] Installation, upgrades (if applicable) and rollback/removal were tried.
- [ ] For FileGuide v0.1: verify **no writes, moves or deletions of source files** and **no uploads**.

## Software freedom and distribution

- [ ] Appropriate open-source licence and dependency obligations are confirmed.
- [ ] Version, source revision and build inputs are recorded.
- [ ] Release notes explain changes, limitations, compatibility and known issues.
- [ ] Downloads match the reviewed source; provide hashes and provenance/signatures where implemented.
- [ ] User documentation, support status and private vulnerability-reporting route are available.
- [ ] No unsupported claims of independent audit, accessibility certification, OpenSSF badge or SLSA level appear.

## Human release decision

- [ ] Named human release approver: __________________
- [ ] Approval date/time: __________________
- [ ] Evidence links: __________________
- [ ] Residual risks/known limitations: __________________
- [ ] Rollback or withdrawal plan: __________________
- [ ] **Approved / Rejected / Deferred** (choose one): __________________

**A green CI check or an AI-generated statement is not release approval.**
