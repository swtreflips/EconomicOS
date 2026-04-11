# Consumer Spending and Retail: Constructing a Real-Time Spending Signal for Developing Economies

## A Synthesis Document

This document maps how modern data sources combine into a real-time consumer spending proxy for developing and emerging economies. It draws on the research already completed in `current-landscape/` and `modern-data-sources/` and presents the construction methodology for an indicator that does not currently exist.

---

## 1. What We're Trying to Measure

The target is total consumer spending -- broken down by category, frequency, geography, and currency denomination. In a crisis economy with dual-currency dynamics, this means tracking both local-currency-denominated spending (mobile payment systems, bank transfers, cash) and dollar-denominated spending (dollar-denominated payment platforms, cash USD, crypto-facilitated purchases). In a middle-income developing country with functional institutions, it means tracking local-currency-denominated spending across formal and informal channels, with particular attention to the rapidly growing mobile payment ecosystem.

No institution currently produces this measurement for most developing countries. Not their central banks. Not their national statistical agencies (which may publish monthly retail sales surveys, but with significant lag, limited scope, and no coverage of the informal economy). Not the IMF, not the World Bank, not any private data provider.

The absence is not a minor gap. It is the absence of one of the most fundamental signals in economics.

### Why This Matters for Allocation Decisions

econOS frames economic growth as an optimization problem. The central chain is: better information leads to better allocation decisions, which leads to less waste, higher productivity, and faster growth. Consumer spending data is the signal that feeds allocation decisions at every level of the economy.

**Individual allocation.** A household deciding how to allocate a monthly budget of $200 -- between food, transport, medicine, school supplies, and savings -- makes that decision better when they know the real price trajectory of each category. In a crisis economy where local-currency-denominated prices can shift 10-20% in a week and the effective price depends on which currency you hold, this information gap is not abstract. It determines whether the family can afford to eat protein this week. A real-time spending signal, disaggregated by category, gives households price visibility that currently requires hours of informal social-media monitoring or physical store visits.

**Business allocation.** A shop owner deciding what to stock, how to price, and whether to expand or contract is making allocation decisions that depend on knowing what consumers around them are spending on. In a functioning data environment, this information arrives through market research, industry reports, and POS analytics. In a crisis economy, it arrives through gossip, gut instinct, and whatever the owner observes at their own register. A real-time spending signal by category and geography gives every business in the economy a view of demand that currently only the largest firms can approximate.

**Investor allocation.** An investor evaluating whether retail in a recovering economy is growing -- and if so, which segments and which cities -- has almost nothing to work with. There are no comparable retail sales reports, no reliable consumer confidence surveys, no category-level spending data. The investor either doesn't invest (capital stays away entirely, prolonging the depression) or invests blind (capital goes to the wrong place, producing waste). A real-time spending signal unlocks capital allocation toward recovering sectors and regions.

**Remittance allocation.** Many crisis economies receive billions in annual remittances. A diaspora family sending $200 home every month needs to know: what does $200 actually buy right now in their home city? Has the real purchasing power of their remittance gone up or down since last month? Should they send more? Should they send it in local currency or dollars? Without a spending signal, these decisions are made by asking the recipient "how are things?" and getting an answer shaped more by pride and anxiety than by data.

**Policy allocation.** A government or NGO designing a social program needs to know where spending is weakest, which categories are under the most price pressure, and which regions are most distressed. In many crisis economies, this information does not exist in any systematic form. Programs are designed on political logic, anecdote, and multi-year-old survey data. A real-time spending signal would allow targeting that matches actual need.

The Hsieh and Klenow (2009) result bears repeating here: eliminating resource misallocation in developing countries could increase manufacturing productivity by 30-60%. Consumer spending data is the demand signal that sits upstream of all downstream allocation. When that signal is missing or distorted, every allocation decision in the economy degrades.

---

## 2. Available Data Sources for a Crisis Economy

A crisis economy's consumer spending landscape is typically fractured across multiple payment channels, often two or more currencies, and a massive informal economy. No single data source captures more than a fraction of total spending. The strategy is to map each source honestly -- what it captures, what it misses, its latency, accessibility, and bias -- and then, in Section 4, show how they combine.

### 2.1 Mobile Payment System Aggregate Volumes (Central Bank / Banking Regulator Data)

**What it captures.** In many developing countries, a dominant mobile payment system serves as the closest thing to a universal digital payment method. Major domestic banks connect to it. It is used for everything from buying coffee to paying rent. When a street vendor accepts a mobile payment, the transaction flows through the interbank system and is recorded. Aggregate mobile payment volumes -- total transaction count and total value, ideally disaggregated by bank, region, or transaction size band -- would be the single best proxy for formal local-currency-denominated consumer spending.

**What it misses.** All dollar-denominated transactions (dollar-denominated payment platforms, cash USD, crypto). All cash local-currency transactions (small purchases, rural commerce). All barter. All in-kind transfers. Mobile payment systems capture the formal, local-currency, digital economy -- which is substantial, but which is not the whole economy.

**Latency.** The underlying transactions settle in near real-time. The question is whether aggregate data is reported at all, and at what frequency. The central bank may have aggregate interbank transfer statistics, but publication is often irregular and the data is not available through any API or structured feed. Banking regulators collect banking statistics but public reporting may be sparse and delayed by months.

**Accessibility.** This is often the hardest access problem in the data stack. The central bank may not publish granular mobile payment data in usable form. Getting it would require either (a) a direct institutional partnership with one or more domestic banks, (b) access to central bank/regulator reporting that is currently not publicly available, or (c) a legislative or regulatory mandate for data transparency that does not currently exist. This is a significant barrier but not an absolute one -- the data exists inside the banking system; it is not destroyed, just inaccessible.

**Bias.** Skews toward the formal, banked population. Misses the poorest households (those relying on cash), misses the dollarized economy, and understates activity in rural areas with unreliable connectivity. Also biased by local-currency inflation: rising mobile payment transaction values may reflect price increases rather than real spending increases, requiring deflation by a reliable price index -- which itself is a challenge in a crisis economy.

### 2.2 P2P Exchange Platform Volume and Exchange Rates

