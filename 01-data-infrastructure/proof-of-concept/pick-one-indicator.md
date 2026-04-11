# Picking the First Indicator: Why Consumer Spending + Real-Time Prices

## The Decision

econOS needs to build one thing first. One indicator, one proof-of-concept, one deliverable that demonstrates the core thesis: better information improves resource allocation. This document argues that the first indicator should be **real-time consumer spending and price tracking** -- a combined signal that tracks both what things cost and how much people are spending on them.

This is not a choice about what data would be "interesting to have." It is a choice about what demonstrably helps people allocate resources better, can actually be built with accessible data, and proves something about the broader project. Every candidate is evaluated against that standard.

---

## 1. Selection Criteria: What Makes a Good First Indicator?

The proof-of-concept must satisfy five criteria simultaneously. Getting four out of five is not enough -- the wrong first move wastes limited credibility and engineering effort on something that either cannot be built, does not matter, or proves nothing about the broader system.

### (a) High Allocation Impact

The indicator must directly help someone make a better economic decision. Not "better" in an abstract sense -- better in the concrete sense that a worker, business owner, investor, student, or diaspora family member uses the information to allocate their scarce resources (money, time, skills, location) more productively.

This is the econOS thesis in its purest form. Hsieh and Klenow (2009) demonstrated that eliminating misallocation in developing countries could increase manufacturing productivity by 30-60%. Jensen (2007) showed that fishermen with mobile phone access to price information reduced waste and increased income -- same fish, same boats, better information, better outcomes. The first indicator must operate on this mechanism: identical resources, better allocation through better information.

In a capital-scarce recovery, every dollar of investment, every worker's career decision, every remittance allocation matters disproportionately. The indicator that improves the most allocation decisions at the widest scale wins.

### (b) Technically Feasible with Available Data

The indicator must be buildable with data sources that are actually accessible -- not data that would be nice to have, not data that requires institutional partnerships that don't yet exist, not data that depends on government cooperation in a country where government data has been unreliable for a decade.

"Available" means: publicly scrapeable from the web, accessible via existing APIs, or collectible through methods that a small open-source team can execute without institutional agreements. In crisis economies, the data environment is hostile to approaches that require cooperation from central banks, financial regulators, or major banks. The first indicator cannot depend on doors that haven't been opened.

### (c) Fills a Void, Not Just Beats a Lag

In the United States, econOS would compete with existing data by being faster. The NY Fed Staff Nowcast beats the BEA GDP release by a few weeks. Affinity Solutions card data beats Census retail sales by a few days. The improvement is marginal -- from a 14-day lag to a 1-day lag on an indicator that already exists.

In developing countries with data voids, the value proposition is categorically different. Central banks have stopped publishing CPI data for years during hyperinflationary spirals. GDP estimates are published sporadically with questionable methodology. Labor market data barely exists for the informal economy. The proof-of-concept must target a void -- a space where reliable data genuinely does not exist -- not merely improve the timeliness of something that is already measured.

Filling a void creates exponentially more value than beating a lag. Any signal in a void is transformative. A slightly faster signal in a data-rich environment is incremental.

### (d) Demonstrable and Visible to Build Credibility

The proof-of-concept is not just a technical exercise. It is the first public artifact of econOS. It must be immediately understandable by non-economists, directly relevant to daily life, and visibly useful. If the first indicator requires three paragraphs of explanation for someone to understand why it matters, it fails as a proof of concept regardless of its technical merit.

Credibility is earned through demonstrated utility, not through methodological sophistication. The target audience for the proof-of-concept is not the World Bank or the IMF -- it is the worker in a developing country checking prices, the business owner setting today's price list, the diaspora family deciding how much to send home. If they use it, the credibility follows.

### (e) Extensible to Other Indicators

The first indicator should create infrastructure -- scrapers, processing pipelines, publication mechanisms, methodology documentation -- that extends to the next indicator and the one after that. Building a bespoke system for one narrow measurement that cannot be reused is engineering waste.

The ideal proof-of-concept creates a platform, not just a product.

---

## 2. The Candidates

Five candidates were evaluated. Each is a legitimate economic indicator with real value. The question is not whether each would be useful -- all would be -- but which best satisfies all five criteria simultaneously.

### 2.1 Consumer Spending + Real-Time Prices (Recommended)

