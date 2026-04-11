# Real-Time Price Level Tracking

## Why Prices Are the Most Fundamental Economic Signal

Friedrich Hayek's 1945 essay "The Use of Knowledge in Society" made an argument that has never been improved upon: the central problem of economics is not optimization of a known production function but the utilization of knowledge dispersed across millions of individuals. No single agent -- no planner, no firm, no algorithm -- possesses even a fraction of the information needed to coordinate a complex economy. Markets solve this problem through the price system. Prices encode information about relative scarcity into a single number that anyone can observe and respond to, without needing to understand the underlying conditions that produced that number.

A tin miner in Bolivia does not need to know that a semiconductor fab in Taiwan increased its demand for tin. He only needs to see that the price of tin rose. That price signal tells him to increase production. Simultaneously, it tells manufacturers to economize on tin, tells recyclers to recover more, and tells prospectors to look for new deposits. The coordination happens without any coordinator. The information transmits without anyone sending a message. This is what Hayek meant by the price system as a "marvel" -- not hyperbole, but a precise description of a decentralized information processing system that outperforms any centralized alternative.

Every allocation decision in an economy depends on prices:

- **What to produce**: A farmer choosing between corn and beans looks at relative prices. A factory deciding whether to manufacture basic goods or luxury items looks at relative prices. Get this signal wrong and productive resources flow to goods nobody wants.
- **What to buy**: A household allocating its budget between food, transportation, and housing responds to relative prices. When food prices rise, consumption shifts. When housing costs fall in one city versus another, migration incentives change.
- **What wages to accept**: A worker deciding whether a job offer is adequate must compare the wage to the cost of living. Without current price information, the worker cannot evaluate the real value of the wage.
- **Whether to save or spend**: Inflation expectations -- which are fundamentally expectations about future prices -- drive the decision to consume now or defer. In a hyperinflationary environment, rational behavior is to spend immediately because prices will be higher tomorrow. This collective rationality produces collective destruction.
- **Whether to hold local currency or dollars**: In dollarizing economies, the daily decision of whether to keep earnings in local currency or convert to dollars depends entirely on the expected trajectory of prices and the exchange rate. This is a price-dependent decision made by millions of people every day.
- **Whether to invest**: Capital allocation -- the engine of growth -- depends on expected returns, which depend on expected future prices of inputs and outputs. Opacity in the price system does not just slow investment; it stops it. Capital that cannot see does not move.

Price transparency is therefore the single highest-leverage information improvement that econOS can make. Not because prices are the only important signal, but because every other signal depends on prices. Labor market data is useful, but a wage number without a cost-of-living number is half an answer. Sectoral growth data is useful, but without knowing the price dynamics within the sector, you cannot distinguish real growth from nominal inflation. Remittance data is useful, but a remittance amount without knowing what it buys at the destination is just a number.

### Crisis Economies as the Definitive Case Study in Price Signal Destruction

The clearest modern demonstrations of what happens when the price system is systematically destroyed come from crisis economies -- countries that have experienced hyperinflation, currency collapse, and statistical blackouts. The destruction is rarely accidental. It is the cumulative result of policies that attack prices at every level:

**Price controls eliminate the signaling function.** Governments mandate maximum prices for hundreds of basic goods -- food, medicine, hygiene products, construction materials. When the controlled price is set below the cost of production, producers stop producing. When it is set below the market-clearing price, demand exceeds supply and shortages emerge. The price cannot rise to signal scarcity, so the scarcity expresses itself instead as empty shelves, multi-hour queues, and a black market where the same goods trade at multiples of the controlled price. The controlled price is a fiction. The black market price is the real price. But the black market price is opaque, variable, and sometimes punishable by law, so even the real price is degraded as an information signal.

**Currency controls destroy the exchange rate signal.** Governments maintain official exchange rates that overvalue the local currency by orders of magnitude relative to the parallel market rate. An importer with access to official-rate dollars can buy goods abroad at a fraction of the parallel-market cost and sell them domestically at enormous profit. This creates massive rents for the politically connected and massive distortion in every price that depends on imports -- which, in economies that import most consumer goods, means virtually every price. The "price" of an imported good becomes a function not of global markets or domestic demand but of which exchange rate the importer has access to.

**Statistical blackouts destroy the ability to measure what is happening.** When central banks stop publishing CPI data, governments eliminate the benchmark that would have quantified the damage. Workers cannot reference an inflation number in wage negotiations. Contracts cannot adjust to a published index. International organizations cannot calibrate their assistance. The information layer of the economy goes dark.

The result is extreme misallocation. Food rots at borders while people go hungry, because the price signals that would have directed distribution are broken. Factories sit idle while demand goes unmet, because controlled prices make production unprofitable. Capital flees or freezes, because no price signal is trustworthy. Economies have contracted by 50-75% in these scenarios -- collapses worse than the Great Depression, driven not by a lack of resources but by a catastrophic failure of the information system that coordinates resources.

Rebuilding the price information layer is not a nice-to-have for economic recovery. It is rebuilding the market itself. A market without visible, current prices is not a market. It is a guessing game.

---

## What a Real-Time Price Index Needs to Capture in a Crisis Economy

A price index for a crisis economy must contend with conditions that no standard methodology was designed for: dual-currency pricing, recent hyperinflation history, deep informality, geographic fragmentation, and weak institutional data. The categories below reflect what actually matters for households and economic agents in these environments, not what a textbook index would measure.

### Food Prices: The Basic Basket

Food dominates household budgets in crisis economies in a way that is difficult to appreciate from a developed-economy perspective. For lower-income families -- which, after a crisis, means the majority of the population -- food expenditure can consume 60-80% of income. The "basic food basket" (canasta básica, cesta básica, or equivalent) is the most politically visible and personally urgent price metric in these countries.

Independent labor or consumer organizations often publish monthly basic basket figures that are widely cited in local media and political debate. When these figures show the cost of a family's food basket running at multiples of the minimum wage, the gap between the official minimum wage and the actual cost of survival becomes one of the most politically charged statistics in the country.

