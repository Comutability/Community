# Stripe Support & Community Funding Design
**Status:** Conditional integration plan. NO PAYMENT LINK OR FUNDING RECIPIENT HAS BEEN VERIFIED.

## Desired user experience

A dedicated `/support/` page should explain:
- Why financial support could matter: infrastructure, build/test systems, accessibility review, security review, documentation and community maintenance
- Who receives the money and how it will be held/accounted for
- A simple transparent explanation of fees and payment processor
- Optional one-off support, with variable amount **if Stripe permits the specific account and purpose**
- Optional fixed-amount recurring support after additional review
- The right to use Comutability's open-source products regardless of payment
- Privacy and consent; no public donor names without explicit permission
- A dated, aggregated spending/use-of-funds statement where real records exist

## Stripe-specific feasibility

As confirmed by Stripe's current help guidance (28 October 2026):
- Stripe-hosted **Payment Links** can handle one-off or recurring fixed payments, and an eligible “customer chooses what to pay” option for **one-off** payments.
- Stripe says a **donation must be tied to a specific charitable purpose**, tips require goods or services, and restrictions exist on payments for unregistered entities and by region.
- Thus a volunteer software community **should not presume it can accept charity-labelled donations** via Stripe. Check with the payment-account holder, Stripe's rules and qualified local advice before enabling.

References:
- https://support.stripe.com/questions/how-to-accept-donations-through-stripe?locale=en-GB
- https://support.stripe.com/questions/requirements-for-accepting-tips-or-donations?locale=en-GB
- https://stripe.com/payments/payment-links

## Launch gating

Before an active Stripe call-to-action:
1. Human confirms **legal recipient** (individual, association, registered entity or fiscal sponsor), name and country.
2. Verify Stripe account eligibility and correct classification (charitable donation, contribution, sponsor payment or another permitted type). Do not mislabel.
3. Confirm specific intended purpose, terms, fees, taxation and receipts including whether any tax relief applies. Never claim tax deductibility without proof.
4. Create/test the official **hosted Payment Link** in Stripe Dashboard, not by inventing a checkout URL.
5. Add **only the approved public Payment Link URL** to configuration. Never put secret API keys, webhook secrets or card data in source/client.
6. Test desktop/mobile link and Stripe test mode where available, verify correct payee, currency, purpose, receipt and post-payment experience.
7. A designated human approver enables the CTA and documents the result.

If any step isn't confirmed, render **“Financial support options are being prepared”** and public funding principles instead of a broken/dummy Donate button.

## Developer integration

For the initial static site, the “Support Comutability” CTA should be an ordinary external link to an explicitly configured **HTTPS Stripe Payment Link**. Do not build custom card entry, store payment information, expose credentials or introduce an unnecessary payment backend.

Provide a safe configuration flag:
```ts
export const supportConfig = {
  enabled: false,   // Must remain false until human verification
  label: "Support Comutability",
  stripePaymentLink: undefined as string | undefined,
  legalPayee: undefined as string | undefined,
  purpose: undefined as string | undefined,
  currency: undefined as string | undefined,
} as const;
```
When enabled, validate that the URL is an exact approved Stripe-hosted URL; no arbitrary redirect URL from user input.

If later adding webhooks, verify signatures server-side, protect secrets, avoid storing unnecessary supporter PII, implement idempotency and never treat a redirect as confirmed funds.

## Fairness and governance

Supporting Comutability must **not buy maintainer privileges, voting control, access to unreleased code or special rights over the community's open-source work**. Any sponsorship programme must state actual terms and conflicts of interest.

## Alternative to discuss, not an automatic switch

GitHub Sponsors may be appropriate for funding open-source work, but has account and eligibility requirements. The founder requested Stripe, so **Stripe remains the proposed primary provider** if legally and operationally eligible.

## Support page draft text

**Help keep useful software open.**

“Comutability is a community initiative. The tools we release are intended to be open-source and accessible regardless of anyone's ability to contribute financially. Support, when available, helps cover the work behind reliable software: infrastructure, testing, accessibility, documentation and security review.”

**Until payments are active:** “We're establishing a transparent, appropriate way to receive financial support. This page will identify who receives contributions, how funds are used and the terms before any payment button goes live.”
