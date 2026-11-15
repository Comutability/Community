# Comutability website: Open Collective support integration

**Status:** Implementation handoff for Base44, **not yet applied to the live website**.  
**Date:** 15 November 2026  
**Website:** https://comutability.org/support  
**Collective:** https://opencollective.com/comutability

## Goal

Update the existing Support page without replacing its layout or changing Founding Charter v1.1. Add a clear Open Collective contribution section, supporter recognition, and accessible links to the five proposed financial policies. Mark draft policies as drafts and do not present them as ratified.

## Suggested Support page copy

### Support Comutability

**Built together. Open to everyone.**

Comutability is a community-led, AI-assisted open-source initiative. Your support helps make useful, accessible, privacy-respecting software possible. We bring people together to build and maintain open technology with human accountability, transparent governance and independence from any one sponsor.

Support can help cover project infrastructure, documentation, development tools, accessibility work, and independent security and code reviews. Our work includes Secure Net, a developing open communication protocol, and applications and tools built around open-source values.

Support is voluntary. Contributing does not provide voting rights, exclusive code, maintainer privileges, influence over technical standards or guaranteed project deliverables.

**Primary action:** [Support Comutability on Open Collective](https://opencollective.com/comutability)

Do not make statements about tax deductibility, accepted payment methods, fiscal host, financial volume, live donation acceptance or processing fees without verifying them in the Open Collective account. Keep the existing site explanation of funding/legal arrangements unless those details have been formally verified and updated.

### Our supporters

Thank you to everyone helping keep Comutability independent and open. Open Collective updates this display automatically as recognised backers change.

### Financial policies

These documents are currently **draft proposals**, published for transparency and feedback. They become effective only after recorded human approval and any fiscal-host checks. The Founding Charter v1.1 remains the approved governing document.

- [Financial Contribution Policy](../policies/FINANCIAL-CONTRIBUTIONS.md)
- [Invoice Expenses Policy](../policies/INVOICE-EXPENSES.md)
- [Reimbursement Expenses Policy](../policies/REIMBURSEMENT-EXPENSES.md)
- [Grant Expenses Policy](../policies/GRANT-EXPENSES.md)
- [Expenses Title Policy](../policies/EXPENSES-TITLES.md)

On the website, create accessible policy detail pages under the support area using the approved text after ratification, or link to these GitHub **draft** files until then. Do not point to uncreated website paths.

## Backers SVG embed supplied by the project

```html
<a href="https://opencollective.com/comutability" aria-label="Visit Comutability on Open Collective">
  <img
    src="https://opencollective.com/comutability/tiers/backers.svg?avatarHeight=36&width=600"
    alt="Comutability supporters on Open Collective"
    loading="lazy"
    style="display:block;max-width:100%;height:auto"
  />
</a>
```

The user also supplied the official `<object>` form, which can be used where the site supports SVG object embedding:

```html
<object
  type="image/svg+xml"
  data="https://opencollective.com/comutability/tiers/backers.svg?avatarHeight=36&amp;width=600"
  aria-label="Comutability Open Collective supporters"
></object>
```

Prefer the linked `<img>` for accessible navigation and graceful responsive scaling, unless the site's visual implementation specifically needs an object element. Never hard-code supporter names, amounts or counts. Do not claim a live widget has loaded until tested in the published site.

### Design and implementation notes

- Keep existing Comutability logo, type, colours, navigation and accessibility conventions.
- Responsive layout with a max-width 600px supporter grid and clear mobile wrapping.
- Use accessible headings, descriptive link text, proper contrast and keyboard-visible focus.
- Link the primary action to the Open Collective page in a normal anchor; don't invent payment infrastructure.
- Link directly to the public Open Collective budget for transparency if its exact stable link is verified.
- Policy titles should lead to individual pages or clearly labelled GitHub drafts, not to modal-only inaccessible content.
- Maintain the existing approved charter and clearly label proposed documents.
- Check SVG loads, the Open Collective link opens, policy links are not broken, and the mobile view is correct.
- Ensure any approved donation CTA does not promise charity tax relief or perks that violate the Charter.

### Short Open Collective organisation description

Comutability is a community-led, AI-assisted open-source initiative building accessible, privacy-respecting software. We bring people together to develop useful technology, with transparent governance, human oversight and freedom for all.

### Suggested discovery tags

Open Source, Privacy, Decentralisation, Community, Artificial Intelligence.

## Publication checklist

1. Human review of content and fiscal-host arrangements.
2. Access to Base44 Comutability app and implement against the actual site source.
3. Preview and test desktop/mobile, keyboard, Open Collective and policy links.
4. Approve and publish website changes through the site's usual process.
5. Ratify any policies intended to be legally operative through the documented human governance process.
