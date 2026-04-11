# Transaction Data as a Real-Time Economic Signal

## 1. The Payment Landscape in Crisis and Developing Economies

In many developing countries, particularly those that have experienced monetary collapse or hyperinflation, the payment landscape does not resemble the card-dominated system of the United States. Instead, what emerges is a layered, improvised stack of payment methods shaped by crisis -- a fundamentally different structure that must be understood on its own terms.

### Mobile Payment Systems

In economies where cash becomes physically unavailable during hyperinflation, mobile interbank payment systems often fill the void. These systems -- operated by the central bank or banking consortium -- allow person-to-person and person-to-merchant transfers between bank accounts using a phone number and national ID. No card required.

Such systems become dominant not because they are technologically superior, but because they are the only way to transact in local currency at all. Every bank in the interbank system connects. The merchant does not need a POS terminal -- just a bank account and a phone. This gives mobile payment systems penetration into economic segments that card networks never reached: street vendors, taxi drivers, and small shops all participate.

**Data signal**: Mobile payment transaction volumes and values, if accessible, would be the single best proxy for formal domestic economic activity in local currency. The central bank has aggregate data on interbank transfer volumes. Whether this data is published in usable form is a different question (see Section 7).

### Dollar-Denominated Payment Platforms

In dollarized crisis economies, US domestic payment platforms can be adopted as de facto dollarized payment systems. Individuals with US bank accounts use person-to-person dollar transfers to pay for goods and services domestically. Businesses in major cities quote prices in "Zelle dollars." A restaurant might list a meal as "$12." A landlord might set rent at "$400 per month."

The mechanism is simple but has profound implications:
- Buyer and seller both have US bank accounts
- Payment is sent in USD
- The transaction settles through the US banking system, not the domestic one
- Local authorities have no visibility into it

These transactions are completely invisible to domestic financial infrastructure. The economic activity they represent -- rent, retail purchases, services, wholesale transactions -- is happening locally but is recorded nowhere in domestic data.

**Data signal**: Essentially zero from the domestic side. From the US side, these platforms do not publish geographic or purpose-of-transaction data. This is a major blind spot.

### P2P Exchange Platforms

Countries experiencing currency instability consistently rank among the top globally for peer-to-peer crypto trading volume. This is not because the population are crypto enthusiasts. It is because P2P exchange platforms serve as de facto foreign exchange markets.

The typical flow:
1. Person A has local currency in a domestic bank account
2. Person A wants dollars (USDT, a stablecoin pegged to USD)
3. Person A goes to a P2P exchange platform, finds a counterparty willing to sell USDT for local currency
4. Person A sends local currency via mobile payment or bank transfer
5. The counterparty releases USDT to Person A's wallet
6. Person A now holds dollar-equivalent value

This becomes the de facto foreign exchange market. The official exchange rate set by the central bank often diverges from the P2P rate, and the P2P rate is typically treated as the real market rate.

**Data signal**: P2P volume data is partially accessible through exchange APIs and third-party aggregators. The local-currency/USDT trading pair volume is a real-time indicator of currency exchange pressure, dollarization demand, and economic activity. The spread between the official rate and the P2P rate is itself an economic signal -- wider spreads indicate greater distrust of official monetary policy.

### Cash (Foreign and Local Currency)

Physical US dollar bills circulate widely in many crisis economies, particularly in border regions and informal markets. Denominations matter: small bills ($1-$20) are common; larger bills are less circulated due to counterfeiting concerns and difficulty making change.

Physical local currency bills exist but in diminished relevance after redenominations. Most transactions above trivial amounts go through mobile payment systems.

**Data signal**: Cash transactions are invisible to digital systems. In economies where a significant share of activity -- street food, informal transport, domestic work, small-scale commerce -- transacts in physical dollars, this invisibility is a major limitation.

### Bank Transfers (Domestic, Non-Mobile)

Standard bank-to-bank transfers within the domestic banking system still occur, particularly for larger transactions (business payments, formal sector payroll). These flow through the central bank's payment infrastructure.

**Data signal**: Captured in banking system data but not typically disaggregated in public reporting.

---

## 2. The Payment Landscape in Middle-Income Developing Countries

Countries with more stable economies but large informal sectors present a different but related picture, undergoing rapid transformation driven by mobile payment platforms.

### Digital Wallets and Mobile Payment Platforms

Digital wallet and payment platforms -- often owned by major banks -- have grown rapidly in middle-income developing countries, reaching tens of millions of users. These allow person-to-person transfers, bill payments, QR code merchant payments, and cash withdrawals.

