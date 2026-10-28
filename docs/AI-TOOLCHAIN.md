# Working with ChatGPT, Claude, Base44 and GitHub
**Status: proposed. Tool names describe services, not a claim of ownership or access.**

## Shared AI working rules

All project work should be prepared against [COM-AI-001](../policies/AI-AGENT-OPERATING-RULES.md) and the [Website & Hosting Rules](WEBSITE-AND-HOSTING-RULES.md), both **proposed until ratified**. Use [Project AI Handoff](../templates/PROJECT-AGENT-HANDOFF.md) to transfer an approved issue from ChatGPT to Claude. The [Base44 Builder Rules template](../templates/BASE44-BUILDER-AGENT-RULES.md) must be explicitly supplied for designated Base44 changes; do not assume Base44 auto-loads GitHub markdown files.

## Roles and responsibility boundary

| System | Job | Inputs | Outputs | Limits |
| --- | --- | --- | --- | --- |
| **ChatGPT, OpenAI** | **Ideas engine**: discover problems, research, assess alternatives, prioritise, draft briefs/specs/review checklists | Founder/user problem and non-sensitive project context | Issue proposals, project briefs, acceptance criteria, risk notes | Advisory only; no automatic approval |
| **Claude / Claude Code, Anthropic** | **Creative & engineering agent**: UX, code, architecture, tests, accessibility work, docs, refactoring | Approved issue, repo instructions and scoped GitHub access | Feature branch, changed code, tests, PR, honest test evidence | No independent merge/release; permission-scoped |
| **Base44** | Builder/hosting/editor for **designated Base44 projects**, with its own GitHub sync | Project-specific requirements and app permissions | App code, preview, deployment, GitHub sync if connected | Not the organisation-wide authority; don't overwrite Claude changes |
| **GitHub** | Canonical source, decisions, issues, reviews, releases, team ACLs | All approved work and evidence | Auditable source history | CI alone is not human approval |
| **Humans** | Mission, decisions, reviews, security, rights, acceptance and releases | Evidence from tools and community | Authorised change and accountability | Must verify claims rather than rubber-stamp AI |

No vendor's model, model weights, system prompts, training data or proprietary service code is provided by Comutability. Publishing our prompts or workflows is optional where non-sensitive; our project source code must be openly licensed.

## Handoff 1: ChatGPT → GitHub issue

Ask ChatGPT for an **idea packet**:
- Problem, target users, competitors (including contributing upstream), accessibility needs
- Proposed small release, out-of-scope behaviours, risks, privacy requirements
- Testable acceptance criteria, open questions, initial licence assumptions
- Links to verified research, confidence level, no invented test results
- Suggested GitHub issue body and status `proposal`

A human checks and posts it. If a connected ChatGPT GitHub action is authorised it may draft an issue directly, but **that action is not automatically approved product scope**.

## Handoff 2: GitHub approved issue → Claude

Human maintainer marks the issue ready and specifies the target repository and expected acceptance criteria. Claude reads `CLAUDE.md`, `AGENTS.md`, README, relevant code and test instructions. It works on an isolated feature branch with scoped permissions, proposes testable changes, records AI involvement and opens a PR. It must ask for approval for expanded scope, secrets, data deletion, network access, privileged commands or costly operations.

**Suggested Claude task:** "Implement issue #N in this repository. First read CLAUDE.md and AGENTS.md. Preserve behaviour outside scope. Do not deploy, merge, rotate secrets or mutate user data. Write or update tests and docs, report what actually ran, open a PR and list any unresolved risks."

## Handoff 3: Base44 ↔ GitHub

For apps built or hosted in Base44, **do not assume** GitHub changes automatically deploy safely or that the Base44 editor respects pull-request requirements. The person responsible for that app chooses one controlled workflow:

1. Confirm the actual GitHub connection, owner, branch and webhook in Base44.
2. Take an app checkpoint and assess whether Base44 sync writes straight to `main`.
3. Route proposed changes through review where supported. If sync bypasses reviews, treat incoming code as **unreleased** until human verification; consider a staging fork/branch rather than pretending it follows normal PR flow.
4. Confirm deployed URL, authentication, environment variables, backing services and data safety.
5. Reverify after repository transfer or permission changes.

Base44's GitHub App access is **separate** from the ChatGPT and Claude GitHub connections. Explicitly authorise each, with least privilege. ChatGPT connection success does not authorise Base44.

## Handoff 4: Human review and release

Review actual diffs and CI evidence. Apply risk-based QA, accessibility and licence checks; approve then merge using repository protections. A named human authorises release. Claude may prepare notes and packages but never claim production authorisation.

## Avoid tool conflicts

- Only one tool/editor should be the **writer of record** for an individual file/branch at a time.
- Use GitHub PRs instead of copying AI chat text over production code.
- Never place API keys in `CLAUDE.md`, `AGENTS.md` or ChatGPT prompts.
- Record vendor dependencies and costs. Projects with optional vendor AI must remain useful without forced proprietary lock-in when promised.

See [workflow](DELIVERY-LIFECYCLE.md), [licensing](LICENSING.md) and [security](SECURITY-AND-RELEASE.md).