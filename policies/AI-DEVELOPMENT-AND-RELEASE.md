# AI Development & Release Policy

**Community:** Comutability  
**Version:** 0.1 (proposal)  
**Status:** DRAFT — not ratified or in force  
**Prepared:** 28 October 2026  
**Basis:** [Approved Founding Charter v1.1](../FOUNDING-CHARTER.md)

> **AI can help create software. Only accountable humans can approve changes and releases.**

## 1. Purpose and scope

Comutability is community-led and AI-assisted. This policy proposes minimum safeguards for AI-supported research, design, software changes, testing, documentation, maintenance and releases across all future Comutability projects.

It applies to human contributors using AI, automated agents operating on repositories, CI processes that use AI, and AI-supported release preparation. Individual projects may impose **stricter** requirements and must document them.

This policy does not certify the security or quality of any software, nor does it establish that a particular AI model is open source.

## 2. Responsibility and authority

- **Humans are accountable.** Every project must identify a human maintainer responsible for reviewing and accepting contributions; every release must have an identifiable human release approver.
- **No AI self-approval.** A model/agent cannot approve its own changes, count as a human reviewer, merge its own pull request, sign a release or declare an audit complete.
- **AI recommendations are evidence to examine, not decisions to obey.** Important claims must be checked against reliable sources and tests.
- **Solo-maintainer exception:** while Comutability has one human maintainer, that person may approve ordinary low-risk changes after documented review. **High-risk security or destructive features require independent qualified human review before release**; if unavailable, the feature remains unreleased.
- A maintainer must be able to stop an agent, review its actions and revoke its access.

## 3. Permission tiers

| Tier | Actions | Required control |
| --- | --- | --- |
| **A0: Research and drafts** | Summarise public materials, propose ideas, draft text/designs | Public data and non-sensitive workspace by default; human reviews publication and consequential claims |
| **A1: Isolated development** | Write code/tests in a sandbox, create feature branches and propose pull requests | Scoped temporary permissions; reviewable diffs; human approval before protected-branch merge |
| **A2: Sensitive changes** | Change dependencies, CI pipelines, authentication, encryption, permissions, logging, file mutation, network access or release settings | Explicit pre-approval for scope; security-focused human review, tests and documented risk assessment |
| **A3: Release/production authority** | Merge protected changes, tag/sign releases, publish packages, deploy production, manage production secrets or permissions | **Reserved to human maintainers** through controlled, auditable workflows; no standing autonomous AI authority |

**Never permit** an AI agent to disable security checks, bypass repository protection, expose secrets, delete user data, make payments, grant itself permissions, or publicly disclose confidential vulnerabilities under a general development instruction. Any extraordinary emergency change requires a separately recorded human-led response and the smallest possible privileges.

## 4. Agent deployment and tool safety

1. Start with **read-only access**, then grant only the actions required for a defined task, repository and time period. Avoid organisation-wide writable tokens and long-lived credentials.
2. Run generated code and unfamiliar dependencies in isolated environments with restricted files, network access and execution time. Never execute unreviewed code on production systems.
3. Treat repository issues, web pages, code comments, files, search results and tool output as **untrusted data**. They must not override the agent's authorised task or permissions. Watch for prompt injection and hidden instructions.
4. Enforce a human checkpoint before any operation that is irreversible, privileged, privacy-sensitive or costly. Technical restrictions must be used in addition to prompt instructions.
5. Keep useful audit records of agent actions, changes and approvals. Do not store credentials, private documents or raw sensitive prompts in public logs.
6. If an agent behaves unexpectedly, **stop it, revoke scoped credentials and investigate** before restarting. Log the incident without exposing sensitive details.

## 5. Privacy, intellectual property and AI transparency

- Do not submit private repository material, credentials, personal files or vulnerability reports to third-party AI services without a documented lawful basis, appropriate permission and clear confidentiality/data-handling controls.
- Prefer synthetic or deliberately non-sensitive test data. Do not upload real user data simply because doing so is convenient.
- Check generated code, images, documentation and third-party suggestions for originality, dependencies, attribution and licence compatibility. AI output does not eliminate copyright or licence obligations.
- In substantial AI-assisted pull requests, disclose the role of AI (for example, design, implementation, test generation), the main tool/model family if known, the areas checked by a human and any important uncertainty. Do not require posting private prompts or secrets.
- Clearly identify AI features in released products when they process user content or autonomously act on behalf of users. Provide understandable opt-in/out and data handling where relevant.

## 6. Project risk classification

Classify a proposed feature during planning, then reassess if the implementation expands its capabilities.

