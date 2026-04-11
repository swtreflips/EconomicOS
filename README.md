# econOS -- Economic Operating System

Open-source economic data infrastructure for developing and emerging economies. econOS transforms how people access economic information -- replacing lagging, unreliable, or nonexistent official statistics with near real-time data that empowers individuals to make better decisions about work, investment, education, and mobility.

In countries where central banks have stopped publishing data, where inflation makes prices stale within days, and where millions make migration decisions with almost no reliable information -- econOS fills the void.

**Start here:** [CLAUDE.md](CLAUDE.md) for the full project vision.

---

## Project Structure

### [00-foundations/](00-foundations/)
The intellectual bedrock -- why this project exists, what theory supports it, and what design principles guide it.
- **problem-statement/** -- The core arguments. Start with [investment-allocation-optimization.md](00-foundations/problem-statement/investment-allocation-optimization.md) -- the central thesis that economic growth is an optimization problem, and better information produces better allocation, less waste, and higher productivity
- **theoretical-foundations/** -- Akerlof, Hayek, Stiglitz, Hsieh & Klenow, mechanism design, behavioral economics
- **design-principles/** -- Multi-dimensional metrics, transparency, adaptability, anti-capture
- **philosophical-position/** -- Not central planning, not laissez-faire -- a high-resolution market system

### [01-data-infrastructure/](01-data-infrastructure/) -- CURRENT FOCUS
Phase 1: Making economic data near real-time. This is the foundation everything else depends on.
- **current-landscape/** -- How economic data is measured today in developing countries and reference economies (and where it fails)
- **modern-data-sources/** -- Mobile payments, web scraping, satellite imagery, remittance flows, social media, IoT
- **data-categories/** -- Synthesis: how modern sources combine into real-time indicator proxies
- **technical-challenges/** -- Nowcasting methodology, validation, bias, schemas, scalability
- **legal-and-privacy/** -- Data rights, aggregation boundaries, ethical considerations
- **existing-work/** -- Prior art: Billion Prices Project, developing country nowcasting, central bank experiments
- **proof-of-concept/** -- First target: real-time consumer spending and price tracking in a developing economy

### [02-algorithmic-coordination/](02-algorithmic-coordination/) -- Future
Pre-built analytical layer: translating raw data into actionable signals for key economic areas.

### [03-metrics-and-transparency/](03-metrics-and-transparency/) -- Future
Pre-built BI views for key life decisions: where to work, what to study, where to invest, whether to migrate.

### [04-governance/](04-governance/) -- Future
Open-source governance: how the project stays open, transparent, and resistant to capture.

### [05-implementation-strategy/](05-implementation-strategy/)
Phased rollout: first implementation country, then expansion to additional developing economies.

### [06-risks-and-challenges/](06-risks-and-challenges/)
Data gaps, informal economy, political risk, infrastructure limitations, adoption barriers.

### [07-open-questions/](07-open-questions/)
Critical assessment, highest-leverage areas, research agenda, and unresolved design questions.

### [references/](references/)
Bibliography, glossary, and comprehensive data sources catalog.

---

## Reading Order

1. [CLAUDE.md](CLAUDE.md) -- The full vision (5-minute read)
2. [investment-allocation-optimization.md](00-foundations/problem-statement/investment-allocation-optimization.md) -- **The core argument**: why better information = better allocation = faster growth
3. [01-data-infrastructure/README.md](01-data-infrastructure/README.md) -- Phase 1 roadmap
4. [07-open-questions/critical-assessment.md](07-open-questions/critical-assessment.md) -- Honest assessment and where to focus
5. Dive into whichever topic interests you from there