**What it is:** A daily price index for consumer goods in a target developing country (food, household, personal care, electronics), combined with a weekly spending activity signal and a real-time effective local-currency/USD exchange rate derived from P2P markets.

**Allocation impact:** Extremely high. Every purchase is a resource allocation decision. Price information is the most fundamental market signal (Hayek, 1945). When a consumer knows that cooking oil costs 40% less in one store than another, or that prices in one city are 15% lower than another, or that their purchasing power has deteriorated 8% this month, they allocate differently. When a business owner can see price trends before setting tomorrow's menu, they price better. When a diaspora family can see what $200 actually buys this week back home, they send the right amount.

**Feasibility:** High. Data sources include dominant e-commerce platforms (product listings with prices), supermarket and pharmacy chains with web presences, delivery platforms, and P2P exchange platform local-currency/USDT rates. The Billion Prices Project already proved this methodology works for developing countries, including crisis economies.

**Void filling:** Total. Countries in crisis have gone years without official price data during severe inflation episodes. Central banks may resume publishing CPI data, but with contested credibility and monthly frequency. There is no independent, daily, transparent, goods-level price tracker for most developing economies.

**Visibility:** Maximum. Everyone understands prices. People in crisis economies have a visceral relationship with inflation. A tool that tells you "here is what things cost today, and here is how that compares to last week" requires zero explanation.

**Extensibility:** Strong. The scraping infrastructure extends to any web-based data. The processing pipeline (normalization, categorization, index construction) is reusable. The publication mechanism (API + website) serves all future indicators.

### 2.2 GDP Proxy / Composite Activity Index

**What it is:** A weighted composite of available signals (P2P exchange volume, electricity consumption, satellite nighttime lights, import data) that approximates real-time GDP movement.

**Allocation impact:** Moderate. GDP is a macro aggregate. Knowing that the economy grew 3% this quarter is useful for investors and policymakers, but it does not help a worker decide where to live, a business owner decide what to price, or a family decide how much to send home. GDP does not disaggregate into actionable decisions for individual economic agents.

**Feasibility:** Moderate-to-low. The strongest inputs (satellite nighttime lights from VIIRS, P2P exchange volume) are accessible. But a credible GDP proxy requires calibration against a known benchmark -- and in crisis economies, the benchmark itself (central bank GDP) is unreliable. What do you validate against? This is the problem Henderson, Storeygard, and Weil (2012) identified: nighttime lights work as a GDP proxy, but the relationship needs calibration, and calibration requires trustworthy baseline data.

**Void filling:** Partial. The IMF, World Bank, and independent consultancies already produce GDP estimates for crisis economies. They are lagged and uncertain, but they exist. A real-time GDP proxy would beat them on timeliness but would face immediate credibility challenges because it cannot be validated against official data that is itself contested.

**Visibility:** Low. GDP is an abstraction. Most people do not think in GDP terms. A headline that says "econOS estimates the economy grew 0.8% this quarter" is meaningful to economists and investors. It is not meaningful to the millions of people living in that economy.

**Extensibility:** Moderate. Satellite data infrastructure is reusable. But the composite construction methodology is specific to GDP and does not generalize easily to other indicators.

**Verdict:** Important for Phase 2, but too abstract, too hard to validate, and too distant from individual allocation decisions for a first proof-of-concept.

### 2.3 Labor Market / Employment Signals

**What it is:** Real-time tracking of job postings, wage levels, and employment demand across domestic and regional labor platforms (country-specific job sites, LinkedIn, regional employment platforms).

**Allocation impact:** Very high. Labor allocation -- where to work, what skills to develop, whether to migrate -- is among the highest-stakes allocation decisions individuals make. A nurse in a developing country deciding between two destination cities is making a 5-year resource allocation decision worth tens of thousands of dollars. Better information directly improves that decision.

**Feasibility:** Moderate. Job posting data is scrapeable from regional job platforms, LinkedIn, and local employment sites. But in many developing countries the labor market is 40-60% informal, and informal jobs do not appear on platforms. The scrapeable data represents a thin slice of the actual labor market. Wage data is even thinner -- most postings in developing countries do not include salary information. The signal-to-noise ratio is unfavorable for crisis economies specifically; it is better for countries with larger formal sectors.

**Void filling:** High. No systematic, real-time labor market intelligence exists for most developing countries. But the void is harder to fill with available data because the labor market is the most opaque part of the economy. The informal economy problem is maximally severe here.

