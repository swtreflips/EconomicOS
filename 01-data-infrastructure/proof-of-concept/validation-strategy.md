# Validation Strategy: How Do We Know It's Right?

## The Fundamental Challenge

In the US, you validate a nowcast against the official GDP release. The official number is imperfect, but it's credible enough to serve as ground truth. In Venezuela, the ground truth barely exists. The BCV's credibility is damaged. The INE's employment data is spotty. There's no Census retail sales report to beat.

So how do you validate a real-time economic signal in a country where the official benchmark is unreliable or absent?

The answer: **cross-validation, internal consistency, and external anchoring.** You don't validate against one source. You validate by checking whether multiple independent signals tell a consistent story, and you anchor to the hardest-to-manipulate data points available.

---

## Validation Framework

### Layer 1: Cross-Source Consistency

If the price tracker says food prices rose 8% this month, does that signal appear across multiple independent sources?

| Signal | Source | Independent? |
|--------|--------|-------------|
| Online retail prices | MercadoLibre, Farmatodo | Yes -- different retailers, different products |
| Delivery app prices | Yummy, PedidosYa | Yes -- different platform, overlapping products |
| Social media prices | WhatsApp groups, Instagram | Yes -- informal, unstructured, but real transactions |
| Exchange rate movement | Binance P2P, Monitor Dolar | Yes -- different market, but prices in bolivares should move with exchange rate |

If web-scraped supermarket prices show 8% food inflation and delivery app prices show 7-9% in the same categories, and the bolivar depreciated by a comparable amount on Binance P2P, the signals corroborate each other. If one source diverges sharply, that's either a data quality issue (investigate) or a real phenomenon worth understanding (e.g., online prices moving faster than physical store prices).

**Rule: No single source is trusted alone. The indicator is the convergence of multiple independent signals.**

### Layer 2: External Anchors

Some data points are hard to manipulate and can serve as anchors:

**Satellite nighttime lights (VIIRS)**: Economic activity correlates with light output. If the spending tracker says the economy is growing but nighttime lights are stable or declining in a region, something is wrong. NASA/NOAA publishes this data freely with ~1 week lag.

**Electricity consumption**: Economic activity requires electricity. If CORPOELEC data is accessible (or can be estimated from satellite thermal signatures), it's a physical-world check on digital signals.

**Binance P2P volume and exchange rate**: The bolivar/USDT rate on Binance P2P is set by millions of individual transactions. It's very hard to manipulate at scale. It provides a currency anchor for converting all prices to a common unit.

**Remittance volumes**: Formal remittance data (Western Union, Remitly) provides a partially independent check on diaspora economic activity. If spending is rising, remittance inflows should be consistent with that.

**Colombia trade data**: DANE publishes Colombia-Venezuela trade statistics. While incomplete (much trade is informal), formal trade flows provide an external check on Venezuelan economic activity.

**IMF, World Bank, and ECLAC estimates**: International organizations produce their own Venezuela GDP and inflation estimates using cross-country models. These are rough but serve as sanity checks.

### Layer 3: Backtesting Against Known Events

Even without a reliable official benchmark, we know what happened during certain periods:

- **2018 hyperinflation peak**: Any price index should show acceleration through 2018 consistent with independent estimates (Hanke, AN).
- **2019-2020 dollarization acceleration**: The spending mix should shift toward USD-denominated transactions.
- **COVID lockdowns (March-April 2020)**: Spending should show a sharp drop, consistent with global patterns.
- **2021-2023 partial recovery**: Gradual spending recovery, dollarization stabilizing, some sectors rebounding.

If the indicator is backfilled and shows these known patterns, it's calibrated correctly. If it misses a known event (e.g., doesn't show a COVID spending drop), something is wrong with the methodology.

### Layer 4: Colombia as Validation Lab

Colombia has a functional statistical agency (DANE). This creates a unique validation opportunity:

1. **Build the methodology in Venezuela** (where it's needed most)
2. **Apply the same methodology in Colombia** (where DANE data exists as benchmark)
3. **Validate the methodology in Colombia against DANE** (CPI, retail sales, employment)
4. **Use the validated methodology in Venezuela with confidence**

If web-scraped prices in Colombia track DANE CPI within a reasonable margin (say, ±1-2 percentage points monthly), the same scraping methodology applied to Venezuelan retailers should produce credible results.

This is the strongest validation path available: **prove the methodology works where ground truth exists, then apply it where ground truth doesn't.**

---

## Validation Metrics

### For the Price Index

| Metric | Target | How to measure |
|--------|--------|----------------|
| Cross-source correlation | >0.85 between web-scraped and delivery app prices | Monthly correlation coefficient |
| Colombia CPI tracking | Within ±2 ppts monthly | Compare econOS Colombia price index to DANE CPI |
| Exchange rate consistency | Price movements consistent with bolivar/USD rate changes | Regression of price index on exchange rate |
| Known event detection | Correctly identifies hyperinflation peak, COVID drop, recovery | Visual + statistical verification against timeline |
| Direction accuracy | Correctly identifies inflation increasing/decreasing >80% of months | Directional accuracy against multiple sources |

### For the Spending Signal

| Metric | Target | How to measure |
|--------|--------|----------------|
| Satellite correlation | Positive correlation between spending signal and nighttime lights changes | Regional correlation analysis |
| Seasonal pattern detection | Shows expected patterns (December holiday spending, carnival, etc.) | Seasonal decomposition |
| Colombia retail tracking | Within ±3 ppts of DANE monthly retail sales growth | Compare econOS Colombia spending signal to DANE |
| Internal consistency | Spending categories move in expected directions (e.g., food stable, discretionary volatile) | Category-level coherence analysis |

### For Labor Market Signals

| Metric | Target | How to measure |
|--------|--------|----------------|
| Job posting trends | Directionally consistent with DANE/GEIH employment changes in Colombia | Correlation of job posting growth with employment growth |
| Wage data plausibility | Reported wages consistent with known minimum wage and informal benchmarks | Range checks, percentile analysis |
| Migration flow consistency | Job postings in destination countries correlate with known migration corridors | Cross-country comparison |

---

## What "Success" Means

**Stage 1 (Months 1-3): Internal credibility**
- Multiple data sources are being collected reliably
- Cross-source consistency is demonstrated
- The methodology is documented and reproducible

**Stage 2 (Months 3-6): External validation**
- Colombia methodology validated against DANE
- Backtesting correctly identifies known Venezuelan economic events
- At least one external reference (IMF, World Bank, academic researcher) acknowledges the data

**Stage 3 (Months 6-12): Usage credibility**
- People are actually using the data (measured by website visits, API calls, media citations)
- The data is referenced in economic analysis or reporting about Venezuela
- Errors are identified and corrected transparently (building trust through honesty about limitations)

**Stage 4 (Year 1+): Institutional credibility**
- International organizations reference or incorporate the data
- Academic researchers use it
- The diaspora community treats it as a trusted source
- Other developing countries express interest in replicating the approach

---

## The Honesty Principle

The most important validation strategy is **radical transparency about limitations**:

- Every indicator should publish its confidence interval, not just a point estimate
- Every data source should have its coverage and known biases documented
- Every methodology change should be versioned and explained
- When the data is uncertain, say so. "We estimate inflation at 8-12% this month" is more credible than "inflation was 9.7%."

Trust is built by being consistently honest about what you know and what you don't. In a country where official data was suppressed and manipulated, honesty about uncertainty is itself a radical act of credibility.