The food categories that matter most, ranked by budget share and political sensitivity:

- **Proteins**: The most consumed local protein sources (chicken, eggs, beef, pork, cheese). Prices vary significantly by cut, quality, and source (domestic vs. imported).
- **Grains and starches**: Rice, pasta, local staple flours, beans, bread -- the caloric foundation of diets in developing economies.
- **Cooking oils and fats**: Soybean oil, corn oil, margarine. These are often among the most chronically scarce items during crises.
- **Dairy**: Milk (powdered milk is often more available than fresh in crisis economies), butter, yogurt.
- **Produce**: Tomatoes, onions, peppers, plantains, potatoes, root vegetables. Prices are highly seasonal and vary significantly by region.
- **Beverages**: Coffee, sugar, and other daily necessities.

The food basket must be tracked in both local currency and dollars in dollarizing economies, because the price a consumer pays depends on which currency they use and where they shop. A kilo of chicken at a large supermarket chain priced in dollars may differ from the same item at a street vendor or an open-air market priced in local currency at the day's exchange rate.

### Currency Dynamics: The Local Currency/USD Exchange Rate

In a dollarized or dollarizing economy, "the price" of anything is a function of two variables: the nominal price in whatever currency it is quoted in, and the exchange rate between that currency and the other currency in which the consumer might hold their money. A bag of rice that costs 50 units of local currency means something very different depending on the day's exchange rate.

The exchange rate is therefore not a separate data category from prices. It is a component of every price. For a worker paid in local currency, the dollar price of food is the local price divided by the exchange rate. For a family receiving dollar remittances, the local currency cost of rent is the dollar amount they need to convert. The exchange rate is the conversion factor that makes all other prices commensurable.

In many crisis economies, the de facto market exchange rate is set not by the central bank's official rate but by the rate on P2P exchange platforms (such as cryptocurrency P2P marketplaces for the local currency/USDT pair), supplemented by independent rate trackers and informal broker networks. Central banks may have narrowed the gap between official and parallel rates, but discrepancies still arise, and the P2P rate often remains the reference that merchants and consumers actually use for pricing decisions.

Tracking the exchange rate at high frequency -- ideally hourly, at minimum daily -- is a prerequisite for any meaningful price index in a dollarizing economy.

### Housing and Rent

Housing costs in crisis economies are among the most opaque price categories. Formal rental markets are often severely distorted by rent control laws that freeze rents at levels that become trivial during hyperinflation. This destroys the formal rental market: landlords withdraw properties rather than rent them under controlled conditions, and new construction for rental purposes collapses.

What emerges is a largely informal rental market where:

- Prices are negotiated privately, often in dollars
- Formal lease contracts may not reflect actual payment amounts
- Short-term and room rentals operate entirely outside any data system
- In capital cities, rental prices vary enormously by neighborhood -- from wealthier, heavily dollarized districts to lower-income popular sectors

Rental data is obtainable from online real estate platforms, but these platforms skew toward the formal, higher-end market. Informal rentals -- the type most lower-income residents actually deal with -- are largely invisible.

This is a known limitation. The price index should include whatever rental data is scrapeable from platforms, clearly labeled as "formal market, online-listed" rather than presented as representative of all housing costs.

### Transportation

Transportation pricing in crisis economies has its own distinctive distortions:

- **Gasoline**: Some crisis economies maintain fuel subsidies as a political commitment, creating two-tier pricing systems -- subsidized fuel at near-zero prices (often rationed or requiring government ID) and market-priced fuel available to anyone. This two-tier system itself is a price signal worth tracking.
- **Public transportation**: Bus fares, metro fares, and informal transportation (shared taxis, motorcycle taxis) are often regulated at artificially low levels, with actual costs supplemented by informal payments or simply by deteriorating service quality.
- **Private transportation / ride-hailing**: Ride-hailing apps provide market-rate pricing data for urban transportation.

### Services: Telecom, Utilities, Internet

- **Mobile phone service**: State-owned telecom (deeply subsidized, deteriorating) alongside private carriers (market-priced) creates dual pricing. The gap between state and private telecom pricing reflects the broader dual-pricing reality in crisis economies.
- **Electricity**: Often heavily subsidized, with price schedules that have not kept pace with costs. Blackouts and rationing are the "price" that consumers actually pay -- not in money but in deprivation.
- **Internet**: Service quality and pricing vary enormously. Satellite and private internet providers charge market rates in dollars; state telecom provides slow, unreliable service at subsidized local currency rates.
- **Water**: Intermittent supply in many areas. The "price" of water includes not just the utility bill but the cost of storage tanks, delivery trucks, and bottled water.

### The Dual-Price Reality

This is the structural feature that makes price measurement in dollarizing crisis economies fundamentally different from conventional CPI. Many goods and services have a local currency price AND a dollar price, and they do not move in lockstep.

A restaurant in the capital may post a menu with dollar prices. A customer paying in local currency pays the dollar price converted at the day's exchange rate (sometimes at the restaurant's own rate, which may differ from the market rate). The dollar price may remain stable for weeks while the local currency price fluctuates daily with the exchange rate. Or the dollar price may adjust independently -- rising due to input cost increases or falling due to competitive pressure -- while the exchange rate moves in the opposite direction.

This means the price index must track:

1. Dollar-denominated prices (for goods and services priced in USD)
2. Local currency-denominated prices (for goods and services priced in local currency)
3. The exchange rate (to convert between them)
4. The currency in which each price observation is denominated (metadata attached to every data point)

A single "inflation rate" for a dollarizing economy is an oversimplification. The system should report: dollar-denominated price changes, local currency-denominated price changes, and a blended rate weighted by the estimated currency composition of actual transactions. Research suggests that 60-70% of transactions in major cities of heavily dollarized economies are dollar-denominated, but this share varies by city, by income level, and over time.