**Visibility:** High. "Where are the jobs and what do they pay?" is immediately understandable.

**Extensibility:** Moderate. Job posting scrapers are specific to job platforms and do not generalize to other economic indicators.

**Verdict:** A strong Tier 1 priority -- identified as such in the project's highest-leverage ranking -- but the data coverage problem in crisis economies makes it a weaker first proof-of-concept than prices. Prices can be scraped comprehensively from e-commerce; jobs cannot be scraped comprehensively from platforms in a 50%+ informal economy. Better as a parallel or second initiative.

### 2.4 Exchange Rate / Currency Dynamics

**What it is:** A real-time effective exchange rate for the local currency, derived from P2P exchange platform local-currency/USDT trading data, supplemented by independent rate trackers.

**Allocation impact:** High in the currency decision itself -- should I hold local currency or dollars? should I price in dollars? -- but narrow. The exchange rate is one price, not a system of prices. It matters enormously for one specific decision (currency allocation) but less for the broader set of allocation decisions econOS aims to improve.

**Feasibility:** Very high. P2P exchange data is accessible via API. Independent rate trackers already publish parallel rates. This is the easiest indicator to build from a data-access perspective.

**Void filling:** Low. This is the one area where crisis economies often already have real-time market data. P2P exchange rates are already widely observed. Independent rate trackers already publish parallel rates multiple times per day. People in dollarized economies already know the exchange rate. econOS would be replicating existing coverage, not filling a void.

**Visibility:** High. Everyone in a multi-currency economy checks the dollar rate.

**Extensibility:** Low. Exchange rate tracking is a single data point requiring a single API connection. It does not create generalizable infrastructure.

**Verdict:** Essential as a component of the price-tracking system (the exchange rate is the price that sets all other local-currency prices), but too narrow and too already-covered to stand alone as the proof-of-concept. It should be embedded in the consumer spending + prices indicator, not built independently.

### 2.5 Regional Economic Activity

**What it is:** An index of economic activity disaggregated by state/province or city, using satellite nighttime lights, mobile data signals, and whatever transaction data can be obtained regionally.

**Allocation impact:** High for location decisions -- where to invest, where to open a business, where to move. Recovery in developing countries is geographically uneven. Different regions have different trajectories. Regional data would be extremely valuable.

**Feasibility:** Low-to-moderate. Satellite nighttime lights (VIIRS) provide regional disaggregation and are publicly available, but require substantial processing infrastructure and expertise. Mobile data signals require telecom partnerships that do not exist. Regional transaction data requires bank partnerships that do not exist. The combination of data access barriers and methodological complexity makes this a Tier 2 project.

**Void filling:** Total. No regional economic data exists for most developing countries in any regular, systematic form.

**Visibility:** Moderate. "Region X's economy is growing faster than the capital" is interesting but less immediately actionable than "your groceries cost 12% more than last month."

**Extensibility:** High for satellite-based infrastructure, but satellite processing is specialized and does not extend to web-scraping-based indicators.

**Verdict:** High value, wrong sequencing. Regional disaggregation should be built on top of the national price and spending signals, not before them. Build the national methodology first, then disaggregate.

---

## 3. Why Consumer Spending + Prices Wins

The recommendation is not marginal. Consumer spending and prices is the clearly dominant choice across all five criteria. Here is the deep argument.

### 3.1 Consumer Spending IS Resource Allocation at the Individual Level

Every purchase is an allocation decision. When a family in a developing country buys 2 kg of chicken instead of 3 kg of beef, they are allocating their budget based on relative prices, perceived quality, and income constraints. When they buy at a supermarket chain instead of a local corner store, they are allocating their time and transport costs against price savings. When they stock up on rice because they expect prices to rise, they are making an intertemporal allocation decision.

This is not a metaphor. Consumer spending is the economy's allocation engine. Household consumption represents roughly 60-70% of GDP in most market economies. In crisis economies, where government spending has collapsed and investment is minimal, household spending is an even larger share of the economic activity that actually occurs.

A real-time picture of what people are buying and what things cost is a real-time picture of how the economy is allocating resources at its most fundamental level. No other indicator captures this granularity of allocation behavior.

### 3.2 Price Information Is the Most Fundamental Market Signal

