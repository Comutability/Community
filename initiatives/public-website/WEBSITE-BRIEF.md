# Comutability Public Website: Creative and Product Brief

**Version:** 0.1 · **Status:** Proposed website concept for Claude implementation · **Date:** 28 October 2026  
**Initiative:** Public community website · **Suggested future code repository:** `Comutability/website` (not created yet)  
**Founding promise:** **Built together. Open to everyone.**

## The intention

Build a memorable, accessible, genuinely useful public home for **Comutability (Community + Usability)**, an independent, community-led, AI-assisted open-source software initiative. The website should explain **what we believe, what we are building, how AI helps, how humans check it, how anybody can help and how people can support the community financially**.

This is **not** a corporate homepage, an AI chatbot product, a mock “AGI company”, or a replacement for GitHub. It is an inviting discovery, learning, contribution and transparency layer over the **canonical GitHub organisation** at https://github.com/Comutability.

### Non-negotiable truthfulness

- The **Founding Charter v1.1** is approved: https://github.com/Comutability/Community/blob/main/FOUNDING-CHARTER.md
- **FileGuide** is selected for **discovery**, not built/released: https://github.com/Comutability/Community/blob/main/projects/001-fileguide/PROJECT-BRIEF.md
- Existing Base44 projects **Commonveil, Veil Social, Mandatera, Lantern OS and Monster Realm: Social Quest** are **intake candidates**, not automatically adopted, audited, open-sourced or released through Comutability. Do not mark them as available downloads. The *Neon Frontier* branding visible in the Monster Realm preview still needs reconciling.
- **Exclude FAMLIOGRAPH/Familograph and RetroOS Portfolio** from the Comutability project catalogue.
- Governance, unified operating handbook, AI rules and release policy exist as **draft pull requests**, not ratified policies: [governance #1](https://github.com/Comutability/Community/pull/1), [AI release #3](https://github.com/Comutability/Community/pull/3), [adoption #4](https://github.com/Comutability/Community/pull/4), [unified operating handbook #5](https://github.com/Comutability/Community/pull/5).
- Project repositories and production release evidence should come only from actual authorised public GitHub data. Do not invent star counts, download counts, testimonials, badges, contributors, vulnerability audits or installed integrations.
- **Only humans** decide community rules, review substantial changes and authorise releases. ChatGPT/Claude/Base44 do not hold human approval authority.

## The brand story

**Name:** Comutability (Community + Usability).  
**Primary strapline:** Built together. Open to everyone.  
**Homepage headline:** Good ideas deserve to become useful tools.  
**Supporting message:** People bring problems and ideas. AI helps research, design and develop solutions. Humans review, test and maintain them. We share our software openly so others can benefit and contribute.

**Positioning:** An accessible, trustworthy open-source community that uses AI transparently as a development tool, not as a substitute for human responsibility. It builds *useful software across different categories*, not just AI applications.

Tone: warm, practical, intelligent, welcoming, independent and grounded. British English. Explain technical terms. No hype, false promises, made-up metrics or corporate jargon. Avoid em dashes in public copy.

## Audience and questions the website answers

1. **Curious visitor:** What is this? Who is it for? Why should I trust it?
2. **Person seeking software:** What can I use today? Is it genuinely open-source? What does it cost? Is the project maintained?
3. **Nontechnical contributor:** Can I suggest an idea, test an app, translate a guide or help without coding?
4. **Developer/AI agent user:** How do I clone a project, read the rules, work on an approved issue and submit an auditable PR?
5. **Reviewer/security researcher:** Where is the code, licence, build/test evidence, security route and known limitation?
6. **Supporter:** How would financial support be used and who actually receives the payment?

## Sitemap and expected page features

| Route | Primary purpose | Key content/actions |
| --- | --- | --- |
| `/` | Inspirational, factual home | Hero, four-step animated pipeline, selected project previews with real status, human-verification section, contribution paths, support CTA |
| `/about/` | Mission and people | Community story, ten charter principles, independence and human responsibility, link to approved charter |
| `/projects/` | Public project directory | Categories, filter by **verified status**, search, source/maturity badges, exclude private repositories, no fake releases |
| `/projects/[slug]/` | Project detail | Problem, audience, exact status, roadmap, licence only if approved, verified repository/releases if present, participation and known limits |
| `/how-we-build/` | AI/human development pipeline | ChatGPT ideation, GitHub issue, Claude implementation, Base44 on designated projects, testing/PR, human sign-off, maintenance |
| `/trust/` | Evidence over claims | What counts as checked, audit/test evidence with links, privacy/security/accessibility, known limitations, no misleading certifications |
| `/community/` | People and participation | Ways to help, GitHub walkthrough, member/maintainer roles, issue and PR etiquette |
| `/handbook/` | Rules and governance index | Approved charter, proposed rules with **draft** states, licensing approach, direct GitHub document links, decision history |
| `/support/` | Financial transparency | Funding purposes, recipient identification, contribution options via verified Stripe link, fees/currency/tax disclosure, privacy |
| `/updates/` | Human-edited news/release notes | Dated updates sourced from canonical repos; no fabricated AI news |
| `/privacy/` | Privacy explanation | Analytics/cookies, third-party links, GitHub/Stripe transitions, retention/contact as actually deployed |
| `/accessibility/` | Accessibility statement | Targets, tested features and known limitations, feedback route |
| `/terms/` | Legal/terms where applicable | Accurate maintainer/recipient, software disclaimers, jurisdiction after actual determination |
| `/404/` | Useful not-found | Friendly error and real navigation to home/projects/handbook |

**MVP can implement routes in stages.** Home, About, Projects, How We Build, Trust, Community, Handbook and Support are priority.

## Homepage storytelling flow

1. **Top navigation:** Comutability logotype, Projects, How We Build, Community, Handbook, Support; accessible mobile menu; GitHub icon linking to actual org.
2. **Hero:** “Good ideas deserve to become useful tools.” Clear summary; CTAs **Explore the projects** and **Join the community**. Secondary GitHub link.
3. **Interactive concept diagram:** “Imagine → Create → Verify → Share”. Clicking each segment provides a plain-language explanation and the responsible AI/human actor. Motion reduced/disablable.
4. **Featured projects:** A verified **FileGuide: discovery** card, plus optional “existing project intake” cards, each explicitly labelled with current state and no fake download button.
5. **How the team works:** ChatGPT = ideas, Claude = engineering, Base44 = designated app builder/host, GitHub = source of truth, Human maintainers = quality and release authority.
6. **“Evidence, not promises” panel:** pull requests, actual tests, licences, audit limitations and human sign-off explained. Live-looking data only if backed by a real source.
7. **Ways to contribute:** “Suggest an idea”, “Help test”, “Write or translate”, “Design”, “Code”, “Review”. Each routes to actual GitHub guidance.
8. **Shared values:** community-first, accessibility, transparency, privacy, true open-source and maintainability.
9. **Financial support:** transparent costs and support CTA. Do not enable paid checkout until Stripe recipient/eligibility verified.
10. **Footer:** governance/doc links, source code, privacy/accessibility, project status, service disclosure, and “Built together. Open to everyone.”

## Interactions that add genuine value

- Project filters and search backed by **static, reviewed metadata**; no unreliable live API required in the browser.
- A clickable **idea-to-release timeline** with an expandable human review checkpoint.
- An honest **release evidence checklist** showing what “code reviewed”, “CI passed”, “human tested” and “independently audited” actually mean, and the difference between them.
- A simple **contributor route chooser** that directs users to the appropriate real GitHub issue form/README rather than collecting sensitive data in an invented member portal.
- Accessible theme toggle and reduced-motion respect; interactions should enhance, not block reading.
- Optionally later: build-time GitHub project sync, real release feed and verified contributor credits. These are not launch blockers.

## Design identity

- Mood: **open-source workshop meets modern digital commons**. Human, optimistic and credible; distinct enough to recognise at a glance.
- Primary dark surface: `#101A25`; secondary dark `#1B2937`; off-white `#F7F8F5`; muted steel `#AAB9C5`; bright teal `#42D9BA`; warm peach `#F2B58D`.
- Use a clean accessible sans serif (for example, a self-hosted, appropriately licensed open font); optional restrained monospaced labels for technical metadata.
- Strong headings, readable long-form layouts, generous spacing, visible focus indicators, variable card borders, subtle dotted-grid/orbit/connection lines and authentic diagrams instead of stock “robot” art.
- Bright, considered light mode. Ensure **contrast is actually measured** for content, controls and status chips.
- Generous mobile design and comfortable touch targets. Avoid decorative endless carousels and excessive animations.
- Make the design *feel built together*: connection nodes, code and contribution trails, human proof marks. Do not invent a formal logo or certify a badge without approval.

## Project statuses and featured catalogue

| Project | Website status | Important warning |
| --- | --- | --- |
| **FileGuide** | **Discovery** | Concept selected, no application repo/download yet |
| **Commonveil** | **Existing project: intake pending** | Existing Base44 project, not officially adopted by Comutability |
| **Veil Social** | **Existing project: intake pending** | Auth/encryption claims need review |
| **Mandatera** | **Existing project: intake pending** | Agent permissions and financial operations are security-sensitive |
| **Lantern OS** | **Existing project: intake pending** | Do not claim a bootable, tested distribution |
| **Monster Realm: Social Quest** | **Existing project: intake pending** | Confirm title/branding and rights before public links |

The homepage may feature FileGuide and a brief “Projects being reviewed for adoption” panel; do not display all intake projects as published Comutability software.

## Build and hosting proposal

**Recommended build:** Astro + TypeScript + accessible CSS/design tokens (Tailwind optional) as a **static-first public website**, with minimal client JavaScript and reusable content components. First build should not require a database, user accounts or a hosted AI API.

**GitHub:** a **separate public repo `Comutability/website`**, created only when the founder authorises it, with README, chosen open-source licence, `AGENTS.md`, `CLAUDE.md`, components, content data, tests, workflows and deployment docs. Do not put website code into `Community`.

**Hosting:** GitHub Pages using a reviewed GitHub Actions workflow is the default low-complexity option; Astro supports it. If future interactive/server features genuinely require a server, propose a separately reviewed provider and cost/privacy analysis. Domain is **TBD**; never assume a domain is registered.

**GitHub data:** rely on a reviewed local metadata file on day one, linking to real GitHub repos, PRs and releases. A later build-time synchronisation may read **public** GitHub API data, using caching, rate-limit handling, safe fallbacks and no secrets in client bundles. Never display private repos or operational secrets.

**Security and verification:** TypeScript checks, build, broken-link checks, accessibility audit (automated + human), mobile and desktop smoke tests, dependency review, CSP/security headers supported by host, no forced third-party analytics. Deployment only after documented human approval.

## Stripe support integration (conditional)

Prefer **Stripe-hosted Payment Links** for one-off support. A support page may offer a button to the **verified** Stripe-hosted checkout URL, instead of implementing custom card collection or placing a secret key in frontend code. A fixed-amount recurring option may be added separately only after accounts and terms are verified.

**Critical qualification:** Stripe's rules distinguish tips from donations. Stripe says donations must be for a specific charitable purpose and may have jurisdiction-specific restrictions, particularly for unregistered groups; do **not** silently label a general developer-support payment as a charitable donation. Before activating checkout, identify the legal payee, country, eligible purpose, correct payment classification, currency, fees and tax/receipt language. If this cannot be established, display **“Support options being prepared”** and an information page rather than a fake/live payment CTA.

If eligible and approved, a Stripe Payment Link can support a customer-chosen **one-off** amount. Fixed-price **recurring** links are separate. Configure return/success messaging accurately; do not treat a `success` URL parameter or redirect alone as confirmed payment for backend purposes.

Financial transparency: explain who receives funds, what they support (hosting, testing, accessibility, security review), how spending is reported, privacy of supporters and whether gifts are tax-deductible. Do not call Comutability a registered charity/non-profit if it has not been legally established as one.

## Definition of done for first public preview

- Every high-priority route works at mobile and desktop widths and remains readable without JavaScript.
- Brand, motto and actual status match Founding Charter v1.1 and GitHub.
- Projects show **verified** maturity states and true source/issue links; no fictitious release downloads.
- Handbook links distinguish **approved** from **draft**.
- The “How We Build” section explains ChatGPT, Claude, Base44 and human review without suggesting AI has release authority.
- Contribution actions open real issues/PRs/guidance and explain GitHub account requirements where appropriate.
- Stripe support UI has no fake link or stored card data; production support only after explicit payee/eligibility verification.
- Source and assets are rights-cleared, dependency licences reviewed and website repo has an appropriate genuine OSS licence.
- Run actual build/test/accessibility checks; report results, limitations and screenshot evidence.
- Preview reviewed by a named human; production domain/DNS/publishing is a separate human-approved step.

## Explicit non-goals for v1

No logged-in member portal, AI chatbot, GitHub user impersonation, automatic contributor approval, autonomous code merging, unverified release dashboards, real-time private GitHub data, custom payment card forms, CRM/donor database, browser tracking or public private-project source.

---

**Hand this brief to Claude together with [Claude implementation prompt](CLAUDE-BUILD-HANDOFF.md), [page copy & data status](CONTENT-AND-DATA.md) and [verification & launch checklist](LAUNCH-CHECKLIST.md).**