**What it captures.** In many crisis economies, P2P exchange platforms serve as the de facto foreign exchange market. The local-currency/USDT trading pair captures two critical signals: (1) the real market exchange rate (which often diverges from the official central bank rate and is used by merchants to set prices), and (2) the volume of currency exchange activity, which proxies for the intensity of economic transactions between the local-currency and dollar economies. When P2P exchange volume spikes, it typically means more people are converting between currencies -- either because they received local-currency income and need dollars, or received dollars (remittances, exports) and need local currency for domestic spending.

**What it misses.** A P2P exchange platform is a currency exchange platform, not a spending platform. It captures the conversion between currencies, not the spending itself. A person who buys USDT on the platform and then spends those dollars at a store generates an exchange signal (the conversion) but no signal for the actual purchase. Also misses anyone who exchanges currency through informal brokers, physical cash exchange, or other platforms.

**Latency.** Near real-time. P2P trades are recorded as they execute. Exchange rates can be observed minute-by-minute. Volume data can be aggregated at daily frequency with no meaningful lag.

**Accessibility.** Moderate and improving. Major P2P platforms provide public APIs that include some trading data. Third-party aggregators provide supplementary data. Local-currency/USDT pairs on P2P platforms are trackable programmatically. Historical data is partially available but not comprehensively archived -- building an archive from the present forward is feasible.

**Bias.** Skews toward tech-literate, younger populations with smartphone access and at least minimal crypto familiarity. Does not represent the older, rural, or least-connected population. Volume is a proxy for exchange activity, not directly for spending -- high volume could mean high economic activity or high currency flight, and distinguishing the two requires corroborating signals. The P2P rate itself may have a small spread over the "true" parallel rate because of platform fees and counterparty risk.

### 2.3 Web-Scraped Prices from Online Retailers

**What it captures.** Product-level prices from online retailers and e-commerce platforms. The primary targets are dominant e-commerce marketplaces, pharmacy chains with online presence, supermarket chains with web presences, and any other retailers posting prices online. This data captures the retail price level and its rate of change -- the numerator in any spending calculation.

The Billion Prices Project already proved this works for crisis economies. MIT researchers scraped retailer websites daily and produced price indexes that tracked inflationary spirals when central banks had stopped publishing their own CPI. The methodology is established. What matters here is what price data tells us about spending specifically.

Price data becomes a spending input through the following logic: if we know the price of a basket of goods (from scraping) and we have a proxy for the volume of transactions (from mobile payment systems or other sources), we can estimate nominal spending. Even without volume data, price movements by category reveal the structure of spending pressure -- when food prices rise faster than other categories, food spending is under stress even if we cannot measure the exact volume.

**What it misses.** Online prices may not reflect physical-store prices, especially for goods where local supply conditions vary (produce, meat, dairy). During the crisis, online prices diverged significantly from physical-market prices due to availability differences and delivery premiums. Also misses entirely the informal market -- street vendors, open-air markets, and the vast informal street economy where prices are negotiated verbally and never posted online.

The dual-currency complexity applies here directly: some online retailers post prices in local currency, some in dollars, some in both. A scraping system must tag currency denomination for every price observation and convert using the contemporaneous parallel exchange rate, not the official central bank rate.

**Latency.** Daily or better. Prices posted online can be scraped once or multiple times per day. This is one of the fastest-available signals.

**Accessibility.** Good, with technical effort. Web scraping of publicly posted prices is technically straightforward, though it requires maintaining scrapers against website changes, handling anti-bot measures, and managing data quality (detecting promotional prices, out-of-stock items listed at stale prices, and regional price variation). The BPP proved this is feasible for crisis economies, though website stability is worse than in developed markets due to infrastructure limitations.

**Bias.** Severe urban, formal-retail, and middle-to-upper-income bias. Online retailers serve the segment of the population with internet access, delivery infrastructure, and purchasing power sufficient to buy from formal channels. The poorest consumers -- who buy from street markets, neighborhood shops, and informal vendors -- are invisible. The basket of goods available online is also biased toward packaged, branded products rather than the staples (loose rice, beans, cooking oil bought by weight) that constitute the bulk of low-income spending.

### 2.4 Delivery App Data

**What it captures.** Order volumes, average order values, category breakdowns (food, pharmacy, groceries, other), geographic distribution, and time-of-day patterns from food and goods delivery platforms operating in major cities. These platforms capture a specific slice of urban consumer spending: prepared food delivery, grocery delivery, and some pharmacy/convenience delivery.

**What it misses.** Everything outside the delivery app ecosystem -- which is the vast majority of consumer spending in crisis economies. Delivery apps serve primarily middle-to-upper-income urban consumers in a handful of major cities. Rural spending, low-income spending, non-food spending, and spending in cities without delivery coverage are entirely absent.

**Latency.** Real-time within the platform. Aggregated data could be available at daily frequency.

**Accessibility.** Difficult. Delivery apps do not publish transaction data. Access would require a data partnership, which is possible but requires negotiation and likely some form of value exchange (analytical services, promotional partnership, or payment). Some proxy data may be available through app download/usage statistics (e.g., SimilarWeb, Apptopia), but these are indirect and expensive.

**Bias.** Extreme income, age, and urban bias. Delivery app users are a thin slice of the population in any developing economy: young, urban, smartphone-equipped, with disposable income above survival level. This data source is useful as one signal among many but would be dangerously misleading if treated as representative of broad consumer spending.

### 2.5 Satellite Nighttime Lights and Commercial Activity Proxies

**What it captures.** Nighttime light intensity from satellite imagery (primarily the VIIRS Day/Night Band from the Suomi NPP and NOAA-20 satellites) serves as a proxy for economic activity. The underlying relationship is well-established in the development economics literature: areas with more commercial activity produce more nighttime light. Henderson, Storeygard, and Weil (2012) demonstrated that nighttime lights can proxy for GDP at the subnational level, particularly in countries with poor national accounts data -- which describes most crisis economies precisely.

For consumer spending specifically, nighttime lights capture the physical footprint of retail activity: lit storefronts, commercial districts, markets, and transportation corridors. A decline in nighttime light intensity in a neighborhood or city signals a decline in commercial activity. An increase signals recovery.