Hayek's central insight in "The Use of Knowledge in Society" (1945) was that prices encode information about relative scarcity. The price system is the mechanism through which dispersed knowledge is aggregated and transmitted. When the price of flour rises, it signals increased scarcity or demand. Producers respond by producing more. Consumers respond by substituting. Resources reallocate automatically, guided by price signals.

But this mechanism only works when prices are visible and current. When prices are opaque, outdated, or absent, the allocation mechanism breaks down. Resources flow to the wrong uses. Waste increases. Productivity falls.

In crisis economies, the price system is systematically destroyed -- first by government price controls that prevent prices from reflecting scarcity (leading directly to shortages), then by statistical blackouts that make prices invisible even after controls are relaxed. Central banks have stopped publishing CPI data for years. Citizens are left with no authoritative, comprehensive, transparent price data.

As dollarization stabilizes and controls are relaxed, the price system slowly recovers. But the information layer -- the part that makes price signals visible, comparable, and analyzable across goods, regions, and time -- does not exist in any systematic form. Rebuilding that layer is not just useful. It is the most direct possible intervention to improve market coordination.

Making prices visible, current, and comparable is the single highest-return information intervention available. It improves allocation automatically, through the market mechanism itself, without requiring anyone to build an algorithm or design an optimization model. The prices do the work.

### 3.3 In Crisis Economies, Price Data Can Be Literally Absent for Years

This point deserves separate emphasis because it is what distinguishes crisis economies from other developing country contexts.

This is not a story about data arriving two months late. This is a story about data not existing at all during the worst economic crises in a country's history. Central banks have stopped publishing regular CPI data for years during hyperinflationary episodes. During such periods:

- Inflation can accelerate from triple digits to six figures annually
- Currencies are redenominated, removing zeros
- Prices change daily or multiple times per day at the hyperinflationary peak
- Workers cannot negotiate wages against any benchmark
- Businesses set prices by guesswork, WhatsApp groups, and tracking the parallel exchange rate
- Contracts with CPI escalation clauses have no index to reference
- International organizations (IMF, World Bank) are forced to produce their own estimates with explicit uncertainty caveats
- Opposition groups may publish their own figures, which are dismissed by the government as politically motivated

The few independent sources that may exist -- PPP-based estimates by international economists, legislative commission figures, the Billion Prices Project's web-scraped data (through PriceStats) -- are typically either methodologically indirect (exchange-rate-based approaches cannot identify which goods are driving inflation), politically compromised (opposition estimates), or commercially restricted (sold to institutional clients, not published freely).

While some developing countries have functional statistical agencies that publish regular, credible CPI data with reasonable lag, many others experience partial or complete data blackouts during crises. Even countries that have had inflation measurement controversies (such as statistical agency manipulation for political purposes) may not experience voids as complete as the worst cases.

Any credible, independent, transparent, daily price signal for a crisis economy is not a marginal improvement. It is the creation of a capability that does not exist. The difference between having this data and not having it is not 5% better decisions. It is the difference between navigating by sight and navigating blind.

### 3.4 The Data Sources Are the Most Accessible

This is the pragmatic case, and it matters as much as the theoretical one. A proof-of-concept that cannot actually be built is worthless.

The data sources for consumer prices in developing countries are more accessible than for any other candidate indicator:

**Dominant e-commerce platforms:** Most developing countries have dominant e-commerce platforms with extensive product listings including prices, categories, locations, and seller information. Prices may be listed in both local currency and dollars. Product categories span food, household goods, electronics, personal care, automotive, and more. E-commerce product pages are structured and scrapeable. The Billion Prices Project used this exact approach -- scraping online retailers -- to produce daily price indexes for multiple developing countries.

**Supermarket and pharmacy chains with web presences:** Major retail chains in most developing countries maintain websites or apps with product listings and prices. These are directly scrapeable for food, household, and personal care product prices.

**Delivery platforms:** Food and grocery delivery apps operate in developing-country cities and list restaurant and store prices in their apps and web interfaces. These provide food and prepared meal pricing data.

**P2P exchange platforms:** The dominant local-currency/USDT trading platforms provide public APIs. Local-currency pairs have high liquidity and continuous trading in crisis economies. This gives a real-time market exchange rate that is treated as the de facto rate by merchants and consumers. Combined with product prices in local currency, this allows conversion to dollar-denominated prices for cross-time comparability.

