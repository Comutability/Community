# Licensing: Open Projects, External Proprietary AI
**Status: recommended licensing framework, not project-by-project legal approval. Seek qualified advice for complex integrations.**

## The distinction

**Comutability's published software projects should be genuinely open source.** Their **source code**, modifications and distribution are governed by a recognised open-source licence. The AI *tools used to write that code* (ChatGPT, Claude, Base44) are independently supplied services, often closed source. **Using a proprietary tool to create open-source code does not automatically make the tool part of the released program or require publication of the vendor's internals.**

Examples:

- Claude writes a Python module: **the module's licence** is selected by rights-holders and is subject to the provenance and dependency review. Claude itself is **not relicensed by Comutability**.
- ChatGPT drafts a README: Comutability may publish it when allowed by applicable terms and contributor rights. ChatGPT's code, weights and service are **not** included.
- Base44 hosts a source-available web app: the exported application code can only be described as open source once **all necessary distributable source**, permissions and licence obligations have been reviewed. Base44's proprietary hosting/editor do **not** become open source.
- An app depends at runtime on a paid proprietary AI API: its **application code can still be open-source**, but the **full service is not self-sovereign/offline** unless there is a viable alternative; disclose credentials, fees, provider and limitations. Do not imply the runtime model is open source.

Open source may be sold, used commercially, forked and redistributed. **You cannot truthfully call a no-commercial-use, no-fork or nonredistributable project open source.** (Open Source Definition: https://opensource.org/osd.)

## Recommended default decision matrix

| Component | Candidate | Why / caution |
| --- | --- | --- |
| General libraries, SDKs and small tools | **Apache-2.0** | Permissive, express patent grant; downstream proprietary use permitted |
| Desktop applications | **GPL-3.0** or **Apache-2.0** | GPL protects downstream sharing obligations on distributed derivatives; Apache maximises reuse; decide per product |
| Network-first self-hosted platforms | **AGPL-3.0** | Copyleft can require corresponding source availability for modified network-served versions; review combined-work compatibility |
| Documentation, diagrams (separate from code) | **CC BY 4.0** (candidate) | Attribution and re-use, subject to authors' rights; avoid indiscriminately relicensing third-party screenshots |
| Code examples/snippets | Match project code licence (often Apache-2.0) | Clear reuse terms |
| Brand marks and project logos | **Separate trademark/brand-use policy** | Code licence usually does not grant trademark rights |
| Third-party fonts, music, images, trained models, sample data | Individual upstream licences | Must inventory and comply; no blanket claim of ownership |

These are **candidates**. Do not add licences to imported project code or assume an existing licence can be overwritten. Maintain `LICENSE`, attribution/`NOTICE` where needed, an SPDX identifier and a third-party list per project.

## Can we keep the AI proprietary but the project open source?

**Yes**, if the proprietary AI is a development tool rather than part of the licensed source distribution, and the chosen licence and vendor terms permit the specific outputs. Do not publish proprietary model weights or hidden credentials. Where an AI API is an *essential* runtime dependency, disclose the proprietary service and avoid claiming the complete stack is open source.

A wrapper around an API can be open source even when the provider is not. A package incorporating closed vendor code cannot simply be declared open source by placing a licence at the root.

## Ownership of AI-assisted work

- Review provider terms, workplace ownership and applicable copyright law. Do not assume AI output is automatically protectable or automatically owned by the community.
- For human contributions, record contributions and use the applicable project licence; default proposal is **DCO (Developer Certificate of Origin) with sign-off**, not a forced copyright assignment or CLA. DCO has to be separately adopted and configured before being enforced.
- Maintain dependency attribution and avoid generating close copies of non-licensed third-party code, artwork or proprietary prompts.
- Migrating a personal repo into Comutability changes **repository administration**, not automatically copyright ownership.
- Handle trademarks, game assets and intellectual property separately from software licences.

## Project licensing checklist

1. Identify all rightsholders and origin of files/assets and generated code; scan for secrets.
2. Check dependency licence compatibility, including transitive dependencies, SDKs, fonts and hosted services.
3. Choose the **actual** OSS licence and add its complete text and SPDX tag; do not invent modifications to licence terms.
4. Specify whether an online service uses a proprietary runtime model. Document privacy, user costs, rate limits and optional open alternatives.
5. Add third-party attributions, notices and a rights policy for media/data.
6. Test whether a stranger can build and meaningfully use the application from the published code. If the app requires undisclosed proprietary backend logic, its open-source status must be qualified.
7. Record a human-approved release decision.

## GitHub organisational licence

The **Community** repository currently has an Apache-2.0 `LICENSE`. This does **not** license all present and future Comutability projects. GitHub does not support a universal inherited licence. Each project must carry its **own explicit licence**.

## Source and legal references

- OSI Open Source Definition: https://opensource.org/osd
- OSI Open Source AI Definition: https://opensource.org/ai
- Choose a License: https://choosealicense.com/licenses/
- AGPL-3.0: https://choosealicense.com/licenses/agpl-3.0/
- SPDX identifier list: https://spdx.org/licenses/
- DCO: https://developercertificate.org/