# econOS Design Principles

## What This Document Is

These are the principles that govern every design decision in econOS -- from which data source to prioritize, to how a dashboard renders on a phone in Maracaibo, to whether a feature ships this month or waits for better data. They are not aspirations. They are decision-making tools.

Every principle here resolves a real tradeoff. When two good ideas conflict, these principles determine which one wins. When a contributor asks "should we build this?" the answer comes from running the proposal against these principles and seeing what survives.

The principles are grounded in a specific context: econOS is open-source economic data infrastructure for Venezuela and Colombia, built on the thesis that economic growth is an optimization problem. Better information leads to better resource allocation, which leads to less waste, higher productivity, and faster growth. Every principle here serves that chain.

---

## Principle 1: Allocation-First

**Every feature is judged by: "Does this help someone allocate resources better?"**

### Why it matters

econOS exists to improve resource allocation. Not to publish data for its own sake. Not to build elegant systems. Not to win academic citations. The entire justification for the project -- the chain from information to allocation to productivity to growth -- depends on the data actually reaching someone making an actual decision about an actual scarce resource.

In Venezuela, the stakes of this principle are concrete. A family deciding whether to invest their savings in a bakery or a motorcycle repair shop. A nurse weighing Bogota against Lima. A student choosing between systems engineering and accounting. A diaspora family sending $200 home and wondering whether it should go to Caracas or Barquisimeto. These are allocation decisions. The quality of these decisions, multiplied across millions of people, IS the Venezuelan recovery.

Hsieh and Klenow (2009) showed that misallocation in developing countries reduces manufacturing productivity by 30-60%. For Venezuela's roughly $100B economy, even a 10% reduction in misallocation means $10B in additional annual output. That number is not theoretical. It is the cumulative effect of millions of people making slightly better decisions about where to work, what to build, and where to invest -- because they had better information.

### What it means in practice

- Before building any feature, ask: who is the allocator, what is the resource, and how does this help them allocate it better?
- A price tracker is allocation-first because it tells a worker what their wages actually buy, tells a business what to charge, and tells a diaspora family what their remittance purchases.
- A pretty visualization that doesn't connect to a decision anyone is making fails this test, no matter how technically impressive.
- Data granularity decisions are allocation decisions. National average inflation is less useful for allocation than city-level prices, because nobody lives in "national average." The worker lives in Valencia. The business is in Maracaibo. The allocation happens locally.
- If a feature helps researchers but not the bakery owner, it's lower priority. Researchers are not the primary allocators in a recovering economy. Workers, small business owners, students, and diaspora families are.

### The tradeoff it resolves

**Allocation-first vs. comprehensiveness.** The temptation in any data project is to build the complete picture before shipping anything. Track every sector, every region, every indicator. econOS rejects this. The question is never "is this data interesting?" but "does someone need this data to make a better decision with their money, time, or skills?" If yes, ship it. If it's interesting but doesn't connect to allocation, it waits.

This principle also resolves the **academic vs. practical** tension. Academic rigor is important, but econOS is not a research project. It is infrastructure for people making decisions under uncertainty with scarce resources. A methodologically imperfect price signal that a shop owner in Petare can use today is worth more than a methodologically perfect one that arrives in six months.

### When to break it

When building foundational infrastructure that doesn't directly face a user but enables future allocation-improving features. A data pipeline, a scraping framework, a validation methodology -- these don't help anyone allocate resources directly, but without them nothing else works. The test here is: does this infrastructure unlock allocation-improving features within a reasonable timeframe? If yes, it passes. If it's infrastructure for infrastructure's sake, it fails.

Also break it for data that serves accountability rather than individual allocation -- for example, tracking whether official BCV data diverges from market reality. This doesn't help a specific person allocate better, but it serves the broader goal of building a trustworthy information environment. The exception should be narrow: accountability data that disciplines the information ecosystem, not general-purpose transparency for its own sake.

---

## Principle 2: Open by Default

**Data, code, and methodology are public. Period.**

### Why it matters

This principle is not idealism. It is a direct response to what happened in Venezuela.

The BCV stopped publishing economic data. The government suppressed inflation statistics during hyperinflation that reached an estimated 130,000% in 2018. Official GDP figures, when they existed, were not credible. The country experienced a 75% GDP contraction -- worse than the US Great Depression -- and the institution responsible for measuring the economy went dark. Seven million people emigrated with almost no reliable data to guide the most consequential decisions of their lives.

This is what happens when economic information is controlled by a single institution with political incentives to suppress it. The information layer breaks, the allocation layer breaks, and the economy follows.

econOS is the structural antidote. Not because open source is fashionable, but because openness is the only architecture that survives political capture. If the data is public, it cannot be selectively withheld. If the code is open, the methodology cannot be secretly manipulated. If anyone can fork the project, no single actor can shut it down.

The analogy is not to open-source software projects that happen to be free. The analogy is to GPS: infrastructure that is openly available and that anyone can build on. econOS is economic positioning infrastructure. It tells you where you are and what's around you. That information belongs to everyone.