---

## Construction Methodology for Crisis Economies

### Layer 1: Web Scraping of Online Retail

Web scraping is the backbone of the Billion Prices Project methodology and remains the most scalable approach to systematic price collection. The key sources in any crisis economy:

**Dominant regional e-commerce platforms**

Regional e-commerce platforms (e.g., MercadoLibre in Latin America, Jumia in Africa, Flipkart/others in South Asia) function as both marketplaces (third-party sellers) and retail platforms. For price tracking purposes, they offer several advantages:

- Broad category coverage: electronics, household goods, food and beverages, personal care, automotive, clothing, and more
- Structured data: product names, prices, seller location, shipping information are presented in consistent formats amenable to scraping
- Dual-currency listings: in dollarized economies, many sellers list prices in both local currency and dollars, providing direct observations of dollar-denominated pricing
- Historical listings: products remain listed for extended periods, allowing tracking of price changes over time
- Seller geography: seller location provides a rough geographic dimension to the data

Limitations: E-commerce prices reflect formal online commerce, which skews toward durable goods and electronics. Food and daily necessities are less well represented. Prices include platform fees and may not match in-store prices. During the worst of crises, e-commerce platforms may have limited inventory due to supply disruptions.

**Pharmacy chains with online presence**

Major pharmacy chains that maintain online catalogs provide structured price data for medicines (over-the-counter and prescription), personal care and hygiene products, baby products, and some food and household items. Their online prices are typically in local currency, with conversion to dollar-equivalent possible via the exchange rate.

**Supermarket chains with online presence**

Major supermarket chains that maintain websites or apps with price listings. Coverage and reliability varies. Some update prices regularly; others may display stale information. The scraping system must track price freshness (date of last change) and flag stale listings.

**Electronics and appliance retailers**

For the durable goods component: electronics retailers with online presence, e-commerce platform sellers specializing in electronics, and social media-based electronics sellers (a significant channel in informal digital commerce in developing economies).

**Scraping frequency and infrastructure**

For crisis economies, daily scraping is the minimum useful frequency. In periods of exchange rate volatility, prices can change multiple times per day, but daily collection captures the trend. The BPP demonstrated that daily frequency was feasible and informative for crisis economies.

The scraping infrastructure should be:

- Cloud-hosted (not dependent on local internet infrastructure, which may be unreliable)
- Resilient to website changes (sites in developing markets change layouts more frequently)
- Equipped with change detection to flag when a website's structure changes in ways that break the scraper
- Storing raw HTML alongside extracted data, to allow reprocessing if extraction logic is updated

### Layer 2: P2P Exchange Rate

The local currency/USDT rate on P2P exchange platforms is the de facto market exchange rate in many crisis economies. Tracking this rate is not optional -- it is a core component of the price index, because the local currency price of any dollar-denominated good is a function of this rate.

**How P2P exchange platforms work:**

P2P trading platforms allow individuals to post buy and sell orders for cryptocurrency (primarily USDT, the Tether stablecoin pegged to USD) in exchange for local currency. The typical flow:

1. A buyer wants USDT (to hold dollar-equivalent value or to send abroad)
2. A seller has USDT and wants local currency
3. They agree on a rate
4. The buyer transfers local currency via mobile payment to the seller
5. The platform releases the escrowed USDT to the buyer

The aggregate of these transactions produces a market-clearing exchange rate that reflects actual supply and demand for dollars. Unlike administratively set central bank official rates, the P2P rate is a genuine market price.

**Data collection approach:**

- Major P2P platforms provide public APIs that include advertisement data (buy/sell offers with prices, quantities, and payment methods)
- Third-party aggregators compile P2P trading data by country
- The system should collect: the median and volume-weighted average buy and sell rates, the bid-ask spread (which reflects market liquidity and uncertainty), total daily volume (which reflects the intensity of currency exchange activity), and the time series of intraday rate movements

**The central bank rate as a secondary reference:**

The central bank publishes a daily exchange rate that may have converged toward the parallel market rate. The system should track both rates and report the spread between them. When the spread is narrow, the official rate is functionally market-determined. When it widens, it signals renewed divergence between official policy and market reality. The spread itself is an economic signal -- a measure of monetary policy credibility.

**Other exchange rate sources:**

- Independent rate aggregators that compile rates from multiple informal sources
- Long-running parallel rate trackers
- Apps aggregating multiple exchange rate sources

Cross-referencing these sources provides a robustness check. If independent trackers, P2P platforms, and the central bank all report similar rates, there is a single effective exchange rate. If they diverge, the divergence itself must be analyzed and reported.

### Layer 3: Social Media and Informal Price Reporting

This layer is unique to crisis economies and is one of the most distinctive aspects of the econOS approach. In countries where official price data has collapsed, citizens have organically developed informal price-reporting networks that contain real-time, ground-level price observations that no formal data source captures.

**WhatsApp and Telegram price groups**

During economic crises, citizens have created city-level WhatsApp and Telegram groups dedicated to sharing prices. These groups -- with names referencing local cities, markets, and basic goods baskets -- function as crowdsourced price databases. Members post:

- Photos of price tags in supermarkets and pharmacies
- Screenshots of delivery app prices
- Text messages reporting the cost of the day's grocery run
- Exchange rate observations from local exchange houses
- Alerts about product availability and scarcity

These groups can have thousands of members and generate dozens to hundreds of price observations per day. The data is unstructured (photos, voice notes, text in informal local language, regional slang) but represents genuine, real-time price observations from actual consumers across geographic areas and income levels that formal e-commerce platforms do not reach.

Systematizing this data requires:

- **Image processing**: OCR (optical character recognition) applied to photos of price tags, receipts, and menus to extract product names and prices
- **Natural language processing**: Parsing text messages in informal local language to identify product names, quantities, prices, and currencies (people use shorthand for products and currency denominations that varies by country)
- **Geolocation inference**: Determining the city or neighborhood from group names, user profiles, or context clues in messages
- **Deduplication**: Multiple group members may report the same price from the same store; the system must identify and handle duplicates
- **Quality filtering**: Distinguishing genuine price observations from complaints, jokes, political commentary, and spam that inevitably appear in these groups