**Independent rate trackers:** Multiple services track parallel exchange rates through informal market surveys and aggregation. These provide cross-validation for P2P rates and capture cash-dollar exchange rates that may differ from crypto-based rates.

**WhatsApp and Telegram price groups:** People in crisis economies organically share prices in chat groups -- a form of crowdsourced price intelligence. While harvesting this data at scale raises practical and ethical questions, its existence demonstrates that the demand for real-time price information is intense enough that informal networks emerge to fill the void.

Compare this data landscape to the alternatives:

- **GDP proxy:** Requires satellite data processing (specialized), mobile payment volume data (inaccessible without central bank cooperation), electricity consumption data (utility partnerships needed), import data (customs data unreliable)
- **Labor market:** Requires scraping job platforms that cover a minority of the labor market. The 50%+ informal economy in many developing countries is invisible on platforms
- **Regional activity:** Requires satellite processing infrastructure and calibration against ground truth that does not exist
- **Exchange rate:** Already covered by existing services

The consumer price data sources are publicly accessible, structured, scrapeable with standard tools, and proven by prior art (the Billion Prices Project). No other candidate has this combination.

### 3.5 Two Indicators in One: Activity and Price Levels

Most candidate indicators measure one dimension of the economy. Consumer spending + prices measures two simultaneously:

**Price levels:** What do things cost? How fast are prices changing? Which categories are inflating fastest? Is dollarization progressing or retreating? This is the inflation measurement dimension -- the CPI replacement function.

**Economic activity:** How much are people spending? Are transaction volumes rising or falling? Is spending shifting between categories (from discretionary to essential, or vice versa)? This is the GDP/consumption measurement dimension -- the activity signal.

These two dimensions are deeply complementary. Prices without volume tell you what things cost but not whether people can afford them. Volume without prices tells you that transactions are happening but not what they mean in real purchasing power terms. Together, they provide a picture of the economy that neither alone can offer.

In the US, these two measurements come from different agencies: the BLS produces CPI (prices), the BEA produces personal consumption expenditure data (spending), and the Census Bureau produces retail sales (volume). In many developing countries, none of these exist in reliable, current form. econOS can produce both from the same data infrastructure.

### 3.6 Direct Service to Individual Allocation Decisions

The proof-of-concept must serve the BI use cases -- the actual decisions that real people face. Consumer spending + prices maps directly to the decisions econOS is designed to support:

**"Can I afford to live in city A vs. city B?"** Requires comparative price data across cities for rent, food, transport, and basic goods. The price-tracking infrastructure produces this directly.

**"Is my purchasing power improving or deteriorating?"** Requires a price index that can be compared against wage trends. The daily price index answers the price side of this question.

**"Should I price my product in dollars or local currency?"** Requires data on the price dynamics in each currency, the exchange rate trajectory, and what competitors are doing. The dual-currency price tracking and exchange rate data address this.

**"What is the real exchange rate this week?"** The P2P exchange rate, cross-validated against other sources, provides this in real time.

**"How much does $200 buy back home this month?"** The diaspora family sending remittances needs exactly this: a purchasing-power conversion that maps a dollar amount to a goods basket at current local prices.

**"Is this a good time to invest in a small business?"** Requires spending trends (are consumers spending more?), price stability data (are prices stable enough to plan?), and exchange rate trends (is the local currency stabilizing?). All three come from the consumer spending + prices indicator.

No other candidate indicator maps this directly to this many individual allocation decisions.

### 3.7 The Billion Prices Project Already Proved This Works

This is not a theoretical proposal. The methodology has been validated in developing countries, including crisis economies.

The Billion Prices Project (BPP), founded by Alberto Cavallo and Roberto Rigobon at MIT, collected daily online prices from retailers in over 60 countries, including crisis economies. The project demonstrated that:

- **Automated price collection from online retailers was feasible even during economic crises.** Despite infrastructure deterioration, power outages, and economic chaos, retailers in crisis economies maintained web presences with scrapeable prices.
- **Daily frequency captured price dynamics that monthly CPI could not.** In hyperinflationary environments where prices changed daily, the BPP's daily scraping was the only way to track the actual speed of price changes.
- **Web-scraped prices correlated with exchange rate movements,** validating the relationship between the parallel rate and the consumer price level.
- **The resulting indexes diverged dramatically from official central bank data** during periods when governments were suppressing inflation numbers, providing independent verification of crisis severity.