### What it means in practice

- All aggregate data outputs are freely accessible. No paywall, no login, no registration. You visit the page, you see the data.
- All code is public on day one. Not "open-sourced eventually" -- public from the first commit. The moment there is something valuable enough to capture is too late to open it.
- All methodology is documented. Every number on the dashboard links to a page explaining: what data sources were used, how they were combined, what the known limitations are, when the data was last updated.
- Model weights, scoring algorithms, and composite index calculations are published. If econOS says inflation is 8% this month, anyone should be able to reproduce that number from the published methodology and data.
- The project is forkable. If the maintainers make bad decisions, anyone can take the code, the data, and the methodology and build something better. This is not a failure state -- it is the immune system.

### The tradeoff it resolves

**Openness vs. competitive advantage.** In a normal startup, proprietary data is the moat. You collect data, you keep it private, you sell access. econOS deliberately rejects this model. The "moat" is not data exclusivity -- it is trust, methodology quality, and community. Proprietary economic data is exactly the problem econOS exists to solve. You cannot fix information asymmetry by creating new information asymmetry.

**Openness vs. data partnerships.** Some data providers may only share data if it stays private. This creates a genuine tension. The resolution: aggregate outputs are always public, even if specific source-level data is restricted by partnership terms. The composite price index is public; the individual scraped prices from a specific retailer may be governed by that retailer's terms. The methodology for combining sources is always public, even if one input is restricted. Never let a partnership compromise the public nature of the output.

### When to break it

Privacy. Individual-level data is never published, even if it is technically accessible. Aggregate spending in a neighborhood is public; a specific family's transactions are not. This is not a difficult call in most cases, but it becomes harder in small markets. If a "sector" in a small Venezuelan city has three businesses, publishing sector-level data effectively reveals individual business performance. The rule: aggregation must be sufficient to prevent individual identification. When in doubt, aggregate more.

Also: security-sensitive operational details. The specific IP addresses of scraping infrastructure, API keys, and server configurations are not public. The methodology is open; the operational security of the infrastructure is not.

---

## Principle 3: Mobile First, Spanish First

**Designed for Venezuelan and Colombian users, on the devices they actually have, in the language they actually speak.**

### Why it matters

This principle sounds like a UX guideline. It is actually a statement about who econOS is for.

Most Venezuelans and Colombians access the internet through smartphones -- often mid-range or budget Android devices on mobile data connections that are neither fast nor reliable. In Venezuela specifically, fixed broadband infrastructure has degraded significantly since the crisis. Mobile is not one channel among many. It is THE channel.

Spanish is not a localization afterthought. It is the primary language of the primary users. Every piece of text, every label, every methodology explanation, every error message is written first in Spanish, then translated to English for the international audience. This inversion matters because it determines what gets attention. When Spanish is the translation target, it gets less care -- awkward phrasing, untranslated technical terms, culturally mismatched metaphors. When Spanish is the source, it reads naturally to the people who need it most.

The combination -- mobile first AND Spanish first -- is a commitment to designing for a Venezuelan worker checking prices on a bus, not for a researcher at a university with a widescreen monitor and fluent English. Both will use econOS. But the Venezuelan worker is the design target. If the experience is good for them, it will be good for everyone. The reverse is not true.

### What it means in practice

- Page weight under 500KB. No heavy JavaScript frameworks that assume broadband. No high-resolution images that assume unlimited data. Every byte costs money on a metered mobile plan.
- Load time under 3 seconds on a 3G connection. This is a hard constraint, not a goal. If a feature makes the page slow, the feature is redesigned or cut.
- Touch targets sized for thumbs, not cursors. Layouts that work on a 5-inch screen. No hover states that assume a mouse.
- Offline capability where possible. Cache the last-known data so the dashboard is useful even when connectivity drops. In Venezuela, connectivity drops.
- All primary content in Spanish. Technical methodology documentation may exist in English first (because much of the academic literature is in English), but user-facing content is Spanish-native.
- Venezuelan and Colombian Spanish, not Castilian. "Chamba" is a word. "Tasa" means exchange rate colloquially. The language matches how the users actually talk about money, work, and prices.
- Currency display handles the dual-currency reality. In Venezuela, some prices are in bolivares, some in dollars, some in both. The interface doesn't force a single denomination -- it reflects how people actually transact.

### The tradeoff it resolves

**Accessibility vs. feature richness.** A desktop BI dashboard can have hover tooltips, multi-panel layouts, interactive filters, drill-down menus, and real-time streaming updates. A mobile-first dashboard cannot. The resolution: if it doesn't work on mobile, it doesn't ship as a primary feature. Desktop enhancements can exist, but the mobile experience is the canonical one. This means simpler interfaces, fewer panels per view, more scrolling and less clicking, larger text, and more aggressive data summarization.