This is not a clean data source. It requires significant processing, and the resulting data will have higher noise and lower precision than web-scraped retail prices. But it captures a segment of the market -- informal vendors, neighborhood shops, open-air markets -- that no online platform reaches. For food prices specifically, where informal commerce is a major channel, this layer is essential.

**Instagram business accounts**

Many small businesses in developing economies, particularly food vendors, restaurants, and service providers, use Instagram as their primary online presence (rather than a website). They post prices directly in their stories, posts, or bio links. Restaurants post daily menus with prices. Bakeries post daily price lists. Home-based food businesses (a significant segment in informal economies) post prices for prepared meals, cakes, and snacks.

Instagram scraping is technically possible but subject to platform restrictions. An alternative is to build a voluntary reporting system where business owners opt in to share their prices through an econOS interface connected to their Instagram presence.

**Twitter/X price reporting accounts**

Several accounts and hashtags on Twitter/X track prices in crisis economies:

- Individual economists and journalists who post weekly or monthly cost updates
- Independent consumer organization reports shared via social media
- Hashtags related to basic basket costs and local prices used by consumers reporting prices
- Bot accounts that automatically post exchange rate updates

These are lower-volume than WhatsApp groups but have the advantage of being public and scrapeable via the Twitter/X API (subject to API access terms and costs).

### Layer 4: Delivery App Data

Delivery apps provide structured, real-time price data for food, groceries, and restaurant meals -- categories that are among the most important for the price index.

In any given developing economy, one or more delivery apps will dominate the market. These apps typically cover:

- Restaurant delivery: menu prices for thousands of restaurants, updated by the restaurants themselves
- Grocery delivery: prices for supermarket and local store products
- Pharmacy delivery: medicine and personal care prices

Delivery app prices are often in dollars in dollarized economies, reflecting the currency reality. The structured nature of the data (product name, price, restaurant/store, category) makes it directly usable for price tracking.

**Delivery app advantages:**

- Prices are structured and machine-readable
- Products are categorized consistently
- Prices update frequently (restaurants adjust prices in real time)
- Geographic coverage is tied to delivery zones, providing city-level data
- Both dollar and local currency pricing may be visible

**Delivery app limitations:**

- Coverage is primarily urban, concentrated in major cities
- Delivery app prices may include markups over in-store prices
- Restaurant prices on apps may differ from dine-in prices
- Product selection is curated by the app, not representative of all available goods

### Layer 5: Formal Retail and Institutional Reporting

**Business associations and chambers of commerce**

Business federations and their member chambers occasionally publish price surveys and economic reports. These are irregular but, when available, provide a business-community perspective on price trends.

**Independent labor and consumer organizations**

Independent organizations that publish basic basket costs serve as widely cited benchmarks. Their methodology involves direct price collection in local markets. Monthly figures serve as benchmarks against which the higher-frequency econOS index can be validated.

**Central bank published data**

When the central bank publishes CPI or inflation data, it should be incorporated into the system -- not as ground truth (given potential credibility issues) but as one data point to compare against independent measurements. Divergence between the official figure and the independently constructed index is itself informative.

### Layer 6: Cross-Validation

The multi-source approach is not just about coverage. It is about robustness. Each data layer has different biases:

- Web-scraped retail prices skew toward formal commerce and durable goods
- P2P exchange rates reflect the financial/exchange market, not necessarily small-transaction rates
- Social media prices skew toward food and daily necessities, with geographic and demographic biases depending on who participates in which groups
- Delivery app prices skew urban and include platform markups
- Formal reporting has institutional biases and lags

Where multiple sources agree, confidence is high. Where they diverge, the divergence itself is diagnostic:

- If online retail food prices rise but social media reports stable street prices, it may indicate a wedge between formal and informal channels
- If the P2P exchange rate moves sharply but delivery app dollar prices don't adjust, it suggests short-term exchange rate volatility that hasn't propagated to goods prices yet
- If formal institutional reports show low inflation but all independent sources show higher inflation, the institutional credibility problem has resurfaced

The cross-validation methodology should be systematic: for each product category, compare at least two independent sources where possible, report the mean and the range, and flag categories where only a single source is available.

---

## Construction Methodology for Middle-Income Developing Countries

Middle-income developing countries with functional statistical agencies present a fundamentally different challenge. The statistical infrastructure works. The national CPI is credible, comprehensive (dozens of cities, hundreds of items, millions of price quotes per month), and timely (released within days of the reference month). The question is not "can we build something where nothing exists?" but "can we add enough value to justify the effort?"

The answer is yes, for specific use cases:

### Higher Frequency

National CPI is monthly. For businesses adjusting prices weekly, for workers negotiating wages, for the central bank monitoring the impact of monetary policy decisions, and for border-region dynamics where migration and trade create rapid price changes, weekly or daily price signals add meaningful information.

Web scraping of online retail provides this higher frequency:

- **Dominant e-commerce platforms**: The largest e-commerce platforms in each country provide extensive product listings across all major categories.
- **Major retail chains**: Large supermarket and department store chains with mature e-commerce platforms offer comprehensive grocery, household, electronics, and general merchandise catalogs. Online prices generally match in-store prices, making these high-quality sources.
- **Delivery super-apps**: The dominant delivery apps covering groceries, restaurants, pharmacies, and general retail in all major cities. Their structured product catalogs with real-time pricing make them excellent high-frequency data sources, particularly for food prices.
- **Online grocery delivery services**: Dedicated online grocery delivery services operating in major cities provide direct grocery price data.

### Informal Commerce Prices