The BPP data was commercialized through PriceStats (later acquired by State Street Global Markets) and sold to institutional clients. It was never published as open-source, freely accessible infrastructure. This is precisely the gap econOS fills: taking a proven methodology and making it available to everyone, not just hedge funds.

Cavallo and Rigobon published the methodology in the *Journal of Economic Perspectives* (2016), providing a detailed, replicable framework. The academic validation is complete. The engineering is proven. What remains is building it as permanent, open, transparent infrastructure -- which is exactly what econOS is designed to do.

---

## 4. What "Success" Looks Like

The proof-of-concept must have concrete, measurable deliverables. "We produced an interesting paper" is not success. "People reference our data when making decisions" is success. Here is what the proof-of-concept must produce.

### 4.1 A Daily Consumer Price Index

**Scope:** Four to six goods categories covering the essentials of household consumption:

1. **Food and beverages** -- staples (rice, flour, cooking oil, chicken, beef, eggs, milk), processed foods, beverages. This is the largest share of household spending in developing countries, estimated at 35-50% of household budgets in lower-income segments.
2. **Household goods** -- cleaning products, paper goods, basic household supplies.
3. **Personal care** -- hygiene products, basic pharmaceuticals (where available without prescription).
4. **Electronics and appliances** -- phones, chargers, small appliances. Relevant as a proxy for discretionary spending and as a dollarized goods category.
5. **Prepared food / restaurant prices** -- delivery platform menu prices as a proxy for food-away-from-home costs.

**Methodology:**
- Daily automated scraping of product listings from dominant e-commerce platforms, supermarket chains, pharmacy chains, and major delivery platforms in the target country
- Matched-model approach: track the same products over time to isolate price changes from product mix changes (following BPP methodology)
- Dual-currency recording: capture whether each price is listed in local currency or dollars; convert using the P2P exchange rate for comparability
- Category-level sub-indexes published alongside the composite index
- Weekly rolling averages to smooth daily noise; monthly aggregates for longer-term comparison

**Output:** A publicly accessible daily price index (composite + category sub-indexes), published on a website and via API, with full methodology documentation. Updates by 10:00 AM local time each day. Historical data downloadable in standard formats (CSV, JSON).

### 4.2 A Weekly Spending Activity Signal

**Scope:** A proxy for the volume and trajectory of consumer spending, derived from whatever transaction-adjacent data is accessible without institutional partnerships.

**Possible inputs:**
- E-commerce platform listing volume and turnover indicators (new listings, items marked as sold, listing durations)
- Delivery platform order volume proxies (menu availability, delivery time estimates as congestion signals)
- P2P exchange trading volume (a proxy for currency exchange activity, which correlates with economic activity)
- Google Trends for commerce-related search terms in the target country (acknowledging the Google Flu Trends caveat: search trends are supplementary, not primary)

**Methodology:**
- Composite index weighted by signal quality and coverage
- Normalized to a base period for interpretability
- Explicit uncertainty bands reflecting the indirect nature of the measurements
- Cross-validation between signals to detect anomalies

**Output:** A weekly spending activity index, published each Monday for the prior week, with methodology documentation and uncertainty quantification. This is the less precise of the two components, and the methodology must be transparent about its limitations.

### 4.3 A Real-Time Local-Currency/USD Effective Exchange Rate

**Scope:** The de facto market exchange rate for the local currency, derived from actual transaction data rather than government announcements.

**Sources:**
- **Primary:** P2P exchange platform local-currency/USDT bid-ask midpoint, updated continuously. P2P platforms are typically the deepest liquidity pool for currency exchange in crisis economies and the rate merchants and consumers actually reference.
- **Secondary:** Cross-validation against independent rate tracking services and other parallel rate sources.
- **Spread calculation:** The gap between the central bank official rate and the P2P effective rate, published as a daily "credibility spread" -- a direct measure of how much the official rate diverges from market reality.

**Methodology:**
- Continuous polling of P2P exchange API for local-currency/USDT trading pair
- Volume-weighted average price (VWAP) calculation over rolling windows (hourly, daily)
- Bid-ask spread tracking as a liquidity/volatility signal
- Central bank official rate captured daily for spread calculation

