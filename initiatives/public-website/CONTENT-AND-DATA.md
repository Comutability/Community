# Content & GitHub Data Contract
**Status:** Proposed content schema and factual seed data · **Checked:** 28 October 2026

## Authority and precedence

1. Approved [Founding Charter v1.1](https://github.com/Comutability/Community/blob/main/FOUNDING-CHARTER.md)
2. Actual public GitHub repo, release and decision state
3. Ratified policy and maintained project-specific release documents
4. Human-reviewed, dated website content

**Do not use an AI conversation as the sole source for live claims.** The website repo contains a reviewed content snapshot, with source URLs and `lastVerified` fields. Any future synchronisation is read-only to public GitHub.

## Organisation seed metadata

```ts
export const organisation = {
  name: "Comutability",
  expandedName: "Community + Usability",
  motto: "Built together. Open to everyone.",
  githubUrl: "https://github.com/Comutability",
  charterUrl: "https://github.com/Comutability/Community/blob/main/FOUNDING-CHARTER.md",
  handbookProposalUrl: "https://github.com/Comutability/Community/pull/5",
  aiPolicyProposalUrl: "https://github.com/Comutability/Community/pull/3",
  aiRulesProposalUrl: "https://github.com/Comutability/Community/pull/5",
  founded: 2026,
  status: "forming",
  noReleasedCommunitySoftwareYet: true
} as const;
```

Do not automatically insert a full registered legal entity name, donation recipient, mailing address, charity number or financial amount until verified by the person actually responsible.

## Project schema example

```ts
export type ProjectState =
  | "idea" | "discovery" | "prototype" | "alpha"
  | "beta" | "maintained" | "archived" | "intake-pending";

export type ProjectRecord = {
  slug: string;
  name: string;
  summary: string;
  category: string;
  state: ProjectState;
  stateEvidenceUrl: string;
  canonicalRepositoryUrl?: string;
  proposalUrl?: string;
  releaseUrl?: string; // ONLY if a real published, supported release exists
  websiteUrl?: string; // only if current, verified and permitted to link
  licenceSpdx?: string; // only if actually established for that repo
  humanMaintainer?: string; // only public, authorised display names
  updatedAt?: string;
  lastVerified: string;
  availableForDownload: boolean;
  communityAdoptionApproved: boolean;
  limitations: string[];
};
```

Initial seed (do not fabricate missing fields):

- **FileGuide:** `discovery`, `availableForDownload: false`, `communityAdoptionApproved: true` *only in the limited sense of concept selection for discovery*, with explicit text “Not yet a released app”. A clearer implementation may separate `ideaSelected: true` from `communityAdoptionApproved: false`.
- **Commonveil:** `intake-pending`, `communityAdoptionApproved: false`.
- **Veil Social:** `intake-pending`, not certified; no release claim.
- **Mandatera:** `intake-pending`, human agent authority needs review.
- **Lantern OS:** `intake-pending`, OS is not independently boot verified.
- **Monster Realm: Social Quest:** `intake-pending`, branding/asset-rights review pending.

**Excluded completely from catalogue:** Familograph/FAMLIOGRAPH and RetroOS Portfolio.

Keep the website content from auto-promoting intake projects to official software based solely on finding a public URL. An existing Base44 site does not prove open-source status.

## Trust evidence schema

Each claim has an explicit status and link:

```ts
type EvidenceClaim = {
  label: string;
  kind: "source" | "ci" | "human-test" | "accessibility" | "security-review" | "release-approval";
  status: "not-started" | "in-progress" | "passed" | "failed" | "not-applicable";
  evidenceUrl?: string;
  reviewer?: string; // consented public maintainer name only
  verifiedAt?: string;
  scope?: string;
};
```

Never render a green “verified” chip without `status: passed` and relevant verifiable evidence, and don't label a self-review as independent.

## Public GitHub integration rules

Use static content first. Optional later: fetch *public* repository metadata at build time with an authenticated **server-only** token if needed and approved. Cache content, handle failure/rate limits and expose timestamps. Ensure private repository names, PRs and data never leak.

Never let visitors browse an invented private GitHub data proxy. Do not imply that checking GitHub API status is the same as verifying a build or product feature.

## Updates and community stats

- All updates need dates and human-reviewed source links.
- Do not show “123 contributors”, “6 production apps”, “98% verified” or any other made-up counts.
- “Latest activity” requires actual public event data or a manually maintained dated changelog.
- Links to draft PRs must retain visible **Proposal / Not ratified** labels.