National statistical agencies' price collection focuses on formal retail establishments. In many developing countries, neighborhood corner stores (estimated in the hundreds of thousands) and open-air markets serve a large share of lower-income consumers, and their prices may diverge from formal retail. Capturing these prices through delivery apps that serve neighborhood stores and through social media price reporting would supplement formal statistical coverage.

### Rental Market Data

Countries with well-developed online real estate platforms offer rental listing data including price, location, property characteristics, and listing date. Scraping rental listings provides a real-time indicator of market rents, compared to the official CPI shelter component which captures existing lease rates with a lag similar to the US CPI shelter lag problem.

The rental data opportunity mirrors the US shelter lag problem documented in the inflation measurement document: national CPI captures the rent on all existing leases, which is a lagging indicator of market conditions. A real-time index of new listing prices on major real estate platforms would provide a leading indicator, particularly valuable in cities experiencing rapid change (gentrifying neighborhoods, areas adjusting to migration inflows, cities responding to digital nomad demand).

### National Statistical Agency as Validation Benchmark

The most important structural advantage for middle-income countries is that a credible national CPI exists. This allows rigorous validation:

- Build the web-scraped daily index
- Compare it monthly against the official CPI
- Where they track closely (which, based on BPP experience in countries with credible statistical agencies, should be most of the time), the daily index is validated
- Where they diverge, investigate whether the divergence reflects a genuine information gain (the daily index capturing an event before the monthly average picks it up) or a data quality issue in the scraped data
- This validation builds the credibility needed to trust the crisis economy index, which has no comparable benchmark

Middle-income countries with functional statistics are the "easy case" -- methodologically, building and validating the daily price index here first, then applying the validated methodology to crisis economies' harder environment, is the right sequencing strategy.

### The Cross-Border Bridge

Many crisis economies share borders, languages, and massive migration flows with neighboring middle-income countries. Border cities often function as single economic zones in practice.

A price index that covers both countries simultaneously enables:

- **Purchasing power parity comparison**: What does $100 buy in the crisis economy's capital versus the neighboring country's capital versus border cities? For millions of people deciding whether to migrate, return, or stay, this is decision-critical information.
- **Cross-border arbitrage detection**: When the price of a basic good is significantly cheaper on one side of the border, trade flows respond. Tracking the price differential identifies these arbitrage opportunities and, more importantly, measures the economic integration of the two markets.
- **Remittance purchasing power**: A migrant in the neighboring country sending money home can see exactly what their dollars will buy in their family's city, compared to what those same dollars would buy locally.

---

## The Billion Prices Project Model: What Worked, What Didn't, and How econOS Adapts

The Billion Prices Project, founded by Alberto Cavallo and Roberto Rigobon at MIT in 2008, is the most directly relevant prior art. Understanding what they did -- and where the approach's limits were -- is essential.

### What They Did

The BPP collected daily prices from online retailers in over 60 countries using automated web scrapers. For each country, they identified major retailers with online catalogs, built scrapers to extract individual product prices daily, and aggregated the resulting data into daily price indexes.

The aggregation used standard index number techniques: products were classified into categories approximating the composition of official CPI baskets, and category-level price changes were weighted to produce an overall index. This allowed direct comparison with official CPI.

The BPP was commercialized through PriceStats (later acquired by State Street Global Markets), which sold daily inflation indicators to institutional clients -- central banks, sovereign wealth funds, hedge funds.

### What Worked

1. **The basic methodology was validated globally.** In countries with credible statistical agencies (US, UK, Brazil, Germany), the BPP daily index tracked the goods component of official CPI with correlations above 0.9. This established that online prices are a reliable proxy for the broader goods price level.

2. **It detected statistical manipulation.** In Argentina, where the INDEC was widely accused of suppressing inflation numbers, the BPP index showed inflation running 2-3x the official rate, consistent with private estimates. This demonstrated the methodology's value as an independent check on government statistics.

3. **It covered crisis economies during hyperinflation.** The BPP/PriceStats collected data from online retailers in crisis economies and produced daily indexes during hyperinflationary periods. Their data showed:
   - Confirmation of hyperinflationary dynamics, with price changes accelerating in line with exchange rate depreciation
   - Strong correlation between online prices and the parallel exchange rate, validating PPP-based approaches
   - Goods-level price dynamics invisible to monthly or quarterly reporting -- synchronized price jumps, rapid pass-through of exchange rate movements, intraday volatility

4. **It scaled.** The BPP eventually covered 60+ countries with a relatively small team, proving that the marginal cost of adding a new country is low once the infrastructure exists.

### What Didn't Work (or Worked Imperfectly)

1. **Services are invisible to web scraping.** The BPP methodology captures goods prices -- things you can buy online and have shipped. It does not capture services: haircuts, medical consultations, auto repair, legal services, domestic labor, tutoring. Services represent 60-70% of developed-economy spending (lower in crisis economies, but still significant). This means a web-scraped index is structurally a goods price index, not a full cost-of-living index.

2. **Online prices may not match offline prices.** The BPP's validation against official CPI was strong for goods, but the underlying assumption -- that online prices track offline prices -- holds best in markets with mature e-commerce where online and offline prices are arbitraged. In crisis economies where online shopping is limited, the representativeness of online prices for the broader market is lower.

3. **Scarcity is not captured by prices.** In crisis economies, the relevant economic signal is often not the price of a good but whether the good exists at all. Empty shelves, rationed products, and multi-hour queues impose real costs on consumers that no price index captures. A good listed at a "low" controlled price that cannot actually be purchased is a meaningless data point. The BPP, like any price index, measured the prices of goods that were available for purchase, not the full cost of living in an economy with chronic shortages.

4. **It was proprietary.** PriceStats served institutional clients at institutional prices. The populations who most needed the data -- families in crisis economies, small business owners, workers negotiating wages -- could not access it. The academic papers published aggregate findings, but the underlying daily data was not public.

5. **Limited geographic granularity.** The BPP produced country-level indexes but not city-level or regional indexes. In countries where capital city prices differ significantly from secondary cities, border towns, or rural areas, national-level data is an incomplete picture.

