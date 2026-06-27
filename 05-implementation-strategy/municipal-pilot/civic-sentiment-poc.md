# Civic Sentiment: Pillar 2 of the PoC (routed around the match)

*The municipal pilot has two complementary sensor families. Pillar 1 makes the **economy** legible from administrative facts ([city-data-roadmap.md](city-data-roadmap.md)). Pillar 2 — this document — makes the **civic experience** legible from citizen perception. The synthesis (perception laid beside administrative reality) is the moat. This doc is scoped to the **proof-of-concept**, which is deliberately not the full vision.*

---

## Vision vs. PoC — keep them separate on purpose

These are different things, and conflating them is what gets the project burned:

- **The broader vision** is a civic-mood instrument that eventually covers the charged questions too — crime, safety, governance — and holds power accountable by showing what citizens feel against what the data says. That capability is national-scale, mature, and politically heavy.
- **The PoC** has one job: prove that **citizen-sourced data can be captured and made to flow into a legible, reality-anchored aggregate** — on a topic nobody fights over. Same mechanism, deliberately inert content.

The PoC is intentionally *under*-ambitious politically while being a *full* proof technically. Don't make the plumbing demo carry the weight of the cathedral.

## The core move: separate the engine from the cargo

The flammability lives entirely in the **content**, never the **mechanism**. The proportional sentiment engine — forced trade-off weighting, geographic aggregation, perception-vs-administrative cross-validation — is identical whether the topic is "police corruption" or "potholes." Only the topic carries charge.

> **So the PoC proves the engine on inert cargo. The charged cargo is a later capability the proven engine can carry — not PoC scope.**

This is the same discipline Pillar 1 already accepted: lead with **business registrations**, not tax receipts; the low-sensitivity dataset proves the pipe without the fight ([micro-standard.md](micro-standard.md)). Second pillar, same principle.

## Two dials — both turned to "cold"

**1. Topic sensitivity.** Crime, corruption, governance = hot, and **out of PoC scope entirely**. Roads, lighting, sidewalks, parks, cleanliness, trees, crosswalks, transit = cold. Nobody is unseated by a pothole map.

**2. Framing.** Ask **"what would most improve your neighborhood?"** — never **"what is the city failing at?"** Both return the *same proportional problem-map* (points poured into "roads" means roads are the problem either way), but one is **collaborative** and one is **accusatory**. Constructive framing positions citizens and the city as co-improvers, not prosecutor and defendant. Same signal, most of the political charge removed.

## What the PoC actually is