Beyond lights, commercial satellite imagery (Planet, Maxar) can capture parking lot occupancy at shopping centers, truck traffic at distribution centers, and construction activity -- all proxies for spending and economic health.

**What it misses.** Nighttime lights are a blunt proxy. They cannot distinguish between residential and commercial electricity use, cannot identify spending categories, cannot measure transaction values, and have limited temporal granularity (cloud cover, satellite revisit rates). They also cannot distinguish between a neighborhood that is lit because businesses are open and one that is lit because streetlights are on but the shops are closed.

**Latency.** Daily satellite passes, but usable data products (after cloud masking, calibration, and aggregation) are typically available at monthly frequency from standard sources (e.g., the VIIRS monthly composites from the Colorado School of Mines). Higher-frequency products are available from commercial providers at higher cost.

**Accessibility.** Good for standard products. VIIRS nighttime light data is freely available through the Earth Observation Group at the Colorado School of Mines and through NASA's LAADS DAAC. Historical archives go back to 2012 (VIIRS) and to the early 1990s (the older DMSP-OLS data). Commercial satellite imagery for parking lot analysis and similar proxies is available through providers like Planet and Orbital Insight but costs $10K-$100K+ per year depending on coverage.

**Bias.** Correlates with urbanization and electrification. Areas without reliable electricity (rural regions, neighborhoods with frequent blackouts) produce artificially low light signals regardless of economic activity. In crisis economies with degraded electrical infrastructure -- particularly those that have experienced nationwide blackouts and ongoing grid instability -- changes in nighttime light intensity can reflect power grid failures as much as economic activity changes. This must be controlled for, and power outage data (if available) becomes a necessary supplementary input.

### 2.6 Electricity Consumption Data

**What it captures.** Total electricity consumption, ideally disaggregated by sector (residential, commercial, industrial) and by region. Electricity consumption has been used as an economic activity proxy in countries with poor national accounts data -- the idea is simple: when the economy is more active, it uses more electricity.

For consumer spending specifically, commercial electricity consumption (retail stores, restaurants, shopping centers) proxies for the volume of retail activity. If commercial electricity consumption in a state is rising, it likely means more businesses are operating, more stores are open, and more spending is occurring.

**What it misses.** Electricity data is a volume proxy with no category or value information. It cannot tell you what people are spending on, how much they are spending, or in which currency. It also cannot distinguish between electricity used for productive activity and electricity used for non-economic purposes (air conditioning, lighting in abandoned buildings, grid losses).

**Latency.** Electricity data is typically available at monthly or quarterly frequency from utility operators. Real-time grid data exists but is operational rather than public.

**Accessibility.** Poor in crisis economies. State-owned electricity companies in crisis economies typically do not publish granular consumption data. Power grids in crisis may have ongoing reliability problems, which both complicate the data and reduce the incentive to publish it. Getting useful electricity data would require either a utility data partnership (often unlikely given the political environment) or proxy estimation from other sources (e.g., satellite-detected nighttime light as a reverse proxy for electricity availability). In middle-income developing countries, electricity market operators may publish dispatch data more openly.

**Bias.** In crisis economies with degraded electrical infrastructure, declining electricity consumption may reflect grid collapse rather than economic contraction. Regions with worse grid infrastructure will show artificially depressed consumption even if economic activity is recovering. Without controlling for outages and rationing, electricity data is uninterpretable.

### 2.7 Formal Retail Sales Reports (Business Associations)

**What it captures.** Intermittent reporting from national and sector-level business associations on retail conditions, sales trends, and sector health. Chambers of commerce, retail federations, and sector-specific associations (pharmacies, supermarkets, automotive dealers) occasionally publish surveys or press statements about retail conditions.

**What it misses.** These reports are qualitative or semi-quantitative at best. They do not produce regular, structured, category-level retail sales data comparable to the US Census Bureau's Monthly Retail Trade Survey or middle-income countries' national statistical agency retail surveys. They tend to capture the formal sector only and are subject to advocacy bias (industry associations typically frame conditions to support their policy preferences).

**Latency.** Irregular. Reports may come quarterly, annually, or in response to specific events. There is no fixed publication schedule.

**Accessibility.** Low-to-moderate. Some association statements are published in media. Systematic access to underlying data would require an organizational partnership.

**Bias.** Formal sector only. Represents registered, tax-paying businesses that belong to these associations -- a shrinking share of total retail in crisis economies as informality expands. Also biased toward larger, urban businesses that are more likely to be association members.

---

## 3. Available Data Sources for Middle-Income Developing Countries

Middle-income developing countries with functional institutions have materially better data environments than crisis economies, but significant gaps persist -- particularly in the informal economy and in real-time frequency.

### 3.1 Mobile Wallet and Digital Payment Platform Transaction Volumes

**What it captures.** In many developing countries, dominant mobile wallet platforms (often tied to major banks or telecom operators) together cover a substantial fraction of the digitally active population. Their transaction volumes proxy for urban digital consumer spending. Different platforms often serve different demographics: bank-affiliated wallets may skew younger and middle-class, while government-transfer-linked wallets skew toward lower-income segments and social program recipients. Combined, they provide a more representative picture than either alone.

Transaction data from these platforms, in aggregate form, would reveal: total digital P2P transfer volumes, merchant payment volumes, frequency patterns, and geographic distribution.

**What it misses.** Cash transactions -- which represent the majority of face-to-face retail transactions in most developing countries. Neighborhood corner shops, street food, informal transport, domestic labor, open-air markets, and the vast informal commercial sector operate predominantly in cash and are invisible to digital payment platforms.

**Latency.** Real-time within the platforms. The question is data accessibility, not latency.

**Accessibility.** Moderate. Major banks publish some aggregate data in quarterly earnings reports and investor presentations. Fintech platforms publicize user count milestones. Granular transaction data (by category, region, transaction size) would require a data partnership. Middle-income countries' institutional environments are generally more favorable to such partnerships than crisis economies -- there is an existing data culture in the financial sector, driven partly by central bank reporting requirements and partly by fintech competitive dynamics.

**Bias.** Urban, younger, and formally banked population. Despite platform growth, active digital payment usage still correlates with income, education, and urbanization. Rural areas, older populations, and the poorest households are underrepresented. Government-transfer-linked platforms partially correct for this, but even social program recipients may conduct the majority of their subsequent spending in cash after receiving the transfer.