Growth accelerated during COVID-19. These platforms are particularly popular among younger, urban populations. Some platforms were designed for financial inclusion, targeting lower-income and rural populations, and serve as the channel through which governments distribute social transfers.

**Data signal**: Digital wallet transaction volumes would be a strong proxy for digital economy activity. Combined data from multiple platforms provides a more representative picture than any single source, since different platforms skew toward different demographics (younger/urban vs. lower-income/government-transfer recipients).

### Online Bank Transfer Systems

National online bank transfer systems enable direct bank-to-bank payments for e-commerce, bill payments, and government services. These process hundreds of millions of transactions annually and serve as the backbone of formal e-commerce payment.

**Data signal**: Aggregate volumes are sometimes published by the operating consortium and provide a reasonable proxy for formal online economic activity.

### Cards (Visa, Mastercard, Domestic Networks)

Card penetration in developing countries is growing but remains well below US levels. Card usage is concentrated in formal retail, supermarkets, and e-commerce. Most informal commerce -- which represents a large share of economic activity -- does not accept cards.

**Data signal**: Card transaction data follows the same logic as in the US (see Section 8) but with much lower coverage of total economic activity.

### Cash

Cash remains the dominant payment method for the majority of face-to-face transactions in many developing countries, even as digital payments grow. Central bank estimates often place cash usage at over 80% of face-to-face retail transactions. Cash dominance is particularly pronounced in rural areas, informal markets, small towns, transportation, and neighborhood shops.

**Data signal**: Invisible, same as everywhere. But in developing countries, "invisible" means the majority of transactions.

---

## 3. Remittance Flows as Economic Data

Remittances are not a peripheral data source for developing countries with large diasporas. They are a central economic flow.

### Crisis Economies

Countries experiencing mass emigration may receive billions of dollars per year in remittances, though exact figures are unreliable because a large share flows through informal channels. Diasporas numbering in the millions send money home regularly.

Formal remittance channels include traditional operators (Western Union), digital services (Remitly, Wise, WorldRemit), dollar-denominated payment platforms repurposed for remittances, and P2P exchange platforms used to convert and transfer value.

Informal channels include physical cash carried by travelers (especially at border crossings), informal money transfer networks (similar to hawala systems), and crypto transfers outside major exchanges.

**Data signal**: Formal remittance data is partially captured by the World Bank's bilateral remittance matrices, by central bank balance-of-payments data, and by the remittance companies themselves. The World Bank estimates total flows but with significant uncertainty for countries with large informal channels. Remittance volume, frequency, and geographic origin patterns are proxies for diaspora economic health, family dependency ratios, and labor market conditions in host countries.

Seasonality matters: remittances spike around holidays, school enrollment periods, and family emergencies. Tracking these seasonal patterns provides insight into household economic planning.

### Middle-Income Developing Countries

Countries with large but more established diasporas may receive tens of billions in remittances annually, ranking among the top remittance-receiving countries in their region. Formal channels are better established and more dominant than in crisis economies, with large physical agent networks, direct bank receipt via digital wallets, and digital platforms.

The central bank may publish detailed remittance data with a lag of approximately 2-3 months, broken down by country of origin and recipient region. This represents some of the best remittance datasets available in developing economies.

**Data signal**: Formal remittance data may be relatively strong. The challenge is incorporating informal flows, which are smaller as a percentage of total than in crisis economies but still significant, particularly along border regions.

---

## 4. What Transaction Data Can Measure in Developing Economies

Given the payment landscape described above, what can digital transaction data actually tell us?

### Formal Digital Economy Activity

Mobile payment volumes and digital wallet transaction data provide a real-time pulse of formal digital economic activity. When mobile payment transaction counts rise, more people are buying and selling through the banking system. When they fall, activity is contracting or migrating to other channels (cash, crypto).

This is not the same as measuring GDP. It measures the **banked, digital portion of economic activity**. But changes in this portion over time -- growth rates, seasonal patterns, shock responses -- are highly informative.

### Currency Preferences as an Economic Signal

In dollarized crisis economies, the ratio of local-currency transactions (mobile payments) to dollar transactions (dollar-denominated platforms, crypto) is itself a macroeconomic indicator. When people shift toward dollars, it signals declining confidence in monetary policy. When local-currency transaction volumes stabilize or grow relative to dollar alternatives, it may signal stabilization.