### How econOS Adapts the BPP Approach

econOS takes the BPP's validated core methodology and extends it in four critical directions:

**More data sources.** The BPP relied almost exclusively on traditional e-commerce retailers. econOS adds delivery apps, social media price observations (WhatsApp groups, Instagram, Twitter/X), exchange rate platforms (P2P exchanges, independent rate trackers), and formal institutional reporting. This dramatically broadens coverage, especially for food, services, and informal commerce.

**Dual-currency tracking.** The BPP tracked prices in local currency. econOS must track in both local currency and dollars, record the denomination of each price observation, and maintain the exchange rate time series needed to express all prices in a common unit.

**Geographic granularity.** Instead of a single national index, econOS targets city-level indexes for major cities in both crisis and middle-income economies. Delivery app data and geotagged social media observations enable this disaggregation.

**Public access.** This is the fundamental difference. The BPP was commercialized as an institutional product. econOS publishes everything: the raw data, the methodology, the index values, and the API. The target users are not hedge funds but the nurse deciding whether to emigrate, the small business owner setting prices for the week, and the diaspora family evaluating what their remittance will buy.

---

## Handling the Hard Problems

### Quality Adjustment

When the price of a product changes, is it inflation or is it a different product? This is the classic quality adjustment problem in price measurement, and it is harder in developing markets.

Examples:

- A brand of rice that was sold in 1kg bags now comes in 900g bags at the same price. The "price per kg" has risen, but the sticker price hasn't changed. This is shrinkflation.
- A supermarket stops carrying a cheaper brand of cooking oil and replaces it with a more expensive brand. The "price of cooking oil" in the index rises, but it reflects a change in the available product, not a pure price increase.
- A smartphone listed at $200 this year has better specifications than the $200 smartphone listed last year. The sticker price is unchanged, but the quality-adjusted price has fallen.

The BLS handles these through "hedonic quality adjustment" -- statistical models that estimate the value of individual product characteristics. This is resource-intensive and not feasible for econOS at scale.

The pragmatic approach for econOS:

- **Match exact products where possible.** Track specific SKUs, not generic product categories. When the same branded product changes price, that is a clean price observation.
- **Flag product changes.** When a tracked product disappears and is replaced by a similar product, flag the substitution. Report both the raw index (which includes the substitution effect) and a "matched-product" sub-index (which only includes price changes for products that remain identical).
- **Track unit prices.** Where quantity information is available (which it often is on e-commerce platforms), report price per kilogram, price per liter, etc. This automatically catches shrinkflation.
- **Accept imperfection.** Quality adjustment is an unsolved problem even in the BLS, with its $600 million annual budget. A transparent methodology that acknowledges its limitations is more valuable than a black-box adjustment that claims false precision.

### Representativeness

Online prices may not match street prices. Delivery app prices include markups. WhatsApp group prices are reported by a self-selected sample. No single source is representative of the full price experience in a developing economy.

The mitigation strategy is multi-source triangulation:

- If online retail, delivery app, and social media sources all show chicken at $4-5 per kilo, the price is likely in that range regardless of channel
- If online retail shows $5 but social media reports $3.50 at the open-air market, the difference itself is informative -- it reveals the formal/informal price gap
- Report ranges and confidence intervals, not false precision. "Chicken: $4.00-5.00/kg (formal retail); $3.00-4.00/kg (informal market reports)" is more honest and more useful than "$4.37/kg"

### The Shelter Problem

Rental data in crisis economies is extraordinarily opaque. Rent control has distorted the formal market, the informal market operates through private negotiation, and online listings skew toward the higher-end formal market.

Honest approach:

- Scrape online rental and real estate platforms and report formal market asking rents
- Clearly label this as "online-listed formal rental asking prices," not as representative of all housing costs
- Track over time: trends in formal market rents still provide useful information about direction and magnitude of shelter cost changes, even if the level may not match the median resident's actual housing cost
- In middle-income countries, the same approach applies with major real estate platforms, validated against the official CPI shelter component

This is a known gap. It should be documented, not hidden.

### Shrinkflation

Package size reduction at constant nominal prices is a global phenomenon but is particularly prevalent in economies with price sensitivity and informal price controls. Tracking it requires:

- Recording package sizes alongside prices (which e-commerce platforms usually provide)
- Computing per-unit prices (price per kg, per liter, per unit)
- Flagging instances where the same brand/product reduces package size
- Reporting a "shrinkflation index" -- the percentage of tracked products that have reduced package sizes over a given period

### Geographic Variation

Prices in a country's capital are not prices in its second city. Prices in major cities are not prices in border towns or rural areas.

The sources of geographic price variation include:

- **Transportation costs**: Getting goods from ports to inland cities adds cost that varies with distance, road quality, and fuel availability
- **Local supply conditions**: Agricultural production varies by region; prices differ between producing regions and purely import-dependent cities
- **Dollarization levels**: Border regions and resource-producing regions may be more dollarized than central areas, affecting the currency denomination of prices
- **Local market structure**: The degree of formal versus informal commerce, the number of competitors, and the presence of large retail chains all vary by city

The econOS approach:

- Produce separate indexes for each major city where data coverage allows
- Report the national index as a weighted average of city indexes (weighted by population or estimated economic activity)
- Flag cities with insufficient data coverage, rather than imputing prices from better-covered cities
- Use the middle-income country statistical agency comparison to calibrate how much geographic variation actually matters: agencies that publish city-level CPI reveal how much city-level indexes diverge from the national average, and this divergence pattern can inform expectations for crisis economies

---

## What This Enables for Allocation

The theoretical argument is that better price information improves resource allocation. Here are the concrete channels through which a real-time price index changes behavior:

### Wage Negotiation