### 3.2 Card Network Data

**What it captures.** National card acquirers/processors handle the vast majority of Visa and Mastercard debit and credit card transactions. Card data provides transaction counts, values, merchant category codes, and geographic distribution for formal, card-accepting retail.

In middle-income developing countries, card penetration has been growing rapidly but still lags developed markets. Card data covers a significant volume of formal consumer spending, concentrated in supermarkets, department stores, e-commerce, and chain retail.

**What it misses.** The majority of face-to-face retail transactions. Card acceptance is concentrated in formal, larger-scale retail. Neighborhood shops do not accept cards. Street vendors do not accept cards. Informal service providers do not accept cards. In countries where 70-80%+ of face-to-face transactions are cash, card data captures the top of the spending distribution, not the base.

**Latency.** Card networks have near real-time settlement data internally. Published aggregates from national card processors or financial supervisory authorities arrive with moderate lag (monthly to quarterly).

**Accessibility.** Moderate-to-good for aggregates. Financial supervisory authorities in many middle-income countries publish payment system statistics. Card processors publish some data through industry reports. Granular data (by merchant category, by region, by transaction size) would require a commercial data agreement or a regulatory mandate for open data.

**Bias.** Income bias -- card users are disproportionately higher-income, urban, and formally employed. This is the same bias that affects card data in the US, amplified by lower card penetration. Using card data alone as a spending proxy would systematically overweight formal retail and underweight the informal economy where the majority of consumers shop daily.

### 3.3 National Statistical Agency Monthly Retail Sales Survey

**What it captures.** National statistical agencies in middle-income developing countries conduct monthly surveys of retail establishments covering sales volumes (in local currency), disaggregated by sector (food and beverages, textiles, pharmaceuticals, automotive, etc.). This is the official retail sales indicator, directly comparable in concept to the US Census Bureau's Monthly Retail Trade Survey.

**What it misses.** By design, these surveys cover formal, registered retail establishments above a minimum size threshold. They exclude informal retail (neighborhood shops, street vendors, open-air markets), which constitutes a large share of actual consumer spending. They also lag: results are typically published approximately 45-60 days after the reference month, which is too slow for real-time spending estimation.

**Latency.** 45-60 days after the reference period. Acceptable for official statistics; too slow for the real-time indicator econOS aims to build. However, the official retail survey serves as a critical calibration benchmark -- the official number against which the real-time proxy can be cross-validated.

**Accessibility.** Good. National statistical agencies publish retail survey data through their websites with historical series available for download. This is typically one of the most accessible data sources in a developing country's economic data environment.

**Bias.** Formal, registered, above-threshold retail only. Excludes the informal economy, micro-enterprises, and street-level retail. The sector disaggregation is useful but coarser than what web-scraped price data can provide.

### 3.4 Delivery Platform Data

**What it captures.** In many middle-income developing countries, dominant delivery platforms cover food delivery, grocery delivery, pharmacy, and increasingly general retail. Platform data captures order volumes, average order values, category breakdowns, restaurant/store popularity, and geographic patterns for urban delivery spending.

**What it misses.** Same as crisis-economy delivery app data, amplified by scale: delivery platforms serve a specific urban, middle-to-upper-income demographic. They are a valuable signal for formal urban consumer spending in certain categories (restaurants, prepared food, groceries from chain stores), but they are not representative of total consumer spending.

**Latency.** Real-time within the platform.

**Accessibility.** Difficult without partnership. Delivery platforms do not publish transaction data publicly. Proxy data through app analytics providers (SimilarWeb, Apptopia for app downloads and engagement) provides indirect signals. A data partnership is the realistic path to useful granularity.

**Bias.** Extreme urban, income, and age bias. Somewhat broader penetration in middle-income countries due to larger middle classes and better digital infrastructure, but still not representative.

### 3.5 Web-Scraped Prices (Retailers)

**What it captures.** Product-level prices from online retailers, supermarkets, and e-commerce platforms. Targets include dominant regional e-commerce marketplaces, major supermarket chains with online platforms, and pharmacy chains. E-commerce penetration in middle-income developing countries is typically higher than in crisis economies, providing a broader scraping surface.

**What it misses.** Neighborhood shop prices, open-air market prices, and informal sector pricing. The street-level economy is priced through negotiation, not posted prices. The gap between formal retail prices and neighborhood shop prices can be meaningful, particularly for staples sold in smaller quantities at different per-unit prices.

**Latency.** Daily or better.

**Accessibility.** Good, with technical requirements for scraper maintenance, anti-bot handling, and data quality management. Retail websites in middle-income countries are generally more stable and better-maintained than in crisis economies.

**Bias.** Formal, chain retail bias. Overrepresents packaged, branded goods and underrepresents loose staples, produce, and locally produced items that dominate lower-income spending.

### 3.6 Bank Economic Research Reports

**What it captures.** Major banks in middle-income developing countries publish economic research reports that include aggregate indicators, consumer confidence assessments, and sectoral analysis. Active bank research units publish regular reports on economic conditions with data drawn from their internal transaction analytics. International banks with local presence (BBVA, HSBC, Santander, etc.) publish country-level economic forecasts and analysis.

These reports sometimes contain proprietary spending indicators derived from the banks' own transaction data -- analogous to how JPMorgan Chase Institute and Bank of America Institute publish spending analyses in the US. When available, these provide a processed, expert-interpreted view of consumer spending trends.

**What it misses.** These are synthesized reports, not raw data feeds. They are published at the discretion of the banks' research teams, at whatever frequency and granularity those teams choose. They are not substitutes for direct data access but rather supplementary expert interpretations.

**Latency.** Weekly to monthly for recurring publications. Some banks publish daily or weekly economic commentary during significant events.

**Accessibility.** Good for published reports (available on bank websites). The underlying proprietary data is not publicly accessible.

**Bias.** Reflects the bank's own customer base, which is not identical to the population. Also subject to institutional bias: bank economists may frame analysis in ways that support the institution's business interests or macroeconomic positioning.

### 3.7 Central Bank Payment System Statistics and Remittance Data

