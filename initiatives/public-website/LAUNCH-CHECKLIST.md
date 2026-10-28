# Website Readiness and Human Release Checklist

**Status:** Proposed quality gates for Claude's first website implementation. Completion requires actual evidence, not AI assurances.

## Product and navigation
- [ ] Home, About, Projects, How We Build, Trust, Community, Handbook and Support routes tested
- [ ] Updates, privacy, accessibility, terms and 404 pages truthful and functional
- [ ] Mobile menu, links, anchors, project filters and contributor buttons tested
- [ ] Keyboard navigation, visible focus, no keyboard traps
- [ ] No placeholder copy, inert controls, invented stats or broken links

## GitHub content integrity
- [ ] Founding Charter v1.1 shown as approved with real source URL
- [ ] Governance, AI and unified handbook drafts clearly labelled **Not ratified**
- [ ] FileGuide status is **Discovery, no download**
- [ ] Existing five projects shown as **Intake pending** without false ownership/audit claims
- [ ] Familograph and RetroOS Portfolio omitted
- [ ] Any repository/release listed actually exists and has public rights/status evidence
- [ ] No private GitHub data is exposed in source or frontend bundles
- [ ] Pages show content last-verified dates where statuses might change

## Design and accessibility
- [ ] Meets the reviewed colour/typography system, contrast measurements documented
- [ ] Tested at narrow phone, tablet and wide desktop widths
- [ ] Functional with reduced motion; no blocking motion or autoplay
- [ ] Screen reader naming, headings, link purpose, controls and form semantics assessed
- [ ] Usability review by a real person recorded; no invented accessibility certificate

## Code and supply chain
- [ ] Open-source licence selected and compatible with actual source and dependencies
- [ ] Fonts, media and icons have appropriate rights/attribution
- [ ] TypeScript typecheck, lint and production build **actually run**
- [ ] Link tests, basic security/privacy checks and dependency audit performed
- [ ] Static site does not require unapproved proprietary runtime AI services
- [ ] No secret keys, tokens or personal data in Git history or deployed output
- [ ] Website README, AGENTS.md, CLAUDE.md and DEPLOYMENT.md reflect actual project state

## Hosting and payment safeguards
- [ ] Staging preview clearly separated from public production
- [ ] Real host/provider and last reviewed commit recorded
- [ ] HTTPS/custom domain/SEO/robots/sitemap reviewed as deployed
- [ ] No automatic production deployment outside authorised review path
- [ ] Stripe support UI is **disabled by default** and contains no fake checkout link
- [ ] For activation: legal payee, purpose, account eligibility, processor fees and recipient disclosures reviewed
- [ ] For activation: real Stripe Payment Link tested, receipt/return verified, human approval recorded
- [ ] No charitable status or tax deduction claims without evidence
- [ ] Rollback/withdrawal instructions tested and published for maintainers

## Release evidence
- [ ] GitHub PR with source diff, actual tests and limitations
- [ ] Screenshots of mobile, tablet and desktop from real running site
- [ ] Named human reviewer and approver
- [ ] Deployment decision and remaining risk recorded
- [ ] Site smoke-tested after deployment and URL verified

## Status

**Currently:** Concept specification prepared. **No website code, Stripe payment link, domain or deployment verified.**

A task is “done” only when it has evidence linked to an actual PR, test report or verified website.
