# The Micro Open Standard (v0.1)

*The minimal econOS publication standard, instantiated at city scale. Deliberately tiny: one dataset, one schema, monthly cadence, aggregates only. This document is the reusable asset — the template the next city copies. Keep it to two pages.*

---

## 1. Scope

This standard governs the publication of **one municipal dataset** as open, aggregated, machine-readable data. The lead dataset is **business registrations** (openings and closures). The same structure extends to building permits and other indicators later; do not add them until the first is live and credible.

**Principle:** publish data the city already collects. This standard adds no new collection — only a format, a cadence, and a privacy rule for publication.

**The shared keys (what lets one standard cover many indicators).** Every indicator published under this standard is keyed on the same three axes — **geography × period × category** (§2 below). Because the keys are shared, a second indicator (building permits, rents, job postings) snaps onto the same spatial and temporal grid as the first, and the two can be overlaid on one map without re-keying. Choosing and freezing these keys once — a canonical sub-city geography, a month bucket, and a standard category scheme (e.g. NAICS) — is the move that turns siloed department exports into a single legible panel. See [city-data-roadmap.md](city-data-roadmap.md) for how the keys are applied across indicators.

## 2. The dataset: business registrations (aggregated)

One row per **(period × geography × sector)**. Each row reports counts only.

| Field | Type | Description |
|---|---|---|
| `period` | string `YYYY-MM` | The calendar month the counts cover. |
| `geography` | string | Sub-city area code (district / ward / ZIP / official zone). Use the city's own canonical codes. |
| `geography_name` | string | Human-readable name for `geography`. |
| `sector` | string | Business category. Use a standard scheme (e.g. NAICS 2-digit) or the city's own license categories — whichever already exists. State which in the methodology. |
| `opened` | integer | New registrations recorded in the period. |
| `closed` | integer | Closures / cancellations recorded in the period. |
| `active_total` | integer | Active registrations at period end (optional if not readily computed). |
| `suppressed` | boolean | `true` if counts were suppressed for privacy (see §4). |

**Net formation** (`opened − closed`) is intentionally *not* a published field — it's an interpretation, and interpretation is left to whoever builds on the data. Publish the raw counts; let others derive the metric.

## 3. Format, cadence, location

- **Format:** both **CSV** (one file) and **JSON** (array of row objects), identical content. UTF-8.
- **Cadence:** monthly. Each release adds the latest complete month; prior months are never altered (corrections go in a new versioned file, see §6).
- **Location:** a public, downloadable URL with **no login and no paywall** — the city's open-data portal or a public Git repository the city owns. The dataset must be **mirrorable and forkable** so it survives any single host or administration.
- **Naming:** `business-registrations_YYYY-MM.csv` / `.json`, plus a rolling `business-registrations_latest.*`.

## 4. Privacy rule (non-negotiable)

- **Aggregates only.** No row may identify an individual person, business, or address.
- **Cell suppression:** any `(geography × sector)` cell with a count **below N = 5** is suppressed — report the count as blank/`null` and set `suppressed = true` (do not report it as `0`). Choose the smallest geography/sector granularity at which most cells clear the threshold; if too many cells suppress, coarsen the geography or sector grouping rather than publishing identifiable data.
- **No individual-level data is ever published, requested, or stored by the pilot.** This is the line that makes the project the opposite of surveillance.

## 5. Methodology page (the credibility mechanism)

Every release links to a plain-language methodology document stating:

- **Source:** which municipal system the data comes from and who exports it.
- **Definitions:** what "opened" and "closed" mean operationally (e.g., does "closed" include lapsed renewals?), and which sector scheme is used.
- **Cadence and lag:** when each month is published and how stale it can be.
- **Known limitations, stated prominently:** registration data is not the whole economy — it misses informal activity, captures legal events rather than real-world open/close dates, and may lag reality. Say this loudly, not in a footnote ([CLAUDE.md §9](../../CLAUDE.md): false-precision principle).
- **Confidence:** where the data is uncertain, mark it. Never present a count as more precise than the underlying records support.

## 6. Versioning and corrections

- The standard itself is versioned (`v0.1`, `v0.2`, …); changes are documented with effective dates and rationale.
- Published months are immutable. Corrections are issued as a new dated file (`..._YYYY-MM_rev2.*`) with a one-line changelog; the original is preserved. **Published data is not un-published** — corrections are additive and transparent.

## 7. The pre-commitment

Published before the first unflattering month arrives, on the record by both the city and the pilot:

> *Every month is published as measured — including the months the numbers look bad. The standard does not flinch, and neither do we.*

This is what converts a one-time press release into trustworthy infrastructure.

---

*This standard is intentionally small. Resist adding fields, datasets, or finer granularity until the first dataset is live, mirrored, and referenced by someone outside the city. Compound over heroic.*