**What it captures.** Central banks in middle-income developing countries publish detailed payment system statistics (transaction volumes and values for cards, electronic transfers, checks, mobile payments) and periodic remittance data by source country and destination region. The payment system statistics provide an aggregate view of formal transaction activity across the economy. Remittance data captures major external income flows -- many developing countries receive billions in annual remittances.

**What it misses.** The same informal economy gap that affects all formal data sources. Remittance data captures formal channels but misses informal transfers (physical cash carried across borders, informal transfer networks).

**Latency.** Payment statistics are published with moderate lag (monthly to quarterly). Remittance data is quarterly with a 2-3 month lag.

**Accessibility.** Good. Central banks in middle-income developing countries generally have strong data publication programs and provide structured data access through their websites.

**Bias.** Formal economy only. The share of remittances flowing through formal versus informal channels varies by country, but the informal component is always non-trivial.

---

## 4. The Construction Methodology

This section describes how to combine the sources mapped above into an actual consumer spending indicator. The approach is layered: start with freely available data, add institutional data as access develops, and handle the structural problems (dual currency, informal economy, seasonal patterns) explicitly rather than ignoring them.

### 4.1 Layer 1: What Is Freely Available Today

The following data sources can be collected without any institutional partnership, data license, or government cooperation. This is the starting layer.

**P2P exchange platform local-currency/USDT rates and volumes.** Accessible via public APIs and third-party aggregators. Provides: daily (or intraday) parallel exchange rate for the local currency, daily volume of local-currency/USDT trades. The exchange rate is the conversion factor needed to aggregate local-currency and dollar spending into a common denominator. The volume is a proxy for the intensity of cross-currency economic activity.

**Web-scraped retail prices.** Publicly posted prices on e-commerce platforms and retailer websites. Provides: product-level price observations at daily frequency, covering hundreds to thousands of SKUs across food, pharmacy, household goods, and other categories. These prices, tracked over time, yield a real-time inflation signal by category -- the denominator needed to convert nominal spending into real spending.

**VIIRS nighttime light data.** Freely available from the Earth Observation Group. Provides: monthly composite images of nighttime light intensity, at approximately 750m resolution, with global coverage. Subnational aggregation (by state/department, by municipality, or by custom region) allows tracking relative changes in commercial activity across geography and time.

**National statistical agency published statistics (where available).** Monthly retail sales (~45-60 day lag), monthly CPI (5-10 business day lag), payment system statistics (variable lag), quarterly remittance data. Accessible through statistical agency and central bank websites in countries with functional institutions.

**Central bank payment statistics.** Published aggregate data on electronic transfer, card, and mobile payment transaction volumes and values.

**Remittance data.** World Bank annual bilateral remittance matrices. Central bank quarterly data for countries with strong publication programs. Platform-published corridor data (Wise transparency reports, where available).

With these sources alone, we can construct a preliminary composite indicator:

For **crisis economies**, the initial signal combines: (1) P2P exchange platform volume as a proxy for economic activity intensity, (2) the platform-derived parallel exchange rate as the local-currency/dollar conversion factor, (3) scraped prices as the inflation/deflation adjustment, and (4) nighttime lights as a geographic and temporal cross-check on activity levels.

For **middle-income developing countries**, the initial signal combines: (1) official retail sales data as the lagging benchmark, (2) scraped prices as the real-time inflation layer, (3) central bank payment system data as a transaction volume layer, (4) nighttime lights as the geographic cross-check.

This is a minimal viable indicator. It is not comprehensive. It misses the informal economy, it has severe biases, and it relies heavily on proxies rather than direct spending observation. But it produces something that does not currently exist: a structured, regularly updated, multi-source consumer spending signal for developing economies.

### 4.2 Layer 2: Institutional Data (As Access Develops)

As partnerships develop, additional data layers can be integrated:

**Mobile payment system aggregate volumes (crisis economies).** If a partnership with domestic banks or the central bank/banking regulator can be established, aggregate mobile payment transaction volumes become available. This is the single highest-value data addition for crisis economies -- it converts the indicator from a proxy-based estimate into a direct observation of formal local-currency spending.

**Digital wallet aggregate volumes (middle-income countries).** Partnership with major banks or fintech operators to access aggregate transaction data (volumes, values, categories, geographic distribution). This is the highest-value addition for middle-income countries, given the rapid growth of these platforms and their demographic breadth.

**Card network aggregates.** National card processor aggregate transaction data, ideally disaggregated by merchant category code and region.

**Delivery platform data.** Partnerships with major delivery platforms to access aggregate order data.

Each new data layer is integrated into the composite through a weighting scheme that reflects its coverage and reliability. The weights are not fixed -- they are updated as the coverage and quality of each source changes over time.

### 4.3 Handling the Dual-Currency Problem (Dollarizing Economies)

In crisis economies with substantial dollarization, the bimonetary economy is the single most distinctive measurement challenge. Consumer spending occurs in two currencies: local currency (through mobile payment systems, bank transfers, cash) and US dollars (through dollar-denominated payment platforms, cash USD, crypto-facilitated purchases, and increasingly through direct dollar-denominated transactions at formal retailers).

The construction methodology handles this through two parallel streams that are then aggregated:

**Local-currency stream.** All local-currency-denominated spending data (mobile payment volumes, local-currency-denominated scraped prices, central bank monetary aggregates if available). This stream is deflated using a local-currency price index constructed from scraped prices, and converted to a common unit (USD) using the P2P platform parallel exchange rate.

**Dollar stream.** All dollar-denominated spending data. This is the harder stream because dollar spending is less visible: dollar-denominated payment platform transactions may be invisible from the local side, cash dollar transactions are invisible to all digital systems, and dollar-denominated card transactions (where they exist) flow through US or international payment rails. The dollar stream is estimated rather than directly observed, using:
- Dollarization rate estimates (independent economic consultancies typically estimate 50-70% of transactions in major cities are dollar-denominated, declining in smaller cities and rural areas).
- Remittance volumes as a proxy for dollar inflows to households.
- P2P exchange platform volume as a proxy for the local-currency/dollar conversion flow.
- Scraped dollar-denominated prices from retailers that post in USD, providing the deflator for the dollar stream.