A worker in the formal sector is told by their employer that a 10% raise is generous. Without current price data, the worker can only push back with anecdotal impressions. With a real-time price index, the worker can say: "The cost of the basic basket has risen 18% in the past three months. A 10% raise is a real wage cut." This is not hypothetical. Workers' primary complaint during economic crises -- echoed by independent labor organizations, unions, and ordinary workers on social media -- is that wages do not keep up with prices. The problem is not just that wages are low; it is that workers cannot precisely quantify how low, because the inflation data is either absent or contested.

A transparent, independent, real-time price index shifts the information asymmetry in wage bargaining. It does not guarantee higher wages. But it gives workers the data to demand them, and it gives employers the data to understand what a competitive wage actually looks like.

### Business Pricing

A small business owner -- a restaurant, a bakery, a neighborhood shop -- must set prices every day, sometimes multiple times per day in volatile periods. Setting the price too high loses customers. Setting it too low means selling below replacement cost. The owner needs to know:

- What are competitors charging?
- What did my inputs cost this week versus last week?
- What is the exchange rate doing?

A real-time price index that includes competitor prices (via delivery app and web scraping data), input cost trends (via wholesale food price tracking), and the exchange rate (via P2P exchange platforms) gives the business owner a dashboard for their most critical daily decision. This is the "BI view for the economy" concept from the investment allocation optimization document, applied at the micro level.

### Remittance Optimization

Millions of people in the diaspora from crisis economies send money home. Remittance flows can reach billions of dollars annually, often exceeding foreign direct investment.

A diaspora family sending $200 per month to relatives wants to know: What does $200 buy this month? Is it more or less than last month? Should we send more this month because prices spiked? Should we advise our family to buy staples in bulk now because the price is about to rise?

Currently, this information travels through phone calls, WhatsApp messages, and anecdote. The price index makes it systematic: a city-level cost-of-living figure, updated weekly, expressed in dollars, showing trends. The diaspora family can see that $200 buys 85% of last month's basket, and adjust accordingly.

At scale, this price transparency may also affect remittance corridors. If the cost of living in one city is rising faster than in another, the aggregate flow of remittances may shift, redistributing diaspora support toward higher-need areas. This is resource reallocation driven by information.

### Migration Decisions

Mass emigration from crisis economies represents one of the largest displacement patterns in recent history. Migration decisions are driven by many factors -- safety, family, legal status, opportunity -- but economic calculation is central. A person considering emigration is implicitly comparing:

- The real value of their income at home (income divided by local prices)
- The expected real value of their income at the destination (expected wages divided by destination prices)
- The costs of migration (travel, legal, social)

A real-time, multi-city price index that covers both home country cities and major destination cities enables this calculation with actual data rather than guesswork. It does not make the decision -- there are non-economic factors that no price index captures -- but it ensures the economic dimension of the decision is informed.

### Independent Economic Signal

Perhaps the most important function: a transparent, independent, methodologically documented price index provides a signal that cannot be suppressed or manipulated by the government.

When central banks stop publishing CPI, they create an information vacuum that serves the government's interest in obscuring the severity of a crisis. An independent price index -- produced from publicly observable data, with published methodology, maintained by a distributed team, and hosted on infrastructure outside government control -- is resistant to this kind of suppression. The data exists because the prices exist. As long as retailers post prices online, as long as P2P exchange platforms operate, as long as citizens share prices on WhatsApp, the inputs to the index are available. No government decision can make the data disappear.

For economists, journalists, opposition politicians, international organizations, and ordinary citizens, this independent signal is a tool for accountability. It answers the question "how are things actually going?" with data rather than narrative.

---

## Technical Architecture: From Data Sources to Published Index

### Data Collection Pipeline

```
Layer 1: Web Scraping (daily)
  Regional e-commerce platforms, pharmacy chains, supermarket chains
  → Raw prices with product identifiers, timestamps, currency denomination, seller location
  → Stored: raw HTML + extracted structured data

Layer 2: Exchange Rate (continuous/hourly)
  P2P exchange platform APIs, independent rate trackers, central bank official rate
  → Bid/ask rates, volumes, timestamps
  → Stored: time series database

Layer 3: Social Media (daily/as available)
  WhatsApp/Telegram group monitoring, Instagram business accounts, Twitter/X
  → Unstructured text and images → NLP/OCR processing → structured price observations
  → Stored: raw content + extracted observations with confidence scores

Layer 4: Delivery Apps (daily)
  Dominant local delivery platforms
  → Structured product prices, restaurant prices, category data
  → Stored: structured data with timestamps and geographic markers

Layer 5: Institutional (monthly/as published)
  National statistical agency CPI, central bank releases, independent consumer organizations, IMF estimates
  → Structured official data
  → Stored: official statistics database
```

### Product Matching and Classification

Each price observation must be mapped to a standardized product category. The classification should follow COICOP (Classification of Individual Consumption According to Purpose) at the top level, for comparability with official CPI baskets, with finer-grained subcategories as data allows.

Product matching uses:

- SKU/barcode matching where available (e-commerce platforms often include this)
- Brand + product name + size matching for packaged goods
- Category-level matching for products without specific identifiers (e.g., "chicken breast, per kg")
- Machine learning models trained on the product matching task, improving over time

### Index Construction

The basic methodology follows standard price index construction, adapted for the multi-source, multi-currency context:

1. **Compute category-level price changes**: For each product category, compute the percentage change in the median (or geometric mean) price from the previous period. Use the median rather than the mean to reduce sensitivity to outliers (a single misreported price).

2. **Weight categories**: Use expenditure weights that approximate local household spending patterns. For crisis economies where no current household expenditure survey exists, weights must be estimated from the best available sources -- independent consumer organization food basket compositions, private research firm estimates, and cross-country comparisons with middle-income country household surveys (adjusted for different consumption patterns). For middle-income countries, official household survey-derived weights serve as the benchmark.

3. **Compute sub-indexes**: Separate sub-indexes for food, housing, transportation, services, and other categories. These are individually useful (food inflation is the most important single number for most households in developing economies).