**Spanish-first vs. contributor accessibility.** Most open-source contributors globally work in English. Code comments, commit messages, and technical documentation in Spanish raise the barrier for international contributors. The resolution: code and technical infrastructure are in English (the lingua franca of software development). User-facing content is in Spanish. Documentation that matters for contributors (architecture docs, contribution guides) is bilingual. Documentation that matters for users (methodology explanations, dashboard help text) is Spanish-first.

### When to break it

When the user is not a Venezuelan or Colombian individual. The API layer -- raw data access for researchers, developers, and institutions -- does not need to be mobile-first. It needs to be well-documented, standards-compliant, and reliable. Researchers accessing the API from a Python script don't need a mobile interface. The principle applies to the product layer (dashboards, BI views) that regular people use. The infrastructure layer follows standard software engineering conventions.

Also: English-first is acceptable for content that serves the international development community, diaspora organizations, or academic collaborators, as long as the Spanish version exists and is not a degraded translation.

---

## Principle 4: Translate, Don't Prescribe

**Show data, let people decide. econOS is a lens, not a compass.**

### Why it matters

The distinction between information infrastructure and advisory infrastructure is the most important architectural decision in econOS. Get it wrong and the project becomes either a paternalistic recommendation engine ("move to Bogota!") or a technocratic control system ("your optimal career is accounting"). Both paths lead to distrust, misuse, and eventual rejection.

The thesis of econOS is Hayekian: knowledge is dispersed. No algorithm knows the full context of a Venezuelan nurse's decision about whether to emigrate. She knows her family situation, her risk tolerance, her connections in different cities, her non-economic preferences, her assessment of political trajectory. econOS knows wages, job postings, cost of living, and exchange rates. The combination of her contextual knowledge and econOS's structured data produces a better decision than either alone. But only if econOS presents its data and steps back.

This principle also addresses the trust problem directly. In Venezuela, institutions that told people what to think -- about prices, about the economy, about opportunity -- were systematically wrong and systematically self-serving. "Trust us, the economy is fine" while hyperinflation destroyed savings. "Trust us, there are no shortages" while shelves were empty. econOS builds credibility by doing the opposite: here is what we measured, here is how we measured it, here is what we don't know. You decide what it means for you.

### What it means in practice

- BI views present data, not recommendations. The labor market view shows wages, job postings, cost of living, and trends for different cities. It does NOT say "you should move to Bogota." The user combines this data with everything else they know and makes their own decision.
- No rankings that imply a single "best" option. Cities are not ranked from best to worst. Fields of study are not ranked from most to least promising. Instead: here are the dimensions that matter (wages, demand, cost of living, growth trajectory), here is where each option stands on each dimension, here are the tradeoffs. The user weights the dimensions according to their own priorities.
- Methodology is always visible. Every composite metric shows its components, its weights, and its data sources. If econOS combines three signals into a "regional activity index," the user can see the three signals individually and decide whether the composite captures what matters to them.
- Uncertainty is shown, not hidden. When the data is noisy, the confidence interval is wide, and the dashboard says so. "We estimate inflation between 6% and 12% this month" is honest. "Inflation is 9%" when you actually don't know is dishonest -- and it's exactly what the BCV did before going silent entirely.
- Language is neutral. "Job postings in nursing increased 40% in Bogota this quarter" is translation. "Nursing is a great career move right now" is prescription. econOS uses the first form.

### The tradeoff it resolves

**Translation vs. accessibility.** Raw data is not useful to most people. A CSV of 50,000 job postings is technically informative but practically useless to a worker deciding where to move. The BI layer exists to make data accessible -- to translate it into views that non-analysts can understand. The tension is that every act of translation involves choices: which dimensions to highlight, how to aggregate, what to put on the default view. These choices shape perception even without explicit recommendations.

The resolution: be transparent about the translation choices. Show the methodology. Let users adjust parameters. Offer multiple views of the same data. And always provide access to the underlying data for users who want to do their own analysis. The BI layer is a lens that helps you see; it is not the only lens, and it never claims to be.

**Translation vs. engagement.** Recommendations drive engagement. "Move to Bogota -- 3x more job postings in your field!" gets more clicks than a neutral data table. The resolution: econOS optimizes for decision quality, not engagement. If the neutral presentation is less viral, that's acceptable. The goal is not maximum traffic. The goal is better allocation decisions. A user who makes a well-informed decision based on a boring data table has been served better than one who makes a hasty decision based on an exciting recommendation.

### When to break it

When the data is unambiguous and the stakes are high. If the exchange rate data shows a sudden, large divergence between the official rate and the market rate, it is appropriate to surface this prominently -- not as a recommendation, but as a factual alert: "The spread between the BCV rate and the Binance P2P rate widened to X% this week, the largest gap in Y months." This is still translation, not prescription, but it is active translation -- the system is drawing attention to something the user should probably notice.

Also: tutorials and onboarding. When a new user arrives at the dashboard, some guidance on how to read the data -- what the exchange rate spread means, how to interpret a confidence interval, what a job posting trend indicates -- is educational, not prescriptive. The line is: explain what the data IS, not what the user should DO about it.