**Aggregation.** The two streams are combined using an estimated currency share that varies by city and over time. In heavily dollarized capital cities, a reasonable starting estimate is 60-65% dollar / 35-40% local currency. For smaller cities, the local-currency share is higher. For rural areas, dollar cash may dominate but data visibility is near zero.

The currency share is itself an important output of the indicator, not just an input. Tracking how the dollar/local-currency split evolves over time is a measure of monetary credibility and dollarization dynamics.

**Critical caveat.** The dual-currency aggregation introduces significant estimation uncertainty. The dollar stream is estimated from indirect proxies, and the currency share is itself an estimate. The indicator must report this uncertainty explicitly -- not as a footnote, but as a core feature. A spending estimate of "$X billion +/- 30% due to informal dollar economy uncertainty" is far more honest and useful than a false-precision point estimate.

### 4.4 Handling the Informal Economy Gap

In both crisis and middle-income developing economies, the informal economy represents 40-60% of total economic activity. No digital transaction data captures it directly. This is not a problem that can be solved by getting more data from existing digital platforms -- the informal economy is informal precisely because it does not flow through recorded channels.

The methodology handles this through a **coverage ratio** approach:

**Step 1: Estimate the digital capture rate.** Using all available data sources, estimate what share of total consumer spending is captured by the indicator. This requires anchoring to an external benchmark. Possible anchors:
- National accounts estimates of household final consumption expenditure (from central banks or statistical agencies), despite their own limitations.
- Independent university-conducted household survey data on spending patterns (common in crisis economies where official data is absent).
- National household budget survey data (in countries where statistical agencies conduct these regularly).
- Cross-country comparisons with similar economies where both formal and informal spending are better measured.

**Step 2: Estimate the scaling factor.** If the indicator's data sources capture an estimated X% of total spending, the scaling factor is 1/X. For example, if the digital/formal data sources capture an estimated 40% of consumer spending in a crisis economy, the total spending estimate is the measured amount divided by 0.40.

**Step 3: Acknowledge the uncertainty.** The scaling factor is the single largest source of uncertainty in the entire indicator. A scaling factor of 2.5x (40% capture rate) versus 2.0x (50% capture rate) changes the total spending estimate by 25%. This uncertainty must be reported. The indicator should publish both the "measured" spending (from data sources) and the "estimated total" spending (with the scaling factor applied and uncertainty bounds stated).

**Step 4: Update the coverage ratio over time.** As developing economies evolve -- as digital payment adoption grows, as formalization expands or contracts, as new data sources become available -- the coverage ratio changes. Periodic recalibration against survey data or national accounts is essential.

The informal economy gap is not a flaw in the indicator to be hidden. It is a structural feature of these economies to be measured and reported honestly.

### 4.5 Seasonal Adjustment Considerations

Consumer spending in developing economies has strong seasonal patterns that differ from the US or European patterns that standard seasonal adjustment methods are calibrated for.

**Common seasonality patterns in developing economies:**
- **Holiday spending spikes (December/January):** Dramatic spending increases driven by holiday consumption, year-end bonus payments (aguinaldo, prima, 13th-month pay), and concentrated remittance inflows from the diaspora. December spending may be 2-3x the monthly average.
- **Cultural festivals:** Carnival, Eid, Diwali, Lunar New Year, and other major cultural events create spending spikes on travel, entertainment, and food.
- **Back-to-school periods:** Spending on school supplies, uniforms, and fees. Less pronounced than in higher-income countries because school spending is a smaller absolute amount.
- **Remittance cycles:** Diaspora remittance patterns are influenced by pay cycles in host countries and by holidays in both origin and host countries. Major family-oriented holidays generate remittance spikes.
- **Pay-cycle effects:** In many developing countries, workers are paid biweekly or monthly. Spending concentrates in the days immediately following pay dates.
- **Mid-year bonuses:** Many developing countries mandate mid-year bonus payments (e.g., prima de servicios, aguinaldo). These create measurable spending surges.
- **Government-created spending events:** VAT-free shopping days, subsidy disbursements, and similar government-created events produce concentrated spending patterns visible in payment data.
- **Regional festivals:** Local festivals and fairs create localized spending spikes that national-level data may miss.

Standard X-13ARIMA-SEATS seasonal adjustment, used by the US Census Bureau and most statistical agencies, can handle these patterns if trained on sufficient historical data. The challenge is that crisis economies' economic structures may have changed dramatically -- from pre-crisis, through hyperinflation, through dollarization, into partial recovery -- so that historical seasonal patterns may not be stable. Seasonal adjustment for crisis economies should be applied cautiously, with short estimation windows that adapt to the current economic regime rather than assuming stationarity across regimes.

### 4.6 Cross-Validation: How Signals Corroborate or Contradict

No single data source is trustworthy in isolation. The real power of a multi-source indicator is cross-validation: when signals from different sources agree, confidence rises; when they disagree, investigation is warranted.

**Corroboration tests:**

*P2P exchange volume vs. nighttime lights.* If P2P trading volume for the local-currency/USDT pair is rising (suggesting increased economic activity driving currency conversion) and nighttime light intensity in major cities is also increasing, the two independent signals corroborate an activity increase. If P2P volume is rising but lights are flat, the volume increase may reflect currency flight (people converting local currency to dollars to hold, not to spend) rather than spending growth.

*Scraped prices vs. P2P exchange rate.* In a dollarized economy, local-currency-denominated retail prices move closely with the parallel exchange rate. If scraped prices are rising at 5% per week but the local currency is depreciating at 8% per week on P2P platforms, it suggests dollar-denominated prices are actually falling -- a deflationary signal in the real economy despite nominal inflation.

*Mobile payment volumes vs. official retail sales.* If digital payment volumes are accelerating but the lagging official retail sales survey shows flat growth, the explanation may be: (a) the digital economy is growing while the cash economy is flat, (b) the survey has not yet captured the upturn, or (c) the digital payment growth reflects price inflation rather than real volume growth.

*Remittance volumes vs. delivery app orders.* If remittance inflows spike (perhaps due to holiday season) and delivery app orders also spike with a short lag, this corroborates the hypothesis that remittances translate quickly into consumer spending. If remittances spike but spending does not follow, it may mean recipients are saving, paying down debt, or using remittances for non-consumption purposes (medical emergencies, emigration costs).