4. **Compute currency-specific indexes**: Separate indexes for local currency-denominated prices and dollar-denominated prices. A blended index weighted by estimated transaction shares in each currency.

5. **Aggregate to city-level and national indexes**: City-level indexes for cities with sufficient data coverage. National index as a population-weighted average of city indexes.

6. **Report with uncertainty**: Every index value accompanied by a confidence range reflecting the number of price observations, the cross-source consistency, and the estimated coverage of the product category.

### Publication

- **Daily index values**: Published to a public website and API
- **Weekly summary**: A human-readable report covering the week's price movements, notable changes, and exchange rate dynamics
- **Monthly comparison**: A formal comparison of the econOS index against official CPI releases (where available)
- **Full methodology document**: Publicly available, version-controlled, updated when methodology changes
- **Raw data access**: API access to individual price observations (anonymized by source where necessary) for researchers and journalists

---

## What Comes Next: From Price Index to Price Infrastructure

A real-time price index is the first step. Over time, the data infrastructure it creates enables increasingly sophisticated applications:

**Price prediction**: With sufficient historical data (6-12 months minimum), time-series models can forecast short-term price movements. This is useful for businesses planning purchases, for families timing major expenditures, and for the exchange rate (where short-term predictability, even modest, has value for remittance timing).

**Price dispersion analysis**: Not just "what is the price?" but "how much does the price vary across sources, cities, and time?" High price dispersion indicates market fragmentation and opportunities for arbitrage. Low dispersion indicates competitive, well-connected markets. Tracking dispersion over time measures whether markets are integrating or fragmenting.

**Relative price tracking**: Not just "are prices rising?" but "which prices are rising relative to others?" If food prices rise 20% while electronics prices fall 5%, the relative price has shifted, signaling changes in supply, demand, or cost structures that affect production and consumption decisions.

**Cross-border price comparison**: Systematic, product-level price comparison between crisis economy and neighboring country cities. This is the data layer needed for the migration and remittance decision-support tools described in the highest-leverage areas document.

**Informal economy price intelligence**: As the social media and WhatsApp data layers mature, they provide insight into informal market prices that no formal data source captures. Over time, this creates a unique dataset on the informal economy's price dynamics -- a contribution to economic knowledge that currently does not exist for any country.

---

## Honest Assessment of Limitations

This document has described a methodology. Here is what it will not achieve:

**It will not measure the full cost of living.** A price index based on observable market prices cannot capture queuing costs (time spent searching for goods), quality degradation (services that nominally exist but function poorly), or the welfare loss from goods that are simply unavailable. During the worst periods in crisis economies, these non-price costs are enormous. They diminish as economies stabilize, but they remain real.

**It will underrepresent the poorest households.** The data sources -- online retail, delivery apps, social media groups -- all require internet access and some level of digital engagement. The poorest residents, particularly in rural areas and in urban informal settlements with weak connectivity, are the least likely to generate data and the most likely to face different prices (often higher, due to transportation costs and limited competition in underserved areas). The index will be more representative of the urban, digitally connected majority than of the rural or deeply informal poor.

**It will not capture services well.** Healthcare costs, education costs, legal services, home repair -- these are difficult to track through any automated method. Delivery apps capture some restaurant and pharmacy services, but the broader service economy remains hard to measure. This is also a limitation of the BPP and of BLS CPI (which relies on labor-intensive field collection for services).

**The social media layer is experimental.** Extracting structured price data from WhatsApp group messages and Instagram posts using NLP and OCR is feasible with current technology but noisy. The error rate will be higher than for web-scraped e-commerce data. This layer should be treated as supplementary and experimental until the processing pipeline is validated.

**The data environment can deteriorate again.** The current moment -- where online retail is functioning, P2P exchange platforms are active, and social media price reporting is widespread -- reflects a period of relative stabilization. A renewed economic crisis, increased government internet censorship, or platform shutdowns (P2P platforms have faced regulatory pressure in multiple countries) could degrade the data sources. The system must be designed for resilience: multiple sources, no single point of failure, data archived continuously.

These limitations are real. They should be documented alongside every published index value. Transparent methodology that acknowledges what it cannot measure is infinitely more valuable than opaque methodology that claims to measure everything.

---

## The Argument in Summary

Prices are the most fundamental signal in any market economy. Hayek's entire framework rests on the proposition that prices encode dispersed information into a form that enables decentralized coordination. When prices are visible and current, allocation improves -- automatically, without anyone directing it, through millions of individual responses to the price signal. When prices are obscured, distorted, or destroyed, allocation degrades just as automatically.

Crisis economies have experienced the most extreme episodes of price signal destruction in modern history. Price controls break the signaling function. Currency controls break the exchange rate signal. Statistical blackouts eliminate even the measurement of the damage. The result can be GDP contractions of 50-75% -- not because resources disappear, but because the information system that coordinates resources collapses.

Rebuilding that information system -- starting with the most fundamental signal, prices -- is not an academic exercise. It is rebuilding the market itself. A real-time, multi-source, multi-currency price index for crisis economies, validated against functional statistical infrastructure in middle-income countries, is the single highest-leverage data product that econOS can build. It serves the worker negotiating wages, the business owner setting prices, the diaspora family calibrating remittances, the potential migrant comparing cost of living, and the economist tracking recovery. It provides an independent signal that cannot be suppressed. It fills a void that no institution currently fills.

The methodology is proven. The Billion Prices Project demonstrated a decade ago that web-scraped daily price indexes work -- that they track official CPI in stable countries and provide superior information in unstable ones. The data sources are richer today than they were when the BPP operated: delivery apps, social media price networks, cryptocurrency exchange platforms, and mobile payment systems provide coverage that was unavailable in 2008.

What is missing is the infrastructure to collect this data systematically, aggregate it transparently, and publish it as a public good. That is what this document specifies. The price index is the beating heart of econOS -- the foundation on which every other measurement depends, the proof of concept that establishes credibility, and the tool that delivers immediate, tangible value to the people who need it most.