The P2P exchange spread over the official rate is a daily, tradeable measure of monetary credibility. This is a signal that no government statistical agency publishes but that every participant in currency exchange knows intimately.

### Price Signals Through Exchange Platforms

Crypto exchange data provides something that official statistics in crisis economies often cannot: reliable price signals. When the central bank publishes an official exchange rate that diverges from the P2P rate, the P2P rate is the one that merchants use to set prices. Tracking the parallel rate through exchange platform data is tracking the actual pricing mechanism of the economy.

In more stable developing countries, where the currency floats more freely and the gap between official and market rates is minimal, this signal is less critical. But cross-border exchange flows at border towns are still informative.

### Geographic Activity Patterns

Mobile payment data has geographic markers (bank branch, city, phone prefix). If accessible in aggregate form, this allows mapping economic activity intensity across regions -- something particularly valuable in countries where official regional economic statistics are essentially nonexistent.

---

## 5. What Transaction Data Misses

### The Informal Cash Economy

This is the single largest blind spot and it is enormous.

In crisis economies, street vendors, informal transport operators, domestic workers, day laborers, small-scale agriculture sellers, and a substantial portion of the service economy transact in physical cash -- primarily US dollars for anything above trivial amounts, and local currency for the smallest transactions. None of this appears in any digital payment system.

In middle-income developing countries, the picture is similar. Neighborhood corner stores (estimated in the hundreds of thousands across many countries), street food vendors, informal construction labor, domestic workers, and the vast informal transport sector operate predominantly in cash. The informal economy is estimated at 50-60% of total employment in many such countries.

When digital transaction data shows "the economy," it is showing the formal, banked, digitized portion. In countries where 40-60% of economic activity is informal, this is a severe limitation.

### Street Vending and Micro-Commerce

A street vendor selling staple goods might do 50 transactions a day, all in cash. Total daily revenue might be $30-50. This vendor contributes to economic activity, employs themselves (and possibly family members), participates in supply chains (buying ingredients from wholesale markets), and serves consumer demand. None of this is captured.

Multiply this by the hundreds of thousands of informal vendors in developing-country cities and the missing data is not marginal.

### Day Labor and Gig Work (Non-Platform)

Platform gig workers (delivery riders, for example) generate digital transaction trails. But the much larger pool of non-platform informal labor -- construction day workers, domestic cleaners paid in cash, informal mechanics, unlicensed taxi drivers -- generates no digital footprint.

### Barter and In-Kind Exchange

In the worst periods of economic crisis, barter can become a real economic mechanism -- not metaphorically, but literally. People exchange goods for goods. This diminishes as dollar economies stabilize, but in-kind exchanges (labor for food, goods for services) still occur, particularly in rural areas and among the poorest populations.

---

## 6. Biases and Representativeness

The income bias problem with transaction data that exists in the United States is dramatically amplified in developing economies.

### Income Bias

In the US, the poorest 20% of the population still overwhelmingly has bank accounts and uses debit cards. The unbanked rate is approximately 4.5% (FDIC, 2021). The bias exists but is moderate.

In crisis economies, while bank account penetration may be relatively high (mobile payments pushed banking access), the quality of access varies enormously. Someone with a major bank account and steady mobile payment usage is visible. Someone earning cash dollars in the informal economy and spending cash dollars at informal vendors is completely invisible. The most economically precarious populations -- street vendors, day laborers, people in rural areas with unreliable phone service -- are the least visible in digital payment data.

In middle-income developing countries, the unbanked population may be estimated at 10-15%, but "underbanked" (having an account but rarely using it for transactions) is much higher. Digital wallets have expanded access, but active digital payment usage still correlates strongly with income, education, and urbanization.

### The Poorest Are the Most Invisible

This is worth stating directly because it is the central representativeness problem for econOS in developing economies. The populations most in need of economic measurement -- the informal workers, the street vendors, the households surviving on cash remittances and day labor -- are the ones least captured by any digital transaction system. Building an economic measurement tool on digital payment data risks creating a system that measures the formal economy well and the informal economy not at all, which would systematically misrepresent economic reality in countries where informality is the norm, not the exception.

### Currency Bias

In dollarized crisis economies, measuring only local-currency-denominated transactions (mobile payments, bank transfers) misses the dollarized economy. Measuring only dollar-denominated transactions (dollar platforms, crypto) misses the local-currency economy. The true picture requires combining both, with appropriate weighting that itself depends on estimates of dollarization levels.

