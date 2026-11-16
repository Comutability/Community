# Website, Hosting and Deployment Rules for All Agents
**Version:** 0.1 · **Status:** Draft for adoption with COM-AI-001

## Principle
A public-facing site must represent the truth of its underlying project, link back to the correct Comutability repository once adopted and have an identifiable human deployment owner. A website is **not** proof that its product works.

## Required site metadata

Every hosted project maintains a `docs/DEPLOYMENT.md` (or equivalent) recording:
- Project slug, domain(s), environment(s) and hosted platform (e.g. Base44, static GitHub Pages, self-hosted)
- Source repository, deployed commit/release identifier and build or sync mechanism
- Named human maintainer and deploy approver (avoid personal credentials)
- Safe environment variables and a list of **secret variable names only**, never secret values
- Data residency/retention and external services; cookie/analytics practices
- Pre-deploy checklist, smoke tests, monitoring status, rollback/restore steps, known limitations and last verified deployment

## Content and UX consistency
- Keep Comutability's approved name/mission and links consistent while allowing distinct project branding.
- Use accurate maturity labels, supported platforms and installation links. Never advertise speculative features as working.
- Accessible design: keyboard functionality, meaningful labels, contrast and content hierarchy, focus states and reduced-motion choices when relevant.
- Responsive layout; check actual phone and desktop previews.
- Privacy: no unexpected trackers, forced logins or uploading user files without documented consent/need.
- SEO: sensible titles/descriptions, accessible link text, working canonical/public URLs and no fabricated reviews/testimonials.
- Preserve project-specific domain, auth, database and user state unless a human signs off on changing them.

## Proposed deployment sequence
1. Human-approved issue states intended behaviour and environment.
2. Claude/author implements on branch. Base44 author may propose changes only on a specifically assigned Base44 project.
3. Validate preview/staging with synthetic data; compare expected and actual behaviour, accessibility and performance.
4. CI plus human review, licence/security check and release documentation.
5. Named human approves production deployment; back up and have a rollback plan.
6. Deploy using scoped, authorised credentials in approved workflow.
7. Run post-deploy smoke checks and record exact live URL, revision, observed result and any gaps.
8. Document incident and rollback if tests fail.

## Base44-specific safety
- Base44 app GitHub sync and domain/deploy operations are **not automatically governed** by a GitHub PR policy. Identify whether the builder auto-pushes to default branch; verify its actual behaviour before claiming enforced review.
- Base44 Builder needs its own GitHub App authorisation in Comutability, separate from ChatGPT/Claude.
- Do not disconnect or migrate active apps without checkpoints and sync verification.
- When using Base44 AI builder, include the approved per-app rules in its request and verify the output; it may not load the repository's `AGENTS.md` automatically.
- Do not change production auth, domain, payment, encryption or real user data based on a generic AI request.

## Failure states and honesty
Use `not started`, `in progress`, `preview verified`, `deployed and smoke-tested`, or `blocked`. **Never call an unverified preview “live and working”.**

Related: [Security and releases](SECURITY-AND-RELEASE.md), [AI agent rules](../policies/AI-AGENT-OPERATING-RULES.md).
