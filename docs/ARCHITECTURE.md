# GitHub Organisation Architecture
**Status: proposed**

## Repository responsibilities

```
github.com/Comutability/
  Community/               # central handbook, charter, decisions, project registry
    FOUNDING-CHARTER.md     # approved v1.1
    OPERATING-HANDBOOK.md   # proposal until approved
    docs/                  # how the community works
    decisions/             # approved decisions, immutable historical record
    projects/              # intake briefs (NOT application source)
  .github/                  # public organisation profile and default community forms
    profile/README.md
    CONTRIBUTING.md
    CODE_OF_CONDUCT.md
    SECURITY.md
    .github/ISSUE_TEMPLATE/
  <project-repo>/           # one per approved application
    README.md, LICENSE, NOTICE (when required)
    CLAUDE.md, AGENTS.md
    docs/, src/, tests/, .github/, SECURITY.md
```

A GitHub organisation owns multiple repositories. The `Community` repository is the **home of policy and coordination**, not a giant monorepo containing every product's code. Use native GitHub teams and per-repository permissions for selected collaborators.

## Ownership and project boundaries

- Source and release artifacts belong in a project repository and its release records.
- One project must not silently change the CI, credentials, code or production environment of another.
- Shared documentation and templates should live centrally but project-specific security plans, licences and CI remain local.
- Project websites, domains and hosting may remain external, including Base44; they must clearly link to the associated source repo and state current maturity.
- GitHub handles issues and pull requests as the auditable work tracker; AI chat history is **not** authoritative project history.
- A closed-source vendor's hosted AI or builder platform does **not** live in our GitHub repositories.

## Repo naming and lifecycle

Use simple lowercase kebab-case for new names; don't rename existing Base44-linked repositories until sync/redirect risks are assessed. State one of: `idea`, `discovery`, `prototype`, `alpha`, `beta`, `maintained`, `archived`.

Every accepted project has: owner/maintainer, approved scope and status, recognised OSS licence, build and test instructions, security route, data/AI dependency disclosures, versioning, maintenance/support status and contributor guidance. No fake install instructions or unreleased binaries.

## Branch and change controls

- Protect `main` from force-push and deletion. Introduce required PRs/reviews when review capacity is established.
- Have a named human code/release owner; use `CODEOWNERS` where appropriate, not as a substitute for permissions or actual reviewers.
- Use feature branches, focused PRs and CI. Required checks must exist before making them blocking.
- For Base44 apps, test vendor sync compatibility before enabling policies that would block its writes. If vendor sync cannot meet required controls, use a staging branch or alternative workflow, and **do not misrepresent the review guarantee**.
- Keep secrets only in approved secret stores; never in Git, public issues or AI instruction files.

See [project onboarding](PROJECT-ONBOARDING.md) and [security](SECURITY-AND-RELEASE.md).