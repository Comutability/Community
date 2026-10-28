# Comutability Website: Design System Direction
**Version:** 0.1 · **Status:** Proposed, subject to accessible contrast testing and founder review.

## Art direction

An **open-source workshop meets digital commons**: contemporary, tactile, imaginative and hopeful. Avoid generic AI robots, neon circuitry everywhere, meaningless 3D renders, heavy gradients or “startup valuation” imagery.

Visual motifs: useful blocks assembling into tools, connecting paths between a person and a project, code revisions moving through transparent checkpoints, human approval signatures and small organic illustrations of collaboration.

## Starting design tokens

| Role | Proposed value |
| --- | --- |
| Dark page | `#101A25` |
| Dark cards | `#1B2937` |
| Light page | `#F7F8F5` |
| Muted text | `#AAB9C5` on dark surfaces (verify contrast) |
| Positive/active accent | `#42D9BA` |
| Warm highlight | `#F2B58D` |
| Main text | `#F7F8F5` on dark; `#101A25` on light |
| Border/divider | `#344755` on dark (verify) |

Do not assume all colour pairs are AA-compliant: measure and adjust. Status text should never rely on colour alone.

Typography: an openly licensed, self-hosted modern sans serif with strong lowercase forms, optional monospace used only for metadata. Use clear hierarchy; body comfortable on mobile. Avoid excessive tiny terminal text.

## Core elements

- Spacious editorial sections with one clear point each
- Project cards with **real status and source** as primary metadata
- Modular “Imagine, Create, Verify, Share” visual pipeline, keyboard-navigable
- Honest release-evidence explainer with checklists and actual links
- “How to contribute” cards based on visitor intent
- Light and dark schemes, reduced motion, logical focus order
- Restrained SVG/node-line animation that conveys workflow, not decoration
- Responsive top navigation, prominent GitHub source links and transparent footer
- Accessible buttons and links with meaningful text; no fake disabled interaction

## Homepage wireframe, narrative order

```
[ Comutability  Projects  How we build  Community  Handbook  Support  GitHub ]
[ Short strapline ]     [ purposeful connecting-node visual ]
[ BIG: Good ideas deserve to become useful tools. ]
[ Explainer / Browse projects / Join community ]
[ Imagine → Create → Verify → Share interactive explainer ]
[ Current projects: FileGuide (discovery) + pending intake notes ]
[ What does “human verified” actually mean? with proof links ]
[ Meet the workflow: ChatGPT | Claude | GitHub | Base44 | Humans ]
[ Who can join and how: ideas | testing | writing | code | review ]
[ Our ten values + open source vs proprietary development services ]
[ Support / transparency CTA, conditionally active Stripe hosted link ]
[ Footer: Charter, decisions, projects, privacy, accessibility, source ]
```

## Suggested motion

Use gentle progressive reveal and small line connections, with `prefers-reduced-motion` honoured. No auto-playing hero videos, endless motion, scroll hijacking, keyboard traps or flashing.

## Graphic asset policy

Preferred: original CSS/SVG diagrams created for this project, openly licensed assets and project logos used with permission. Do not scrape source code or protected imagery from unrelated products. Avoid invented partner logos or certification seals.

## Content and tone examples

Hero: **Good ideas deserve to become useful tools.**

Subheading: “People bring ideas. AI helps build. Humans test, review and decide what ships. The result is useful software developed openly, for everyone.”

Human-check heading: **AI can help write the code. People must earn the trust.**

Contributor heading: **You don't need to code to make something better.**

Support heading: **Help keep useful software open.** (Activation conditional on Stripe eligibility)

All text in natural UK English. No unsupported “fully tested”, “100% secure” or “independently verified” claims.
