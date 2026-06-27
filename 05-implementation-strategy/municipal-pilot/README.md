# Municipal Pilot: The Publish-Mandate at City Scale

This folder is the operational kit for the first econOS proof-of-concept: a **single municipality publishing data it already collects**, under a tiny open standard, with a recruited team building a public dashboard on top.

It is the national vision ([CLAUDE.md §5.6](../../CLAUDE.md), the publish-mandate) shrunk to a scale where adoption is actually achievable — you persuade one local official, not win an election. The working pilot becomes the artifact that de-risks the larger argument.

**The thing being proven is not the dashboard.** It is one sentence, made true with evidence:

> *A government official enacted a tiny publish-mandate. It cost almost nothing. It made the local economy legible. And no one could attack it, because it's just facts.*

## Two pillars

The pilot has two complementary sensor families, sharing one `geography × period × category` spine so they overlay on the same neighborhoods:

- **Pillar 1 — Economic legibility** (administrative *facts*): make the local economy visible from records the city already collects.
- **Pillar 2 — Civic sentiment** (citizen *perception*): make the civic experience visible from what residents report. Scoped for the PoC to route around politically charged content.

The synthesis — perception laid beside administrative reality — is the moat.

## What's here

- **[champion-pitch.md](champion-pitch.md)** — the one-page case you bring to a city official. Framed as *their* win.
- **[micro-standard.md](micro-standard.md)** — the minimal open standard: one dataset, an agreed schema, monthly aggregates, privacy rules, publication format. This document is the reusable asset — the template the next city copies.
- **[city-data-roadmap.md](city-data-roadmap.md)** *(Pillar 1)* — the data substance beneath the pitch: how to capture, structure, and publish a data-rich city's records into a legible map of the local economy (capture → structure → publish, staged one indicator at a time).
- **[civic-sentiment-poc.md](civic-sentiment-poc.md)** *(Pillar 2)* — the citizen-perception instrument, scoped for the PoC: a constructively framed "what would most improve your neighborhood?" budget-allocation mirror that proves the sentiment engine on inert content, without lighting a match.

## The sequence (full plan)

1. **Pick the city + champion** — small/mid-size, already digitizes records, reachable sponsor.
2. **Inventory what they already collect** — lead with **business registrations**.
3. **Define the micro standard** — see [micro-standard.md](micro-standard.md).
4. **Recruit the team** — university capstone builds the pipeline + dashboard.
5. **Extract the value** — case study, testimonial, press, and a replication kit.

Guardrails throughout: aggregates only (never individuals), one low-sensitivity dataset first, forkable/mirrored hosting so the data outlives the official, and defend the method — never the conclusion ([political-positioning.md](../political-positioning.md)).