---

## Principle 5: Partial Is Better Than Nothing

**Don't wait for perfect data. Imperfect real-time views beat the void.**

### Why it matters

This principle exists because the alternative to imperfect data in Venezuela is not perfect data. It is no data.

The BCV did not stop publishing data and then some other institution stepped in with better data. The data just stopped. Inflation estimates during hyperinflation ranged from 100,000% to over 1,000,000% depending on methodology and time period -- and most Venezuelans had access to none of these estimates in real time. They experienced inflation as the daily reality of prices changing faster than they could track, with no authoritative source telling them what was happening at an aggregate level.

In this context, the academic instinct to wait for methodological rigor before publishing is not caution. It is complicity with the void. A price index based on web-scraped data from 500 products in three cities is not comprehensive. It misses the informal economy, rural areas, and services. But it is infinitely more useful than the nothing that currently exists. "Infinitely" is not hyperbole -- the current denominator is zero.

The Billion Prices Project demonstrated this. When Alberto Cavallo and Roberto Rigobon started scraping online prices in Argentina and Venezuela, their methodology was imperfect. It over-represented goods sold online, under-represented services, and had limited geographic coverage. But it was the only independent, near-real-time price signal available. It was cited by the IMF, used by investors, and trusted by the public -- not because it was perfect, but because it was there.

### What it means in practice

- Ship the first version of any indicator as soon as it's minimally credible, not when it's comprehensive. A price tracker covering Caracas, Maracaibo, and Valencia is worth shipping even though it doesn't cover Barquisimeto, Ciudad Guayana, or San Cristobal yet.
- Every published metric includes explicit statements of what it DOESN'T cover. "This price index covers approximately 500 products from online retailers in 3 major cities. It does not cover services, informal markets, or rural areas. Coverage is being expanded." This is not a disclaimer -- it is part of the data product.
- Confidence indicators are mandatory. Every data point has a signal quality marker: is this based on multiple corroborating sources, a single source, or an extrapolation? The user decides whether the confidence level is sufficient for their decision.
- Data freshness is displayed prominently. "Last updated: 3 hours ago" or "Data from: March 25, 2026." Stale data that looks current is worse than no data -- it creates false confidence.
- Coverage gaps are mapped visually. If the labor market data covers Caracas and Bogota but not Barquisimeto, the dashboard shows this explicitly. The user knows what they're seeing and what they're not.
- New data sources are integrated incrementally. Don't wait to launch until you have satellite data, transaction data, job postings, AND prices all working. Launch with prices. Add exchange rates next week. Add job postings next month. Each addition makes the system more useful, and waiting for all of them means launching with none of them.

### The tradeoff it resolves

**Speed vs. accuracy.** This is the central tension in any real-time data system. Official statistics are accurate (within methodology) but slow. Real-time web-scraped data is fast but noisy. econOS chooses speed with transparency -- publish fast, show the uncertainty, and improve the methodology continuously. The user gets to decide whether speed with known uncertainty is more useful to them than accuracy with a three-month lag. For most allocation decisions in a fast-moving economy, it is.