**Output:** A real-time exchange rate dashboard (updated hourly), daily VWAP, and daily official-vs-market spread. This component provides the exchange rate conversion that makes the price index interpretable in dollar terms, and it is independently useful as the most transparent local-currency exchange rate tracker available.

### 4.4 Publication and Credibility Standards

All three components must be:

- **Published openly:** Free, no paywall, no registration. Website + API + downloadable data files.
- **Updated automatically:** Scraping, processing, and publication are automated. No manual intervention required for routine updates.
- **Methodology-transparent:** Full documentation of data sources, scraping methods, index construction, weighting, and known limitations. Anyone can audit the methodology and, in principle, replicate it.
- **Version-controlled:** Methodology changes are documented with effective dates. Historical data is preserved under prior methodology for continuity.
- **Honest about limitations:** The index covers online-listed prices, not all prices. It is biased toward the formal, digital, urban economy. It does not capture informal market prices, rural prices, or the prices experienced by the poorest populations who buy from street vendors in cash. These limitations are stated prominently, not buried in footnotes.

### 4.5 Credibility Milestones

**Within 3 months:**
- Daily price index operational and published
- Exchange rate tracker operational
- Methodology documentation complete
- Website and API live

**Within 6 months:**
- Spending activity signal operational
- Local media or analysts reference the data
- Independent researchers begin using the data
- At least one concrete example of the data informing an allocation decision (a business pricing decision, a migration cost comparison, a remittance value calculation)

**Within 12 months:**
- The econOS price index is more trusted than official CPI for tracking current price dynamics in the target country
- Diaspora communities reference the data when discussing purchasing power back home
- The data is cited in at least one academic or institutional report
- The methodology has been independently reviewed and critiqued (critique is a sign of relevance, not failure)
- Other developing countries express interest in replicating the approach

The 12-month target is not arbitrary. It mirrors the trajectory of the Billion Prices Project, which went from initial scraping to institutional credibility in approximately 18-24 months. econOS has the advantage of building on proven methodology, which should compress the timeline.

---

## 5. What This Proves for the Broader Project

The proof-of-concept is not just about prices. It is about demonstrating five things that determine whether econOS has a viable future.

### 5.1 The Allocation Thesis Is Demonstrated

If the price data is used -- if a business owner prices more accurately, if a family calibrates their remittance to purchasing power, if a worker uses price differentials to evaluate city-to-city moves -- then the core econOS thesis is empirically supported: better information improves resource allocation.

This is not something that can be proven in a whitepaper. It can only be proven by building data infrastructure that people actually use to make better decisions. The proof-of-concept is the experiment.

The evidence chain is: (1) we produce price data that did not previously exist in this form, (2) economic agents access this data, (3) their decisions demonstrably improve (or at minimum, they report that the data informed their decisions). Steps 1 and 2 are within econOS's control. Step 3 requires observation and, eventually, measurement -- but even qualitative evidence (user testimonials, media citations, analyst adoption) is meaningful for an early-stage proof of concept.

### 5.2 The Methodology Extends to Other Indicators

The web-scraping infrastructure built for prices extends directly to:

- **Labor market data:** The same scraping framework that collects prices from e-commerce platforms can collect job postings from regional job sites and LinkedIn
- **Rental and housing data:** Real estate listings on property platforms provide housing cost data using the same scraping technology
- **Trade and commercial activity:** Online marketplace listing volumes, categories, and turnover serve as proxies for commercial activity
- **Regional disaggregation:** Prices scraped from platforms can be tagged by seller location, enabling city-level and state-level price comparisons without additional data sources

The processing pipeline -- data normalization, categorization, index construction, dual-currency handling -- is reusable infrastructure. Building it for prices means building it for everything that follows.

### 5.3 Credibility Is Established for Phase 1 Expansion

The proof-of-concept is the entry ticket to institutional conversations. A functioning, publicly accessible, transparent price tracker gives econOS something to point to when approaching:

- **Banks** for aggregate transaction data partnerships: "Here is what we built with public data. Imagine what we could build with yours."
- **NGOs and international organizations** for funding and support: "Here is a working system that demonstrates our methodology."
- **Academic researchers** for validation and collaboration: "Here is our data, our methodology, and our code. Help us improve it."
- **Media and analysts** for distribution: "Here is a new data source for your coverage of the economy."