### Platform Bias

Each payment platform has its own demographic skew:
- Digital wallets aimed at younger users: younger, urban, middle-class populations
- Financial inclusion platforms: lower-income, some rural, government transfer recipients
- Mobile payment systems: broad but skews toward those with stable banking relationships
- Dollar-denominated platforms: those with US bank access (a specific, non-representative subset)
- P2P exchange platforms: tech-literate, typically younger, often with some dollar access

No single platform represents the economy. Any measurement system must combine multiple sources and explicitly model the biases of each.

---

## 7. Cost and Accessibility

Can the transaction data described above actually be obtained?

### Mobile Payment / Domestic Banking System (Crisis Economies)

In crisis economies, the central bank may publish some aggregate statistics on interbank transactions, but the data is limited, irregularly updated, and not available through any API or structured feed. Individual banks do not publish transaction volume data.

The banking supervisory authority collects banking statistics, but public reporting is sparse and often delayed by months.

**Assessment**: Getting useful aggregate mobile payment data would likely require either a direct institutional partnership with one or more domestic banks, or access to central bank/supervisory reporting that is currently not publicly available in usable form. This is a significant barrier.

### Digital Wallets / Banking System (Middle-Income Developing Countries)

In countries with stronger institutional frameworks, the financial superintendent publishes more regular and detailed banking statistics. Payment system operators publish transaction volumes. The central bank publishes payment system statistics.

Major banks publish some aggregate data in quarterly reports and investor presentations. Digital wallet platforms publish user count milestones but not detailed transaction data.

**Assessment**: The data environment in more stable developing countries is materially better. Aggregate payment system data is obtainable through public sources. Granular data (by region, by transaction size, by merchant category equivalent) would require partnerships, but the institutional infrastructure for such partnerships exists.

### Crypto Exchange APIs

P2P exchange platforms provide public APIs that include some trading data, though not comprehensive historical archives. Third-party sites track P2P volumes by country. The local-currency/USDT pair is trackable in near real-time.

**Assessment**: This is the most accessible data source for crisis economies. Crypto exchange data can be scraped, accessed via API, or obtained through third-party aggregators. It is not comprehensive, but it is real-time and accessible.

### Remittance Data

The World Bank publishes annual bilateral remittance estimates. Central banks in countries with strong institutions publish quarterly remittance data by country of origin. Individual remittance companies do not publish transaction data, but some (Wise, for example) publish aggregate corridor data in transparency reports.

**Assessment**: Formal remittance data is available with moderate lag (quarterly to annual). Real-time remittance flow data would require partnerships with platforms like Remitly, Wise, or Western Union.

### Central Bank Reporting

Central banks in more stable developing countries may have strong data publication programs -- payment statistics, remittance data, monetary aggregates, and financial system reports available through their websites with structured data access.

Central banks in crisis economies have historically published economic data but with increasing irregularity and credibility concerns. Basic monetary aggregates and some payment system data may be published, but with significant lags and questions about reliability.

**Assessment**: Central banks in stable developing countries are viable data sources. Central banks in crisis economies are not reliable for timely, granular transaction data.

---

## 8. Reference: How It Works in the US

For comparison, the US transaction data ecosystem is mature, deep, and expensive.

The US processes roughly 150-170 billion card transactions per year. Visa processed $14.8 trillion in payment volume in fiscal 2023; Mastercard processed approximately $8.9 trillion. The card networks do not sell raw transaction data but publish aggregated indexes: Visa Business and Economic Insights and Mastercard SpendingPulse provide spending trend data used by analysts and researchers.

A layer of fintech data aggregators -- Earnest Research (MarketAxess), Second Measure (Bloomberg), Yodlee (Envestnet), Plaid -- aggregate anonymized transaction data from banking partners. These products cost $100K-$500K+ per year and are used primarily by hedge funds and equity research.

Bank research arms (Bank of America Institute, JPMorgan Chase Institute) publish periodic analyses based on their internal transaction data, covering tens of millions of accounts each.

The landmark proof of concept was the Opportunity Insights Economic Tracker (Chetty et al., 2023), which used Affinity Solutions card data during COVID-19 to track real-time consumer spending by income group, geography, and category -- demonstrating that private transaction data, properly anonymized and aggregated, could provide economic insights faster and with more granularity than official statistics.

The US model is relevant as a reference point but is not directly replicable in developing economies. Card penetration, data provider ecosystems, and institutional norms around data sharing are fundamentally different. The lesson from the US is that transaction data works for economic measurement. The challenge in developing countries is that the transaction data infrastructure is different in kind, not just in degree.