A **participatory neighborhood-improvement instrument**, run as an **independent civic mirror** (no city buy-in required — it reflects, it doesn't run a service desk):

> *"Distribute 100 points across what would most improve your area — roads, lighting, green space, cleanliness, transit, public services…"* — aggregated by neighborhood and over time, and laid beside the city's existing 311 data to show where perceived priority and formal complaints agree or diverge.

What this buys, for free:
- It's the **exact proportional mechanic** of the full vision, pointed at a safe question.
- It **cross-validates against administrative data** — the moat survives intact.
- It carries **democratic legitimacy** (participatory budgeting has decades of precedent), so even as an independent mirror it reads as pro-civic, not adversarial. A pothole-priority map threatens no one, so the independent posture stops looking like an attack.

## Capture — the proportional mechanic

- **Forced trade-off, not ratings.** Ask people to **distribute a fixed budget (100 points)** across categories, or to **rank their top 3**. Per-issue 1–10 ratings collapse to "everything's a 9" and yield no *relative* signal; a budget forces scarcity — the same allocation logic as the whole project — and produces a genuine proportional weighting.
- **Fixed improvement taxonomy.** A closed, comparable category set (roads/transport, lighting/safety-of-space, green space/parks, cleanliness/sanitation, public services, transit…). Fixed categories are what make proportions comparable at all. Keep an "other + open text" channel purely to *discover* new categories to promote later.
- **Optional issue-report texture.** A free-form "describe a specific spot" field can ride underneath as qualitative color — but it is **not** the headline and is never the thing that must get "fixed" (a mirror can't close that loop).

## Structure — the shared spine

Identical backbone to Pillar 1, so the two pillars literally overlay on one map:

> **geography × period × category**

Snap every response to the **same canonical neighborhood layer** and **month bucket** as the economic pillar; the category axis here is the improvement taxonomy. Aggregate to proportions per (area × period × category). Apply the same small-cell suppression — never publish a cell that could expose an individual respondent.

## Publish — the divergence is the product

- **The improvement-priority map:** what each neighborhood would most improve, in proportion, over time.
- **The administrative overlay:** the same categories laid beside the city's **311** signal (e.g., road-priority sentiment ↔ 311 road requests). Where they **match**, a priority is confirmed; where they **diverge**, that gap is the insight — and the genuinely novel output no incumbent offers.
- **Open data + a simple public view,** mobile-first, no login, every tile showing methodology, freshness, and confidence ([data-pipes-architecture.md](../../00-foundations/architecture/data-pipes-architecture.md)).

## Representativeness — your whole credibility, with no city to lend it

With no institution behind it, the first attack is "this is just the people with your app." Defeat it with method, not authority:

- **Post-stratification weighting:** weight responses so respondent demographics/geography match the census — the standard, defensible survey fix.
- **Radical disclosure:** publish *who answered* next to every result ("responses skew 25–44, downtown, smartphone-owning"). Naming your own bias is the credibility move — the false-precision principle applied hard ([design-principles.md](../../00-foundations/design-principles/design-principles.md)).
- **Honest brand:** *"the engaged public's weighted perception,"* never "the city thinks."

## Explicitly out of PoC scope (the deferred, flammable capability)

- **Crime and safety** — and if ever added, only as aggregate **perception of safety** at coarse geography, never incident reports (which create panic maps, stigmatize neighborhoods, and carry real liability).
- **Governance / corruption / official performance.**

These are capabilities the proven, trusted engine can carry *later*, after credibility is banked on inert topics. Adding them is then a **content change, not a method change**.

## Guardrails kept even at low stakes

Run the full honesty/method stack even on potholes — perception-labeled, methodology-public, bias-disclosed, aggregate-only, and **defend the method, never the conclusion** ([political-positioning.md](../political-positioning.md)). Not because potholes are dangerous, but because it builds disciplined habits where mistakes are cheap, and makes the eventual jump to charged topics safe.

## Staged sequence

- **Stage 0 — Backbone:** fix the improvement taxonomy and reuse Pillar 1's canonical geography + month bucket. No data yet.
- **Stage 1 — One benign question, end to end:** the 100-point allocation, captured → weighted/aggregated/suppressed → published as a neighborhood map + methodology. Proves the entire capture→structure→publish loop on inert content.
- **Stage 2 — Administrative overlay:** lay the result beside 311 data; ship the divergence view. This is the moment it becomes more than a poll.
- **Stage 3 — Representativeness:** add post-stratification weighting and the "who responded" disclosure panel.
- **Stage 4 — Synthesis:** overlay with Pillar 1 (economic vitality + civic priority on the same neighborhoods) and hand a real decision-maker the combined picture.

## Honesty about the limits (state prominently)

- **Perception is not reality** — and is only valuable when never presented as fact. A high improvement-priority for roads is a *feeling about roads*, not a pavement measurement.
- **Self-selected participation skews** toward the engaged, online, and connected; weighting mitigates but never fully removes it. Disclose it.
- **It is gameable** — a motivated group can flood it. Friction (one-per-device, rate limits), anomaly detection, and the administrative anchor are the defenses.
- **A mirror does not fix anything** — its value is the reflection, not resolution. Set that expectation so participation doesn't die waiting for repairs.

---

## The one-paragraph version

The PoC for the civic dimension does not deal with the flammable thing — it **routes around it**. The political charge lives in the content (crime, governance), never in the mechanism, so the proof runs the full proportional, reality-anchored sentiment engine on inert cargo: a constructively framed *"what would most improve your neighborhood?"* budget-allocation instrument, run as an independent mirror, aggregated on the same geography × time × category spine as the economic pillar, and laid beside the city's 311 data so the divergence between perceived priority and formal complaint becomes the product. It proves the whole thesis — citizen data captured and made to flow into a legible, reality-anchored aggregate — without ever lighting a match, and it banks the credibility that lets the proven engine carry heavier cargo later.
