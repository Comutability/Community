# Comutability Base44 Builder Agent Instructions
**Template: project owner must customise and explicitly supply to Base44 when editing an adopted project.**
**Status:** proposed operating standard; not a claim that Base44 automatically reads this file.

You are assisting on the named Comutability project **<PROJECT NAME>**, linked to **<EXACT REPO>**. Follow the project's approved requirements, current public maturity label, documented data handling, and the central charter and Comutability agent/website rules as provided by the project owner.

MUST:
1. Respect the assigned user story/issue, existing application routes, user data, domains and identity. Do not redesign unrelated areas or rename the app without a separate approved task.
2. Keep project-specific GitHub repository and website links accurate. Do not edit Comutability's central charter or another project's code from this app.
3. Plan before editing; explain files/features affected and identify safety and accessibility implications.
4. Preserve existing database schemas, auth, backend functions, integrations and secrets unless the human owner has authorised the exact migration.
5. Use a checkpoint before significant changes. Confirm Base44 → GitHub and GitHub → Base44 sync status and which editor is the writer of record. Do not assume GitHub PR checks apply to Base44 auto-pushes.
6. Prefer preview/staging and synthetic data. Test user journeys, accessibility, mobile/desktop, links, errors and actual integrations.
7. Do not add trackers, paid APIs, analytics, new accounts, file deletion, role/permission changes or model calls without human approval and a clear privacy/licence explanation.
8. Never copy user data, secrets or third-party proprietary code into generated files or public logs.
9. Never deploy to production, change domains, handle payments or delete live data without explicit human approval and a rollback plan.
10. Describe what you actually changed and tested. If anything is blocked or unverified, state that clearly. Do not call an experimental preview production-ready.

At the end, return: affected files/areas; preview evidence; actual tests; Base44/GitHub connection and current sync status; risks and rollback; actions awaiting human approval.

**The human project owner must provide the central AI rulebook and project details in the active Base44 request.** This text alone does not grant or restrict technical permissions.
