# Case study: Watch Collector

A running, modular case study of Watch Collector, a visual-first website for researching watch purchases and tracking a collection. It is a research tool and a digital collection, not a marketplace. This is a repo-only doc, never built or shipped. It is the raw material for portfolio write-ups.

## How this file works

- **Modules, not chapters.** Each `##` section stands alone, so a write-up can pick some modules and drop the rest without leaving a gap.
- **Tag lines.** Every module opens with an italic tag line:
  - **Core** modules are the spine of any version.
  - **Optional** modules suit the long form or a specific audience, named in brackets.
  - **Evidence** says what to show beside the text, marked `[ ]` until it has been captured.
- **Running.** When work is worth telling, add or amend a module and add a row to *Log of additions*. Facts and dates come from [`DECISION-LOG.md`](DECISION-LOG.md), and the reasoning from [`DECISIONS.md`](DECISIONS.md). This file is where they become a story.
- **Placeholders** go in `[[double brackets]]` for the owner to fill in: role, tools, metrics, reflections. Never invent them.

> **Status:** The project is at the planning stage, with no code yet. Modules 4 and 5 are written as open problems and get rewritten as the decisions behind them are made.

## Suggested cuts

| Form | Modules |
|---|---|
| Short | 1, 2, 3, 8 |
| Standard | 1, 2, 3, 4, 5, 6, 8 |
| Long | 1–9 |

## 1. Overview

*Core · Evidence: [ ] hero screenshot of research mode beside collection mode*

Watch Collector is a website for watch enthusiasts that does two things in one place: research the next purchase, and keep track of the collection afterwards.

- **Role:** [[your role(s), e.g. designer and developer]]
- **Timeline:** Planning started 2026-10-14. [[end date or "ongoing"]]
- **Tools:** [[stack and tools, once chosen]]
- **Team:** [[solo / collaborators]]

## 2. The problem

*Core · Evidence: [ ] the tabs and spreadsheets a collector juggles today*

A collector researching a watch jumps between brand sites, spec databases, forums and marketplace listings. Once they buy it, they track it somewhere else entirely: a spreadsheet, a notes app, or nowhere. Nothing joins *"should I buy this?"* to *"I own this"*. Most of the tools that exist treat watches as rows of specs, even though people choose watches mostly by how they look.

The brief: a one-stop shop that puts the visuals first, with every relevant piece of metadata available. [[why this mattered to you personally]]

## 3. Reframing the brief: one catalog, two modes

*Core · Evidence: [ ] diagram of catalog → research → "Add to collection" → collection*

The brief called for two modes, so the first framing question was whether they are two apps or one. The proposed answer is one shared catalog of watch references, seen through two modes:

- **Research mode** for browsing, filtering, comparing and shortlisting.
- **Collection mode** for the watches the owner actually has.

A single action, *Add to collection*, connects them. It turns a catalog reference into an owned watch with the specs already filled in, so the owner only adds what is personal to their copy: price paid, condition, box and papers, service history.

That split gives two levels of metadata: reference-level specs (case, dial, movement, bracelet) and copy-level records (purchase, provenance, wear, service). [[confirm or amend once this is logged as a decision]]

## 4. The hard part: where the data and images come from

*Core · Evidence: [ ] comparison of the data-source options considered*

I don't know of a good free, licensed source of watch specifications. Scraping marketplaces or spec sites raises terms-of-service problems, and brand press photos are copyrighted. That matters for a product whose whole pitch is visual. The options on the table are a curated seed catalog with manual entry, a licensed provider, or community contributions. For images, a possible split is attributed catalog imagery and owner-uploaded collection photos.

This is still open; see `DECISIONS.md → Open questions`. [[the decision and its trade-off, once made]]

## 5. Designing for the watch, not the spreadsheet

*Core · Evidence: [ ] gallery, deep-zoom viewer, true-to-scale comparison*

[[Write once design decisions are logged.]] Planned direction: large hero imagery on a dark, gallery-like theme; a multi-angle deep-zoom viewer; and a true-to-scale size comparison that shows two watches side by side, or on the owner's wrist size, at real millimetres.

## 6. Saying no on the record

*Core · Evidence: [ ] the Deferred rows from DECISION-LOG.md*

The first "no" came with the brief itself: **not a marketplace.** Watch Collector helps someone decide and keeps a record. It does not sell, list or broker. That keeps it free of listings, payments and seller trust, and leaves its attention on research and collection.

Later Deferred rows in the decision log belong here, each with what would bring it back.

## 7. Quality

*Optional [engineering audiences] · Evidence: [ ] test and CI summary*

[[Testing approach, CI and accessibility checks, once the codebase exists.]] The decision log already has its own rule here: once the repo has a test runner, a test validates every pending entry, so a malformed record fails CI.

## 8. Outcome and reflection

*Core · Evidence: [ ] before/after or usage metrics*

- **Outcome:** [[what shipped, and who uses it]]
- **Metrics:** [[collection size tracked, research sessions, etc.]]
- **Reflection:** [[what you would do differently]]

## 9. Working with an AI collaborator

*Optional [process / AI-curious audiences] · Evidence: [ ] excerpt from the planning conversation*

The project started as a planning conversation with an AI coding assistant, and the instruction was explicitly *not* to build anything yet. The assistant proposed the one-catalog, two-modes framing and a metadata schema. It flagged data sourcing and image rights as the hardest problems and returned five questions for the owner instead of choosing for them. The running records in this repo came from the same collaboration, so decisions are written down as they are made. [[your view on how the collaboration went]]

## Log of additions

| Date | Module | Change |
|---|---|---|
| 2026-11-19 | All | Initial draft from the planning conversation and the first decision-log entry |