---

## 9. The econOS Opportunity

The payment landscapes of developing economies, precisely because they are fragmented and unconventional, present an opportunity that is different from but potentially larger than the US case.

### Mobile Payments as the Backbone

In the US, econOS would need to negotiate with entrenched players (Visa, Mastercard, banks) who already monetize their data. In crisis economies, mobile payment data is sitting in a banking system that has no existing data monetization infrastructure. The competitive dynamics are different. The barriers are institutional and political, not commercial.

If econOS can establish a data partnership with even one major domestic bank, it would gain access to a substantial share of formal domestic local-currency transactions. Combined with crypto exchange data (accessible via API) and remittance corridor data, this would constitute the most comprehensive real-time economic dataset for a crisis economy in existence. There is no Bloomberg terminal, no Mastercard SpendingPulse, no Opportunity Insights tracker for these countries. The baseline is near zero.

In more stable developing countries, the path is more conventional but still open. Digital wallet platforms are growing fast and have not yet been fully leveraged for macroeconomic measurement. The central bank may already publish good data. The opportunity is to integrate multiple data sources (digital wallet volumes, online payment data, card data, remittance data, central bank statistics) into a unified real-time picture that currently does not exist in combined form.

### Multi-Source Integration

The real value proposition is not any single data source but the combination:

| Data Source | Coverage | Accessibility | Signal |
|---|---|---|---|
| Mobile payment system (crisis economy) | Formal local-currency economy | Difficult -- requires bank partnerships | Domestic activity level |
| Dollar-denominated platform (crisis economy) | Dollarized formal transactions | Inaccessible from domestic side | N/A without US-side data |
| P2P exchange platform (crisis economy) | Currency exchange, dollarization | Moderate -- API and scrapers | Exchange rate, dollarization demand |
| Digital wallets (middle-income country) | Digital economy, younger/urban population | Moderate -- some public data, partnerships needed for granularity | Consumer spending, financial inclusion |
| Online payment system (middle-income country) | Formal e-commerce | Good -- operator publishes data | Online economic activity |
| Remittances (both) | Diaspora economic support | Moderate -- World Bank, central bank data, platform partnerships | External dependency, household income |
| Cash (both) | Informal economy | None | Blind spot |

### What "Real-Time Economic Measurement" Means Here

In the US, "real-time economic measurement" means beating the developed-world statistical agencies' retail sales report by two weeks. The improvement is marginal -- from a 14-day lag to a 1-day lag on an economic indicator that already exists.

In a crisis economy, "real-time economic measurement" means producing economic indicators that do not currently exist in any reliable form. Countries may not have published complete, credible GDP data in years. Inflation estimates may come from independent sources rather than the central bank. Regional economic data may be essentially nonexistent.

An econOS system that aggregates mobile payment volumes, P2P exchange data, and remittance flows would not be competing with existing statistics. It would be creating economic visibility where there currently is none. This is a fundamentally different value proposition than in developed markets.

### The Informal Economy Problem Is Not Solvable by Transaction Data Alone

This must be stated clearly. In economies where 40-60% of activity is informal and cash-based, digital transaction data cannot provide a complete picture. econOS in developing countries must be designed from the start to acknowledge and explicitly model the informal economy gap, using complementary approaches:

- Satellite imagery (nighttime lights, commercial activity indicators)
- Survey-based calibration (periodic informal economy surveys to estimate the digital-to-total activity ratio)
- Supply chain proxies (wholesale market volumes, import data for consumer goods)
- Mobile phone activity data (call/data usage as a general economic activity proxy)

Transaction data is the backbone, but it is not the whole skeleton.

### The Starting Point

Phase 1 for econOS in a crisis economy should focus on what is immediately obtainable:

1. **P2P exchange local-currency/USDT data** -- accessible via API, provides daily exchange rate and volume signals
2. **Public central bank data** -- whatever central banks currently publish, standardized and integrated
3. **Remittance corridor data** -- World Bank annual data supplemented by whatever platform-level data can be obtained
4. **One banking partnership** -- a single domestic bank willing to share aggregate, anonymized transaction volume data

This is a minimal viable dataset. It does not solve the informal economy problem. It does not provide granular regional data. But it would produce something that does not currently exist: a structured, regularly updated, multi-source economic activity indicator for a crisis economy.

That is the proof of concept.