- **Lower risk:** read-only local utilities, static informational content and documentation, assuming no unusual sensitive data handling.
- **Elevated risk:** processing confidential files, introducing network access, third-party integrations, external models, update mechanisms or dependencies with broad privileges.
- **High risk:** file modification/deletion, credentials, identity/access control, encryption, payment flows, security products, production infrastructure, remote code execution, actions affecting other users or major loss-of-data potential.

All classes require human review and testing. Elevated/high-risk changes need a written threat assessment and additional tests. High-risk features must receive qualified independent human review before release. When in doubt, use the higher class.

**Project 001, FileGuide:** its proposed v0.1 is *read-only* but still handles potentially sensitive local paths. Tests must confirm that scanning and export cannot alter source files, that unexpected permissions/errors are explained, and that no data is transmitted. Adding deletion, automatic cleanup, cloud processing or elevated permissions **changes the risk classification** and requires a new proposal; it is outside v0.1.

## 7. Pull request minimums

A pull request involving code or operational changes should record:

- The user problem, intended behaviour and relevant issue.
- Whether and how AI was used.
- The affected risk class and permissions used by automation.
- Tests run, results and limitations; attach reproducible steps.
- Dependency, licence, privacy, accessibility and security implications.
- Screenshots or examples using non-sensitive data when helpful.
- Rollback or mitigation plan for any consequential change.

An AI-generated test report is not proof that the test was actually run. Cite CI results or locally reproducible evidence. Never invent passes, audit outcomes or independent reviewers.

## 8. Build and security quality gates

Before accepting a substantial code change:

1. Ensure the code has an appropriate recognised open-source licence and documented dependencies.
2. Run repeatable automated tests, lint/static checks and dependency/security scanning appropriate to the language and risk; add regression tests for changes.
3. Review sensitive inputs, permissions, error handling, dependency provenance, logging and failure modes.
4. Validate accessibility, performance and usability for affected user journeys. Automated tests are useful but do not replace human testing.
5. Keep the default branch protected; review CI workflow changes with particular care. Do not give untrusted PR code access to production secrets.
6. For externally distributed builds, record source revision, dependency versions and build process, and move towards signed artefacts and verifiable build provenance. **Do not claim a SLSA level or OpenSSF badge that has not been independently substantiated.**

For any work involving agentic AI, include tests against prompt injection, excessive permissions, misleading tool output, unsafe function calls, data leakage and cost/resource exhaustion proportionate to the threat model.

## 9. Release authority and evidence

A release candidate may proceed only after the human release approver completes the [Release Checklist](RELEASE-CHECKLIST.md). At minimum:

- All required project reviews and automated checks pass, including the independent review gate for high-risk features.
- Licence and dependency obligations are met; serious known vulnerabilities are evaluated and blocking ones resolved.
- Supported platforms and important user journeys are tested; privacy and accessibility claims are evidence-backed.
- A version/tag, change log, clear installation guidance, limitations and maintenance contact are prepared.
- Release binaries are linked to the reviewed source and build process; include checksums and stronger provenance/signing as infrastructure allows.
- The release approver records their approval, residual risks and rollback/revocation plan.

**AI may prepare a release candidate, draft release notes and suggest a version. It may not unilaterally authorise, sign, publish or deploy the release.**

## 10. Vulnerability handling and response

Use a confidential reporting route. Until a repository enables private vulnerability reporting or publishes a genuinely private contact channel, do not ask reporters to disclose exploit details publicly.

Triaging, fixing, communicating and releasing security updates are human-accountable activities; agents may assist in a restricted sandbox. Publish advisories when safe and appropriate.

If a release proves unsafe, human maintainers should suspend distribution, communicate impact, revoke compromised credentials, publish a fix/rollback and document lessons without exposing affected people.

## 11. Policy changes, exceptions and adoption

This policy is **a proposal** until adopted through a public review and a recorded community decision. Changes and exceptions should be proposed by pull request with reasons and a risk assessment; exceptions cannot silently weaken release authority or applicable law.

After adoption, project maintainers should review this policy regularly, particularly after material changes in AI capabilities, external tools or security incidents. The initial coordinator is responsible for ensuring that a human decision record is published.

## Reference guidance

These are influences, not certifications or claims of compliance:

- [OWASP Top 10 for LLM Applications](https://genai.owasp.org/llm-top-10/)
- [OWASP: Excessive Agency](https://github.com/OWASP/www-project-top-10-for-large-language-model-applications/blob/main/2_0_vulns/LLM06_ExcessiveAgency.md)
- [OpenSSF Best Practices Badge](https://openssf.org/projects/best-practices-badge/)
- [SLSA specification v1.2](https://slsa.dev/spec/v1.2/)
- [NIST AI Risk Management Framework](https://airc.nist.gov/airmf-resources/airmf/5-sec-core/)