**Contradiction protocols.** When data sources disagree, the indicator should not silently average them. It should flag the contradiction and publish it. Contradictions are information. A spending indicator that says "our payment data suggests spending is up 8% but our nighttime light data suggests commercial activity is flat -- here is why these might diverge" is more useful than one that reports a blended 4% with false confidence.

---

## 5. What This Enables for Allocation

This section makes the econOS theory concrete. A real-time consumer spending signal, even an imperfect one, enables specific allocation decisions that are currently made blind.

### 5.1 A Business Deciding Whether to Open in a Neighborhood

An entrepreneur in a crisis economy considering opening a bakery in a neighborhood of the capital city currently has no systematic way to assess local spending intensity. They can walk the block, count pedestrians, ask other shop owners how business is. They cannot compare spending levels across neighborhoods, track how a neighborhood's spending has changed over the past six months, or see whether food spending specifically is growing or contracting.

With a spending indicator disaggregated by geography (even at the city or municipality level), the entrepreneur can compare locations quantitatively. Nighttime light data provides a physical activity proxy at the neighborhood level. Scraped prices for food in nearby areas provide the price context. If mobile payment data becomes available with geographic disaggregation, it provides a direct transaction density signal.

This is not about replacing the entrepreneur's judgment. It is about giving them data inputs that currently do not exist. The difference between opening a bakery in a neighborhood with rising food spending and opening in one with declining food spending is often the difference between survival and bankruptcy. In a capital-scarce economy, every business failure wastes resources that cannot be easily replaced.

### 5.2 A Diaspora Family Deciding How Much to Send Home

A member of the diaspora sends $200 per month to family back home. She wants to know:
- What does $200 buy right now in her family's city? (Requires: local prices for a representative basket, available through scraping.)
- Has the real purchasing power of $200 gone up or down since last month? (Requires: a local price index, available through scraping plus the exchange rate from P2P platforms.)
- Should she send more this month? (Requires: category-level price signals -- if food prices are spiking, the family needs more.)
- Is it better to send dollars or local currency? (Requires: the P2P platform rate compared to whatever rate her conversion service offers.)

Today, she gets this information by calling her mother and asking how things are. The spending indicator converts this from an emotional conversation into an informed decision. Across the millions-strong diasporas of crisis economies, millions of remittance decisions per month are being made with information this indicator could provide.

### 5.3 An Investor Evaluating Sector Recovery

A fund evaluating a recovering crisis economy needs to answer: is retail actually growing, or is it just nominal inflation making numbers look bigger? Which categories are growing? Is the growth concentrated in the capital or broad-based?

Today, this investor has almost nothing to work with. There are no public-equity-style retail sales reports. There are no consumer confidence indexes. There is scattered anecdotal reporting from business associations. The result is that most institutional capital remains completely absent from recovery economies -- not because the opportunity is not there, but because it cannot be assessed.

A spending indicator that shows real (inflation-adjusted) spending growth by category and geography, even at low resolution, provides the minimal information base for investment decisions. If the indicator shows food retail growing at 8% real across multiple cities, corroborated by nighttime light increases and P2P exchange volume growth, an investor has a basis for evaluating grocery-sector opportunities. Without the indicator, the investor has nothing.

The capital allocation implications compound: every dollar of investment that flows to a recovering sector because the data exists to identify it generates employment, tax revenue, and further spending. The indicator does not just measure recovery -- it accelerates it by enabling the capital allocation that recovery requires.

### 5.4 A Worker Negotiating Wages

A worker in a developing country's second-largest city is negotiating a salary increase. The official CPI says inflation was 9% last year. But her actual spending pattern -- heavy on food and transportation, light on recreation and education -- may have experienced effective inflation of 14% because food and transport prices rose faster than the headline average.

A category-level spending indicator allows this worker to see her effective inflation rate based on her actual spending profile, not the average basket. This is not a theoretical exercise: the difference between demanding a 9% raise and a 14% raise, backed by data, is the difference between losing purchasing power and maintaining it.

In a crisis economy, the stakes are higher. A worker paid in local currency needs to know the real-time inflation rate to know whether her current salary still covers basic needs or whether she needs to negotiate immediately. The spending indicator, combined with the price component, provides this signal.

### 5.5 A Policymaker Designing Social Programs

A policymaker designing a targeted cash transfer program needs to know: where is spending weakest? Which regions have the most severe purchasing-power erosion? Is the erosion concentrated in food, housing, or healthcare?

In middle-income developing countries, the statistical agency provides some of this at moderate resolution with significant lag. The spending indicator, by combining higher-frequency data sources (digital payments, scraped prices, nighttime lights), can provide a more current picture of geographic and category-level spending distress.

In crisis economies, where government social programs are both more desperately needed and more poorly targeted, a spending indicator that identifies the cities and categories under the most stress could -- if the political will existed -- dramatically improve targeting. Even in the absence of government adoption, NGOs and international organizations (which play major roles in humanitarian response) could use the indicator to allocate resources more effectively.

---

## 6. Limitations and Honest Uncertainty

This section is not a disclaimer to be skimmed. It is a core component of the indicator's credibility. An indicator that overstates its precision will be discredited the first time reality diverges from its estimates. An indicator that reports its uncertainty honestly builds the trust that sustains long-term use.

### 6.1 The Informal Economy Is the Dominant Reality, Not the Exception

In both crisis and middle-income developing economies, the informal economy accounts for 40-60% of economic activity. The spending indicator, in its initial form, directly observes only the formal, digital fraction. The scaling factor applied to estimate total spending from the observed fraction is the largest source of uncertainty in the entire system.

To state this concretely: if the indicator observes $X in formal digital spending and applies a scaling factor of 2.5x (assuming 40% capture), but the true capture rate is 30%, the total spending estimate is off by 33%. If the true capture rate is 50%, the estimate is off by 20% in the other direction.

This is not a small error band. It means that the indicator's total spending estimate could be off by 20-40% in absolute terms. The useful signal is not the absolute level but the rate of change: if measured spending grows 5% month-over-month across multiple independent sources, the probability that total spending (including informal) also grew is high, even if the exact magnitude is uncertain.