**Completeness vs. usefulness.** A comprehensive economic dashboard covering every sector, every region, every indicator, every demographic is a beautiful vision and a recipe for never shipping anything. The resolution: start with the indicators that have the highest allocation impact (prices, exchange rate, jobs) in the locations with the highest need (Venezuela's major cities), and expand from there. Every version is incomplete. Every version is useful.

### When to break it

When partial data is actively misleading rather than merely incomplete. If a price index based on online retailers systematically under-represents the actual cost of living (because the cheapest goods aren't sold online), publishing it without strong caveats could lead to worse decisions than no data at all. The test: is the partial data directionally correct? Does it move in the same direction as the reality it's trying to measure, even if the level is imprecise? If yes, publish with caveats. If the partial data is systematically biased in a direction that would cause harm, fix the bias first or publish the caveat so prominently that it cannot be missed.

Also: when adding a data source would take only slightly more time but dramatically improve quality. If spending two more weeks to add a second corroborating data source to a single-source indicator would move it from "possibly misleading" to "directionally reliable," spend the two weeks. The principle is "partial is better than nothing," not "partial is better than slightly less partial in all cases."

---

## Principle 6: Transparency Over Authority

**Show your work. Credibility comes from methodology, not from institutional status.**

### Why it matters

econOS has no institutional authority. It is not the BCV. It is not DANE. It is not the IMF. It is an open-source project publishing economic data about countries where the official data is unreliable or absent. On what basis should anyone trust it?

The answer is: methodology. Every number econOS publishes is accompanied by a complete explanation of how it was produced. The data sources, the collection methods, the cleaning and normalization procedures, the aggregation algorithms, the weighting choices -- all of it is public. Any economist, data scientist, journalist, or curious citizen can trace a published number back to its inputs and evaluate whether the methodology is sound. This is how science works. It is how econOS works.

This approach inverts the traditional model of statistical authority. The BCV's numbers were trusted (when they were trusted) because the BCV is the central bank -- an institution with legal authority and historical credibility. When the institution failed, the credibility collapsed. There was nothing underneath it. econOS builds credibility from the ground up: the methodology is sound, the data sources are documented, the outputs are reproducible, and anyone can verify this for themselves. The credibility doesn't depend on who econOS is. It depends on what econOS does and whether that work holds up to scrutiny.

In a country where official institutions weaponized data -- publishing politically convenient numbers, suppressing inconvenient ones, and eventually going silent altogether -- the only path to trust is radical transparency. Not "trust us, we're experts." Instead: "here's exactly what we did, here's every assumption, here's where we're uncertain, here's the raw data -- check our work."

### What it means in practice

- Every composite metric is decomposable. If the dashboard shows "Economic Activity Index: +3.2% this month," the user can click through to see: this is composed of Pago Movil transaction growth (weighted 40%), nighttime light intensity change (weighted 30%), and job posting growth (weighted 30%). Each component links to its own data source and methodology page.
- Weights are published and justified. Why 40/30/30 and not 33/33/33? The methodology page explains: Pago Movil volume has the highest correlation with DANE-reported GDP in Colombia (the validation benchmark), nighttime lights have the broadest geographic coverage, and job postings capture labor market dynamics that the other two miss. Users who disagree with the weights can see the underlying components and weight them differently.
- Version history of methodology changes is maintained. If the weighting changes from 40/30/30 to 50/25/25 based on new validation data, the change is documented with the rationale. Historical data is available under both the old and new methodology so users can assess the impact of the change.
- Known limitations are stated prominently, not buried in footnotes. The dashboard doesn't just show a number -- it shows the number AND the uncertainty AND the coverage gaps. This is not a weakness. It is the core feature. An institution that says "we don't know" when it doesn't know is more credible than one that projects false certainty.
- Third-party validation is actively sought. Where possible, econOS cross-validates against independent sources. In Colombia, DANE provides a benchmark: do econOS's real-time estimates converge to DANE's official numbers when the official numbers eventually arrive? If yes, this builds credibility. If not, the divergence is investigated and reported.

### The tradeoff it resolves

**Transparency vs. simplicity.** Most users do not want to read a methodology paper. They want to see a number and trust it. Full transparency can overwhelm non-technical users and make the dashboard feel academic rather than practical. The resolution: progressive disclosure. The dashboard shows the number. One click reveals the components. Another click reveals the methodology. The raw data and technical documentation are available for those who want them. The default experience is simple. The depth is there for those who need it.

**Transparency vs. perceived credibility.** Paradoxically, showing uncertainty can reduce perceived credibility in some audiences. "We think inflation is between 6% and 12%" sounds less authoritative than "inflation is 9%." Some users will prefer the false precision. The resolution: econOS chooses honesty over the appearance of authority, every time. The users who learn to trust wide confidence intervals are better-informed decision makers than those who trust false precision. Over time, this builds deeper credibility than the alternative, because econOS is never wrong in a way it didn't warn about.

### When to break it

When transparency would compromise the safety of contributors or data sources. If publishing the specific methodology for collecting data from a particular source would allow a hostile government to block that source, operational security takes precedence over methodological transparency. The general approach can be described ("web-scraped retail prices") without revealing the specific operational details that would enable suppression.

Also: when explaining methodology to a general audience, some simplification is necessary and appropriate. The full mathematical specification of a nowcasting model belongs in a technical paper, not on the dashboard help page. The dashboard can say "we combine price data from online retailers with exchange rate data to estimate current purchasing power" without deriving the statistical model. The simplification must be honest -- it should not misrepresent the methodology -- but it can omit technical detail that would obscure rather than illuminate.

---

## Principle 7: Redundancy Over Dependence

**Never rely on a single data source. Platform risk and political risk are existential -- design for both.**

### Why it matters

Every data source econOS uses can disappear. MercadoLibre can change its website structure or block scrapers. Binance can exit the Venezuelan market or restrict API access. The BCV can stop publishing monetary data again. A government can pressure a mobile payment provider to stop sharing aggregate data. A satellite data provider can change pricing. None of these are hypothetical -- every one of them has a precedent.

Venezuela taught the world what single points of failure look like in economic data. The BCV was THE source for macroeconomic statistics. When it failed, there was no backup. The economy went dark. econOS cannot replicate this architecture. If any single data source is removed, the system must continue functioning -- perhaps with reduced precision, perhaps with wider confidence intervals, but functioning.

This principle extends beyond data sources to infrastructure. If the project is hosted on a single cloud provider, that provider can be pressured or can fail. If the project depends on a single maintainer, that person can burn out or be threatened. If the project is legally domiciled in a single jurisdiction, it can be subjected to legal pressure. Redundancy is not about efficiency. It is about survival.

### What it means in practice

- Every key indicator is built from at least two independent data sources. The real-time price index doesn't rely solely on MercadoLibre. It combines MercadoLibre, pharmacy chains, supermarket catalogs, delivery app menus, and Instagram business listings. If one source goes dark, the index degrades gracefully rather than collapsing.
- Data source health is monitored and reported. The dashboard includes a "data source status" indicator: which sources are active, which are degraded, which are offline. If the price index is running on three sources instead of five, the user sees this and can calibrate their confidence accordingly.
- The exchange rate is tracked through multiple channels: Binance P2P, Monitor Dolar, DolarToday, and the BCV official rate. If Binance exits or restricts the Venezuelan market, alternatives exist.
- Code and data are mirrored across platforms. Not just GitHub -- if GitHub restricts access (as it has for users in sanctioned countries), the project must be available elsewhere. GitLab, self-hosted instances, and downloadable archives provide redundancy.
- The project can be maintained from anywhere. Contributors in Caracas, Bogota, Miami, Madrid, or Santiago can all participate. No physical presence in any specific location is required for the project to function. This is not just convenience -- it is political survival. A contributor who faces pressure in one jurisdiction can continue from another.
- Data pipelines are modular. Adding or removing a data source doesn't require rewriting the system. Each source has a defined interface, and the aggregation layer consumes whatever sources are available.

### The tradeoff it resolves

**Redundancy vs. efficiency.** Maintaining five scrapers for price data when one would suffice is more expensive in engineering time and compute resources. The resolution: the cost of redundancy is small (a few extra scrapers, a few extra API integrations). The cost of dependence is catastrophic (the entire indicator goes dark when a single source fails). In any cost-benefit analysis where the downside of failure is "no data for the Venezuelan public," redundancy wins.

**Redundancy vs. simplicity.** More data sources mean more complexity in the aggregation layer: reconciling conflicting signals, weighting sources by reliability, handling sources that update at different frequencies. The resolution: build the aggregation layer well once. The complexity is in the infrastructure, not in the user experience. The user sees one price index. The infrastructure maintains five inputs to that index. This complexity is justified and manageable.

### When to break it

When a data source is genuinely unique and irreplaceable. If Pago Movil aggregate transaction data becomes available through a BCV partnership, there may be no alternative source for domestic digital payment volumes in Venezuela. The principle doesn't say "never use unique sources" -- it says "never DEPEND on them." Use the unique source, but don't build an indicator that collapses without it. Design the indicator so it can fall back to proxies (Binance P2P volumes, satellite data, electricity consumption) if the primary source disappears. The fallback will be worse, but it will exist.

In the very early stages of the project, some indicators may launch with only one source because that's all that's available. This is acceptable as a starting condition, not as a permanent state. The roadmap should include a plan to add redundancy to every single-source indicator.

---

## Principle 8: Compound Over Heroic

**Small improvements that accumulate beat one-time breakthroughs. Build for compounding.**

### Why it matters

econOS is not going to launch one day and fix Venezuela's information problem. The information problem is the accumulated result of decades of institutional failure, and it will be repaired by the accumulated result of sustained, incremental improvement. A price tracker that covers 500 products in 3 cities in month one, 800 products in 5 cities in month three, and 2,000 products in 10 cities in month twelve has more impact than a project that spends twelve months trying to launch with 2,000 products in 10 cities and ships nothing until then.

The compound logic applies at every level:

- **Data quality compounds.** Each month of historical data makes the next month's estimates more accurate (better baselines, better seasonal adjustment, better anomaly detection). A price index that has been running for two years is dramatically more useful than one that launched yesterday, even if the methodology is identical, because it has history to contextualize the present.
- **Trust compounds.** Each month that econOS publishes data that turns out to be directionally correct, each time it flags uncertainty honestly, each time its estimates converge to official figures when those figures eventually arrive -- these build credibility that cannot be manufactured. Trust is a compound asset.
- **Coverage compounds.** Each new data source, each new city, each new indicator adds marginal value. But the marginal value is multiplicative, not additive, because cross-validation improves reliability across all indicators. Adding satellite data doesn't just add satellite insights -- it validates the price data, which validates the activity data, which improves confidence in the labor market data.
- **Community compounds.** Each contributor who improves a scraper, adds a data source, fixes a bug, or translates a methodology page makes the project more useful, which attracts more users, which attracts more contributors.

Venezuela's recovery itself is a compound process. The economy doesn't jump from contraction to prosperity. It grows 2-3% this year, then 3-4% next year, then the growth compounds. econOS supports this by making each round of allocation decisions slightly better informed than the last. The cumulative effect of millions of marginally better decisions, compounding over years, is the difference between a recovery that stalls and one that accelerates.

### What it means in practice

- Ship early and improve continuously. The first version of any indicator is a starting point, not a finished product. The development process is: launch, measure, learn, improve, repeat.
- Prioritize investments that pay dividends over time. A robust scraping framework that makes it easy to add new sources is worth more than a one-off deep scrape of a single source. A well-designed data schema that accommodates new indicators without restructuring is worth more than a fast hack for today's indicator.
- Maintain historical data religiously. Every data point collected is a future baseline. Never throw away historical data, even if the collection methodology was imperfect. Imperfect historical data with known limitations is valuable for trend analysis.
- Build automation for things that need to happen repeatedly. Manual data collection doesn't compound. Automated pipelines do. Every manual process is a candidate for automation, because automation runs forever while manual effort stops when the person stops.
- Document as you go. Documentation compounds: a well-documented methodology attracts contributors, who improve the methodology, which attracts more contributors. Undocumented code is a dead end.

### The tradeoff it resolves

**Compounding vs. ambition.** The temptation is always to build the grand vision now -- the comprehensive economic dashboard covering all indicators, all regions, all countries. The compound principle says: build the smallest useful thing, ship it, and start accumulating. The grand vision is achieved through accumulation, not through a single heroic effort. This is not lack of ambition. It is the only path to the ambitious outcome.

**Compounding vs. perfectionism.** Perfectionism is the enemy of compounding because it delays the start. Every day spent polishing before shipping is a day of compound growth lost. The first version doesn't need to be good. It needs to be correct enough to be useful and transparent enough to be trustworthy. Quality improves as a natural consequence of the compound process.

### When to break it

When the foundation is wrong. If the data schema is fundamentally flawed, incrementally building on it compounds the problem rather than the solution. Sometimes you need to stop, redesign the foundation, and restart. The test: is the current trajectory, if continued, converging toward the right outcome? If yes, keep compounding. If the trajectory is pointed in the wrong direction, a corrective discontinuity is better than compounding in the wrong direction.

Also: when an external opportunity requires a step change. If a major data provider offers partnership access that would transform the project's capabilities overnight, seize it. Compound growth is the default strategy, not a prohibition against strategic leaps when they present themselves.

---

## Principle 9: Measure What Matters to People, Not What's Easy to Measure

**Job quality over job count. Purchasing power over GDP. The indicators that matter are the ones people live.**

### Why it matters

Traditional economic statistics were designed for governments and central banks making macro policy. GDP growth, unemployment rate, CPI -- these are useful for deciding interest rates and fiscal policy. They are much less useful for a Venezuelan worker deciding whether to move to Bogota, a student deciding what to study, or a family deciding what to do with a $200 remittance.

The gap between what is measured and what matters is vast:

- **GDP** measures aggregate output. It tells you nothing about whether ordinary people's lives are improving. Venezuela's GDP could grow 5% while that growth accrues entirely to the oil sector and connected elites, leaving the majority no better off. What matters to people is purchasing power: what can I actually buy with my wages?
- **Unemployment rate** counts people who are looking for work and not finding it. It says nothing about the quality of the work that people DO find. In Venezuela and Colombia, where 40-60% of employment is informal, the unemployment rate misses most of the labor market entirely. What matters to people is: can I find work that pays enough to live on? Is the work stable? Does it use my skills?
- **CPI** measures a weighted average basket of goods. It says nothing about the prices of the specific things YOU buy. A family that spends 60% of income on food experiences food price inflation, not headline CPI. What matters to people is: what do the things I actually need cost this week?
- **Foreign direct investment** measures capital inflows. It says nothing about whether that capital reaches the neighborhoods and sectors where ordinary people work. What matters to people is: are businesses opening near me? Is my neighborhood recovering?

econOS is not building macro statistics for policymakers. It is building decision-support infrastructure for individuals. The indicators must reflect what individuals actually need to know, even when those indicators are harder to measure, harder to define, and harder to validate than their traditional counterparts.

### What it means in practice

- Track real purchasing power, not just prices. "A kilo of chicken costs X bolivares" is useful. "Your average monthly salary buys Y kilos of chicken, compared to Z kilos six months ago" is much more useful, because it connects price data to the allocation question that actually matters: am I getting ahead or falling behind?
- Track job quality indicators, not just job counts. Number of job postings is a signal. But so is: what percentage of postings include salary information? What's the median posted salary relative to cost of living? What percentage of postings are for formal vs. informal positions? What percentage offer benefits? These are harder to measure but more relevant to the worker making a career decision.
- Track geographic granularity that matches lived experience. National averages obscure the enormous regional variation in Venezuela and Colombia. Caracas and Maracaibo are different economies. Bogota and Cucuta are different economies. The data should be as local as the decisions people make.
- Track trends, not just levels. "Inflation is 8%" is less useful than "inflation was 12% three months ago and has fallen to 8%, with the decline driven by stable exchange rates and increased imports." People make allocation decisions based on trajectory, not snapshots.
- Be willing to build indicators that don't have clean official analogs. If the most useful thing for a Venezuelan migrant is "real-time cost-of-living-adjusted wage comparison between Caracas and Bogota for nurses," build that, even though no statistical agency publishes it. The constraint is what people need, not what statistical agencies traditionally produce.

### The tradeoff it resolves

**Relevance vs. measurability.** The easiest things to measure (posted prices, exchange rates, job posting counts) are not always the most relevant. The most relevant things (purchasing power, job quality, neighborhood economic trajectory, small business viability) are harder to measure. The resolution: start with measurable proxies and improve them. A rough estimate of purchasing power based on scraped prices and wages is better than a precise exchange rate that doesn't connect to anyone's lived experience. Invest methodology effort in making the relevant indicators more reliable, rather than making already-reliable but less relevant indicators more precise.

**Innovation vs. comparability.** Traditional statistics exist in a comparative framework -- you can compare CPI across countries because the methodology is (roughly) standardized. Novel indicators like "cost-of-living-adjusted wage comparison for nurses" don't have this standardization. The resolution: build novel indicators that serve users AND map them back to traditional frameworks where possible, so the data can be contextualized. Show both the novel indicator (what matters to you) and its relationship to traditional indicators (how this compares to official statistics).

### When to break it

When traditional indicators serve as essential validation benchmarks. DANE's CPI in Colombia is a traditional indicator, and econOS needs to validate against it. The Colombian CPI is not the most relevant indicator for a Colombian worker, but it is the benchmark that establishes whether econOS's methodology is reliable. Measure it, validate against it, and then go beyond it. Traditional indicators are the stepping stones, not the destination.

Also: when what people THINK matters and what ACTUALLY matters diverge. If users obsess over the dollar exchange rate but the economically important signal is the rate of dollarization in everyday transactions, econOS should track both -- the exchange rate because users want it, and the dollarization rate because it matters more for long-term allocation decisions. Serving what people ask for and providing what they need are both legitimate goals; they just occasionally require different indicators.

---

## How the Principles Interact

These nine principles form a coherent system. They reinforce each other in most cases and create productive tension in a few.

**The reinforcing relationships:**

- Allocation-first and translate-don't-prescribe are natural partners. If the goal is better allocation, and allocation decisions belong to the individual, then the system's job is to provide the information and let the individual decide. Prescription would mean the system is allocating, not the person.
- Open-by-default and transparency-over-authority are the same commitment applied at different levels. Openness is the structural principle (the code, data, and methodology are public). Transparency is the operational principle (every number shows its work).
- Partial-is-better-than-nothing and compound-over-heroic are the temporal dimension of the same insight. Ship the partial thing now (Principle 5), and improve it continuously (Principle 8). Together they produce a system that starts useful and gets better.
- Redundancy-over-dependence and open-by-default jointly address the Venezuela lesson. Openness prevents political capture. Redundancy prevents technical capture. Together they produce infrastructure that survives.
- Mobile-first-Spanish-first and measure-what-matters-to-people are both expressions of the same commitment: design for the actual user in their actual context, not for an abstract ideal user.

**The productive tensions:**

- Partial-is-better-than-nothing can conflict with transparency-over-authority when partial data published with insufficient caveats misleads. The resolution: publish partial data AND publish aggressive caveats. Both principles are served.
- Mobile-first can conflict with transparency-over-authority when full methodological transparency creates information overload on a small screen. The resolution: progressive disclosure. Simple on the surface, deep when you dig.
- Allocation-first can conflict with compound-over-heroic when building foundational infrastructure that doesn't immediately serve allocation. The resolution: foundational infrastructure is justified when it enables near-term allocation-improving features. Infrastructure for infrastructure's sake is not.
- Measure-what-matters can conflict with partial-is-better-than-nothing when the thing that matters is hard to measure and only a very rough proxy is available. The resolution: ship the rough proxy with clear labeling, and invest in improving it. A rough purchasing power estimate labeled "rough estimate -- see methodology" is better than a precise exchange rate that doesn't answer the question the user is actually asking.

---

## Using This Document

When making a design decision, run it against the principles:

1. **Does this help someone allocate resources better?** If not, deprioritize it.
2. **Is the output public?** If it can't be, justify why.
3. **Does it work on a phone in Maracaibo?** If not, redesign it.
4. **Does it show data without telling people what to do?** If it prescribes, pull back.
5. **Is it shipping now, or waiting for perfection?** If waiting, consider shipping what exists.
6. **Does it show its work?** If the methodology isn't visible, make it visible.
7. **Does it survive a data source going dark?** If not, add redundancy.
8. **Does it compound over time?** If it's a one-shot effort, consider whether a compounding alternative exists.
9. **Does it measure what people actually need to know?** If it measures what's easy instead, consider whether the harder measurement is worth the effort.

Not every decision will satisfy all nine principles. When principles conflict, the context determines which one governs. But the burden of proof is on the exception: if you're breaking a principle, articulate why, and make sure the reason is stronger than the principle.

These principles are not permanent. They will evolve as the project evolves. But they change through deliberate revision with documented rationale, not through silent drift. If experience shows a principle is wrong, change it explicitly and explain why. That's the compound process applied to the principles themselves.