Without a working proof-of-concept, these conversations are abstract. With one, they are concrete.

### 5.4 The BI Layer Has Its First Real Data Feed

The pre-built BI views that econOS envisions -- "Can I afford to live in this city?", "Is the recovery real?", "What does $200 buy back home?" -- require data feeds. The consumer spending + prices indicator provides the first feed for at least three of these views:

- **Cost of living comparison:** Requires prices by city and category. The price index provides this.
- **Purchasing power tracker:** Requires a price index over time. The daily index provides this.
- **Remittance value calculator:** Requires current prices for a goods basket plus the exchange rate. Both are produced by the proof-of-concept.

These BI views are what turn raw data into allocation-improvement tools for regular people. The proof-of-concept is what turns the BI views from mockups into functional products.

### 5.5 The Open-Source Model Is Validated

The Billion Prices Project proved the methodology but kept the data commercial (PriceStats was a paid product for institutional clients). econOS takes the same proven approach and makes it open-source, freely accessible infrastructure.

If the open-source model works -- if people use the data, if the methodology is audited and improved by external contributors, if the infrastructure is maintained and extended by a community -- then econOS has demonstrated something the BPP did not: that real-time economic data infrastructure can function as a public good, not just a commercial product.

This has implications beyond the first implementation country. If the model works in the hardest possible environment (a data-void, crisis-recovery economy), it can work in any developing economy where official data is lagged, unreliable, or absent. The proof-of-concept proves the concept not just for one indicator in one country, but for a class of interventions in a class of economies.

---

## 6. Implementation Considerations

### 6.1 Known Risks

**Website fragility:** Retail websites in developing countries experience downtime due to power outages, server issues, and infrastructure degradation. The scraping system must be resilient to intermittent data loss and must not treat missing data as zero prices. The BPP faced this exact problem and documented workarounds (interpolation, multi-source redundancy).

**Representativeness bias:** Online prices are not all prices. The poorest populations buy from informal markets, street vendors, and small-scale merchants where prices may differ from online listings. The index will systematically under-represent the price experience of the most economically vulnerable populations. This must be stated clearly and prominently.

**Anti-scraping measures:** Retailers may implement CAPTCHAs, rate limiting, or structural changes that break scrapers. The system must be maintained actively. This is an ongoing operational cost, not a one-time build.

**Dual-currency complexity:** Handling prices in both local currency and dollars, converting between them at a rate that changes daily, and presenting results in a way that is meaningful to users who transact in both currencies is analytically nontrivial. The methodology must be rigorous but the presentation must be accessible.

**Political sensitivity:** Independent economic data in countries with data blackouts has historically been politically charged. Statistical blackouts are political decisions. Opposition estimates are dismissed as political attacks. econOS must be scrupulously non-partisan and methodologically transparent to avoid being dismissed as politically motivated by any faction.

### 6.2 What Comes Next

If the proof-of-concept succeeds, the natural expansion path is:

1. **Regional disaggregation** of the price index (major cities across the target country) -- achievable by tagging scraped data by seller location
2. **Labor market intelligence** -- applying the same scraping infrastructure to job platforms
3. **Housing and rental costs** -- extending price tracking to real estate listings
4. **Second-country expansion** -- replicating the methodology for another country's data sources, ideally one with a stronger institutional data environment for validation
5. **Composite activity index** -- combining the spending signal with satellite and exchange rate data to approximate GDP movement

Each step builds on the infrastructure and credibility established by the proof-of-concept. The sequence matters: start with what is most accessible and most visible, then extend to what is harder and more complex.

---

## 7. The One-Paragraph Summary

Consumer spending and real-time prices is the right first indicator for econOS because it sits at the intersection of maximum allocation impact and maximum data accessibility. Prices are the most fundamental market signal -- the mechanism through which the entire economy coordinates -- and crisis economies have gone years without credible price data during severe economic collapse. The data sources (e-commerce platforms, supermarket chains, P2P exchange platforms) are publicly accessible and the methodology (web-scraped daily price indexes) was already validated for developing countries by the Billion Prices Project at MIT. A daily price index plus a real-time exchange rate plus a weekly spending signal gives individual economic agents -- the worker, the business owner, the diaspora family -- the information they need to allocate their scarce resources more productively. That is not just the proof-of-concept for econOS. It is the thesis of econOS, made tangible.
