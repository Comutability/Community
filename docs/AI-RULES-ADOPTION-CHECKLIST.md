# AI Agent Rules Adoption and Enforcement
**Status: draft rollout plan. This list is not evidence that controls are already configured.**

## Central approval
- [ ] Review [COM-AI-001](../policies/AI-AGENT-OPERATING-RULES.md) and website/deploy companion standard.
- [ ] Reconcile with existing Governance PR #1 and AI/release PR #3.
- [ ] Decide DCO/licensing policies and confidential security-reporting channel.
- [ ] Record founder/community human approval and effective version in `decisions/`.
- [ ] Merge rules into `Community/main` after approval, then update public handbook links.

## Every project repository
- [ ] README identifies owner, scope, release status, source and licence.
- [ ] Copy the reviewed `AGENTS.md` and `CLAUDE.md` templates **locally**, and ensure an AI operator can read the current ratified central rulebook.
- [ ] Create local `docs/DEPLOYMENT.md` if any website or deployment exists.
- [ ] Configure GitHub branch protection, PR review, limited App access and CI; do not pretend docs enforce these.
- [ ] For GitHub Copilot, optionally put reviewed guidance at `.github/copilot-instructions.md`; do not assume copying it only into organisation `.github` propagates to each repo.
- [ ] Configure Claude Code project permissions and suitable `.claude/rules/` files if needed; do not store secrets in them.
- [ ] Identify the **writer of record** for Base44-linked repos and test sync/review controls.
- [ ] Test a harmless draft issue → feature branch → Claude PR → human review cycle.

## Human audit
- [ ] Run two test prompts: one legitimate scoped change and one out-of-scope privileged request. Confirm the agent refuses/defers the latter.
- [ ] Verify CI/test evidence and no unapproved production deploy.
- [ ] Review permissions/tokens after each new member or third-party GitHub App installation.
- [ ] Record date, maintainer and findings; repeat after major agent/tool changes.

## Scope note
All external project repositories presently outside Comutability are **not** automatically controlled by these rules. Their AI tooling and Base44 sync must be separately configured after safe transfer or authorised adoption.

Related: [Operating Handbook](../OPERATING-HANDBOOK.md), [Project Onboarding](PROJECT-ONBOARDING.md).