### 6.2 Dollar-Denominated Payment Platforms and Cash Dollars Are a Black Box

In dollarized crisis economies, the dollar economy that flows through dollar-denominated payment platforms (e.g., US-linked payment services used for domestic transactions) is genuinely unmeasurable from the local side. These transactions appear as domestic transfers in the platform's home country and carry no geographic or purpose information that could link them to local economic activity. Cash dollars circulating locally are equally invisible.

This means the indicator structurally undercounts the dollar economy. In border regions where cash dollar circulation is highest, and among higher-income households in the capital where dollar payment platforms are the primary payment method, the undercount is most severe. The indicator must state this explicitly and provide its estimate of the dollar economy gap, not paper over it.

### 6.3 Web-Scraped Prices Are Not Representative Prices

Online prices from e-commerce platforms and supermarket chains represent formal, middle-to-upper-tier retail. The prices actually paid by the poorest consumers in developing economies -- at neighborhood shops, open-air markets, and from street vendors -- may be systematically different. Sometimes neighborhood shop prices are higher (smaller package sizes with per-unit premiums). Sometimes they are lower (less overhead, informal sourcing). The relationship is not constant and varies by product category and location.

Using scraped prices as the deflator for the entire spending estimate introduces a bias whose direction and magnitude are uncertain. The indicator should report scraped prices for what they are -- formal retail prices -- and note the limitation explicitly.

### 6.4 Nighttime Lights Are a Blunt Instrument

Nighttime light data is a genuine proxy for commercial activity, validated in the academic literature. But it is a very coarse proxy. It cannot distinguish a neighborhood where businesses are thriving from one where streetlights are on but shops are closed. It cannot detect economic activity during the day. It is confounded by power grid reliability in crisis economies, where grid instability means that changes in light intensity may reflect infrastructure failure rather than economic change.

Nighttime lights should be treated as a corroborating signal, not a primary signal. When lights agree with other sources, confidence increases. When they disagree, the other sources should generally take precedence.

### 6.5 Historical Baseline Instability

Crisis economies may undergo such radical structural change -- from commodity-dependent to collapsed to dollarized to partially recovering -- that historical data offers limited guidance for calibrating current relationships. The relationship between P2P exchange volume and consumer spending in one year may be completely different from the relationship five years later because the economy itself is structurally different.

This means the indicator cannot rely on long historical backtests to validate its current methodology. It must be calibrated against contemporary cross-checks and updated frequently as the economy evolves. This is less a limitation than a design principle: the indicator must be adaptive, not static.

### 6.6 Political and Institutional Risk

In crisis economies, economic data is politically sensitive. Central banks have stopped publishing data precisely because the data was unflattering. An independent spending indicator that contradicts official narratives -- showing, for example, that spending is contracting while the government claims recovery -- could face political pushback, regulatory interference, or restricted access to data sources.

In middle-income developing countries, the risk is lower but not zero. An indicator that reveals geographic or demographic spending patterns could be used for commercial purposes that raise privacy concerns, or could embarrass policymakers by highlighting regional disparities.

These risks must be managed through transparency (publishing methodology openly), independence (not aligning with any political faction), and redundancy (not depending on any single data source that could be cut off).

### 6.7 Communicating Uncertainty Without Undermining Credibility

The hardest part of publishing an uncertain indicator is framing: too much uncertainty language and users dismiss it as useless; too little and users treat estimates as facts. The balance is:

- Always publish confidence intervals, not point estimates alone.
- Use clear language: "Our data sources directly capture an estimated 35-45% of consumer spending in this economy. The remainder is estimated from indirect proxies and historical relationships."
- Distinguish between what is observed and what is inferred: "Formal digital spending in the capital city rose 7% month-over-month (observed from N data sources). Total estimated spending including informal economy rose an estimated 5-9% (inferred using scaling factors with stated uncertainty)."
- Publish the methodology in full, including the assumptions behind every scaling factor and weight.
- When the indicator is wrong -- when a subsequent survey or national accounts release contradicts the real-time estimate -- publish the discrepancy and update the methodology. Being wrong and transparent builds more credibility than being wrong and silent.

---

## 7. Summary: The Construction Roadmap

**Phase 1 (Immediately feasible):**
- P2P exchange platform local-currency/USDT rate and volume collection (API, automated)
- Web scraping of online retailer prices in target countries (daily)
- VIIRS nighttime light data integration (monthly composites)
- National statistical agency published statistics integration (retail sales, CPI, payment statistics) where available
- Central bank payment system and remittance data integration
- Publication of a preliminary composite: "econOS Consumer Spending Signal" with explicit uncertainty bands

**Phase 2 (Requires partnerships):**
- Aggregate mobile payment volume data (bank or central bank partnership in crisis economies)
- Digital wallet aggregate transaction data (fintech/bank partnerships in middle-income countries)
- Card network aggregates from national card processors
- Delivery platform data from major platforms in each country
- Recalibration of coverage ratios and scaling factors with new data layers

**Phase 3 (Requires institutional maturity):**
- Category-level disaggregation (food, transportation, housing, healthcare, education)
- Geographic disaggregation (state/department level, then municipality level)
- Real-time publication at weekly or daily frequency
- Integration with price tracker (inflation-adjusted real spending)
- Integration with employment and migration indicators for a complete activity picture

Each phase builds on the previous one. The indicator becomes more precise and comprehensive over time, but the Phase 1 version -- despite its limitations -- already produces a signal that does not exist today. In an information environment where the baseline is near zero, an imperfect signal is transformatively better than no signal.

The goal is not to replicate the US Census Bureau's Monthly Retail Trade Survey or the BEA's Personal Consumption Expenditures measure. Those are products of a massive statistical infrastructure built over decades. The goal is to produce the consumer spending equivalent of what the Billion Prices Project produced for inflation: a real-time, independently produced, transparent signal that fills a void where official measurement has failed or does not exist.

That is the starting point. Everything that follows -- better data access, more sources, finer granularity, higher frequency -- improves on a foundation that itself represents a step change from the current state of knowledge about what people in developing and crisis economies are actually spending and on what.
