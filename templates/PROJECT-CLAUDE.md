# Claude Code instructions for <PROJECT NAME>

@AGENTS.md

**Source of truth:** `https://github.com/Comutability/<REPOSITORY>`  
**Status:** Copy/template; replace placeholders and verify actual environment before use.

### Before writing
1. Read the local README, LICENSE, build/test documentation and approved issue.
2. Consult Comutability's **ratified** charter and any applicable adopted [AI agent rules](https://github.com/Comutability/Community/blob/main/policies/AI-AGENT-OPERATING-RULES.md). Until those rules are merged, read the draft with the human maintainer and do not claim it is adopted.
3. Confirm one writer of record. If Base44 is connected, check its sync strategy first.

### Hard boundaries
- Work on an assigned feature branch and linked issue; preserve architecture and scope.
- Use **no secrets, real user data, production tokens, private vulnerabilities or unreviewed third-party assets** in model context or commits.
- Never approve your own PR, grant yourself repository permissions, merge protected branches, publish releases, deploy production, modify auth/payment/data rules or delete user data on your own authority.
- Test functionality and accessibility relevant to the task; report only checks actually run.
- Before introducing dependencies or proprietary AI runtime features, identify licences, data flows, costs and approved alternatives.
- Prepare reviewable PRs with AI-use disclosure, tests, security impact, risks and rollout/rollback notes.
- Ask the human maintainer when work is out of scope or high-risk.

### Local project specifics (human maintainer must fill)
- Stack and versions: <stack>
- Build: <verified command>
- Test: <verified command>
- Lint/format: <verified command>
- Core folders: <paths>
- Deploy ownership: <human role>; Claude **not authorised to deploy** by default
- Base44 sync (if applicable): <branch/writer-of-record and constraints>
