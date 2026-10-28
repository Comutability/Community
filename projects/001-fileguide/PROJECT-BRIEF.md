# Project 001: FileGuide

**Status:** Selected for discovery; no application repository or implementation has been created yet  
**Selected:** 28 October 2026  
**Working product name:** FileGuide (name and branding subject to availability checks)  
**Type:** Local-first, accessible, open-source desktop utility  
**Initial platform:** Linux desktop; assess Windows and macOS after validation

> **Understand your files. Stay in control.**

## The problem

It can be difficult for nontechnical computer users to identify which folders occupy storage, understand whether files are genuine duplicates and confidently decide what to do next. Existing capable tools include [Czkawka](https://github.com/qarmin/czkawka) and [dupeGuru](https://github.com/arsenetar/dupeguru). We must **not** simply duplicate their features or claim to be first.

Our hypothesis: a narrowly focused, **read-only and plain-language guided workflow** may better serve people who find conventional file-management utilities confusing or risky. This remains **unvalidated** until we speak with prospective users.

## Who it helps

- People new to file organisation, especially those afraid of deleting important files.
- People who prefer clear explanations, keyboard navigation and an uncluttered interface.
- People organising photographs, downloads or documents across local drives.

## Proposed first user journey

1. Choose one or more folders on your own computer.
2. See a straightforward breakdown of folder sizes and file counts.
3. Request an exact-duplicate scan, with clear progress and a way to cancel.
4. Review groups of identical files, including paths, sizes and why they match.
5. Save a CSV report or exit without changing anything.

## Proposed MVP, read-only

- **Folder selection:** explicit user-chosen folders only; no automatic scan of the whole device.
- **Size summary:** per-folder totals, large-file list and plain-language explanations.
- **Exact duplicates only:** group by file size, then stream SHA-256 hashes for candidates; do not infer similarity from filenames alone.
- **Review screen:** show complete paths and sizes, identify uncertainties, and avoid language suggesting it is safe to delete particular copies.
- **Export:** manually selected, local CSV report.
- **Accessibility:** keyboard-operable controls, meaningful labels, scalable text, sensible focus handling and screen-reader testing with users.
- **Privacy:** process local files without accounts, uploads, analytics or telemetry.

**Safety contract:** v0.1 must not delete, rename, move, overwrite or automatically clean any user files. It is a diagnostic tool only.

## Explicit exclusions for v0.1

- Deleting or moving files, automated cleanup and storage optimisation.
- Similar-image detection, fuzzy matching and deduplication by hard-linking.
- Cloud sync, network accounts, cloud drive support and AI-generated deletion advice.
- Background monitoring, automatic startup and privileged/system scanning.
- Windows/macOS production installers until those platforms are separately tested.

## Possible implementation, not yet approved

- **Backend:** Python standard-library file traversal and streaming SHA-256, with cancellable workers and safe handling of symlinks, unreadable files, mount points and changing files.
- **Desktop interface:** PySide6 / Qt 6, subject to licence obligations and accessibility testing. Qt for Python is distributed under LGPL/GPL and commercial options; distribution must comply with applicable obligations.
- **Testing:** pytest plus synthetic directory fixtures, behaviour tests and manual accessibility testing.
- **Licensing:** a recognised open-source licence to be selected before accepting external code. Apache-2.0 is a candidate, subject to dependency and distribution review.

## Research and go/no-go gate

Before building the MVP:

1. Interview **10 prospective users** about current file organisation problems, including people with accessibility needs.
2. Watch at least **5 people attempt relevant tasks** using existing tools, with consent and no collection of their personal files.
3. Review whether contributing an accessibility-focused interface or documentation to an existing project could solve the problem better.
4. Document actual unmet needs and competing options in this repository.
5. Proceed only if the feedback supports a materially useful, maintainable difference. Otherwise **pivot or contribute upstream**.

## Proposed delivery phases, not commitments

- **Discovery:** interviews, comparable-tool tests, licence and threat-model review.
- **Prototype:** local size report and safe exact-duplicate detection with generated test files.
- **Alpha:** accessible interface, cancellation, error handling and CSV export.
- **Community beta:** reproducible builds, documentation, independent testers and release review.

## Initial quality gates

- No file-mutating code paths in v0.1.
- Correct results on known fixtures: exact duplicates, different contents with the same name, empty files, symlinks, permission errors, files modified during a scan and nested folders.
- Scans remain responsive and cancellable; no unrestricted memory loading of large files.
- All errors clearly explained without falsely asserting that a scan was complete.
- Keyboard and screen-reader flows tested by people, not merely assumed.
- Privacy claims verified by inspecting dependencies and behaviour; do not claim an independent audit without one.
- Releases must comply with Comutability's eventual human-led AI development policy.

## Community participation

The first opportunity is **problem discovery**, not coding. Contributors can share usability experiences, accessibility requirements and what current utilities do well. Do not post private filenames, directory contents or sensitive screenshots in public issues.

## Decisions still open

- Whether the discovery results support a new product rather than an upstream contribution.
- Final project name, repository, architecture and licence.
- Maintainers and risk review before a public release.
