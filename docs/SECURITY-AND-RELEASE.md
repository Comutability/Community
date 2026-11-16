# Security, Access and Releases
**Status: operational recommendations; detailed formal AI/release policy is still proposed in PR #3.**

## Human decisions and least privilege

- All project scope and release decisions require named, accountable humans.
- Treat ChatGPT and Claude as assistants, not organisation owners or human approvers.
- Set vendor integrations **individually** (ChatGPT GitHub App, Claude Code GitHub credentials, Base44 GitHub App). Give each only necessary repos/scopes. No blanket cross-org write rights.
- Never put API keys, secrets, session tokens, signing keys or customer data in repository files, issue bodies, model prompts, build logs or public previews.
- When removing a contributor, revoke GitHub teams, SSH keys, actions tokens, Base44 app access and relevant external accounts independently.

## Risk levels

- Low: docs, public research, read-only non-sensitive examples.
- Medium: handling user files, new network calls, packages, access to private projects.
- High: deletion/mutation of user data, authentication, encryption, payments, agent permissions, production deployment.

Test proportional to risk. High-risk projects need a threat model and appropriately qualified independent human review before public release; if unavailable, defer the risky functionality.

## Pull request/release workflow

- Branch and PR preferred for reviewable code changes.
- GitHub Actions may check lint, unit tests, dependencies, accessibility checks and build reproducibility.
- An AI summary or green CI result is **not** evidence that an independent security review occurred.
- Human release approver records version, changelog, dependencies, tested environments, privacy/known issues and rollback.
- Keep signing keys separate from AI workspaces and untrusted PR builds.
- Protect main against deletion/force pushes; expand PR approval requirements once reviewers and builder sync are ready.

## Vulnerabilities

Enable **private vulnerability reporting** per GitHub repository or establish a verified private contact method. **Until then do not solicit exploit detail through public issues or post an invented contact address.** A public `SECURITY.md` may state this limitation.

Escalate high-impact issues to the human maintainer, contain access, document communication, rotate affected secrets and issue an accurately labelled security release.

## Project-specific examples

- **FileGuide v0.1:** source files are never deleted, renamed or modified.
- **Commonveil / Veil Social:** independently review identity, encryption and recovery claims.
- **Mandatera:** maintain explicit human approval for financial/privileged agent actions.
- **Lantern OS:** verify actual boot/security claims on real systems before release promotion.
- **Monster Realm:** review rights to character images, music and third-party game assets.

See [AI policy PR #3](https://github.com/Comutability/Community/pull/3) and [governance PR #1](https://github.com/Comutability/Community/pull/1).