# Onboarding Projects into Comutability
**Status: proposed. No existing personal repositories transferred by this guide.**

## Route A: New community project

1. A public proposal and human adoption decision are recorded in `Community`.
2. Assign a named human maintainer; agree scope, maturity label, security exposure and licensing.
3. Create a separate repository under `Comutability` with the agreed visibility, `README.md`, `LICENSE`, locally reviewed `AGENTS.md` and `CLAUDE.md` from [templates](../templates/PROJECT-AGENTS.md), `docs/`, `tests/` and CI as appropriate. Follow the [AI rules adoption checklist](AI-RULES-ADOPTION-CHECKLIST.md).
4. Apply repo permissions, scoped AI tokens and branch/ruleset protections; keep deployment secrets separate. If hosted, add a reviewed `docs/DEPLOYMENT.md` from the [deployment template](../templates/PROJECT-DEPLOYMENT.md).
5. Link the issue/brief from the organisation profile. Announce release **only after** release evidence and human sign-off.

## Route B: Existing GitHub repo

1. Verify permission to transfer, rights to code/media and intended community stewardship.
2. Capture a backup; audit source and git history for leaked secrets, PII, licences and third-party assets.
3. Do **not** automatically make private repositories public or overwrite names.
4. Use GitHub's **Settings → Danger Zone → Transfer ownership** to move the original repo when appropriate; the available ChatGPT connector does not expose the transfer action.
5. After transfer, verify issues, branches, tags, collaborators, webhooks, GitHub App installations, branch rules and CI.
6. Confirm external deployments, custom domains, Base44 sync and secret scopes still work.
7. Publish an adoption decision and licence after the audit; until then label as **intake/private/unverified**.

## Route C: Base44 app with no GitHub repo

1. Confirm the Base44 app owner and backups; take a checkpoint.
2. Install/authorise the **Base44 GitHub App** for the Comutability organisation from Base44's integration flow (this is independent of ChatGPT's GitHub App).
3. Check Base44 lists Comutability among eligible GitHub organisations; if not, **stop** and fix permissions.
4. Use Base44's official GitHub connect option to create a new **private** source repo owned by Comutability. It pushes the app's current code and sets up sync.
5. Verify repository, default branch, webhook, first commit, licence/assets and working app preview.
6. Implement a review-compatible sync plan; avoid direct auto-push to protected `main` without checks and human review.

## Known 2026-10-28 intake candidates

| Existing Base44 app | Current GitHub connection | Next action |
| --- | --- | --- |
| Commonveil | None | Prepare private source repo and code/IP/security audit |
| Monster Realm: Social Quest | `beitmenotyou1/monster-realm-social-quest` | Verify IP/branding (Neon Frontier); back up and transfer |
| Lantern OS | None | Create private source repo; label concept vs verified OS |
| Veil Social | `beitmenotyou1/Veil` | Back up; check encryption/auth and transfer |
| Mandatera | `beitmenotyou1/nexora` | Back up; review agent/payment authority and transfer |

**Excluded by founder:** FAMLIOGRAPH/Familograph, RetroOS Portfolio. Keep them outside this migration.

These are **candidates**, not adopted open-source releases. See [migration proposal PR #4](https://github.com/Comutability/Community/pull/4) and its detailed migration checklist.

## No ownership shortcut

GitHub transfer does not automatically change contributors' copyright, make a project open source, move Base44 account ownership, migrate private keys, or guarantee uninterrupted sync. Review each issue separately.