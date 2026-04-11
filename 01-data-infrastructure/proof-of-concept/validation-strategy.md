# Validation Strategy: How Do We Know It's Right?

## The Fundamental Challenge

In the US, you validate a nowcast against the official GDP release. The official number is imperfect, but it's credible enough to serve as ground truth. In many developing countries, the ground truth barely exists. The central bank's credibility may be damaged. Employment data is spotty. There's no Census retail sales report to beat.

So how do you validate a real-time economic signal in a country where the official benchmark is unreliable or absent?

The answer: **cross-validation, internal consistency, and external anchoring.** You don't validate against one source. You validate by checking whether multiple independent signals tell a consistent story, and you anchor to the hardest-to-manipulate data points available.

---

## Validation Framework

### Layer 1: Cross-Source Consistency

If the price tracker says food prices rose 8% this month, does that signal appear across multiple independent sources?

| Signal | Source | Independent? |
|--------|--------|-------------|
| Online retail prices | E-commerce platforms, pharmacy chains | Yes -- different retailers, different products |
| Delivery app prices | Food/grocery delivery apps | Yes -- different platform, overlapping products |
| Social media prices | WhatsApp groups, Instagram | Yes -- informal, unstructured, but real transactions |
| Exchange rate movement | P2P exchange platforms, independent rate trackers | Yes -- different market, but prices in local currency should move with exchange rate |

If web-scraped supermarket prices show 8% food inflation and delivery app prices show 7-9% in the same categories, and the local currency depreciated by a comparable amount on P2P exchange platforms, the signals corroborate each other. If one source diverges sharply, that's either a data quality issue (investigate) or a real phenomenon worth understanding (e.g., online prices moving faster than physical store prices).

**Rule: No single source is trusted alone. The indicator is the convergence of multiple independent signals.**

### Layer 2: External Anchors

Some data points are hard to manipulate and can serve as anchors:

**Satellite nighttime lights (VIIRS)**: Economic activity correlates with light output. If the spending tracker says the economy is growing but nighttime lights are stable or declining in a region, something is wrong. NASA/NOAA publishes this data freely with ~1 week lag.

**Electricity consumption**: Economic activity requires electricity. If electricity utility data is accessible (or can be estimated from satellite thermal signatures), it's a physical-world check on digital signals.

**P2P exchange volume and rate**: The local-currency/USDT rate on P2P exchange platforms is set by millions of individual transactions. It's very hard to manipulate at scale. It provides a currency anchor for converting all prices to a common unit.

**Remittance volumes**: Formal remittance data (Western Union, Remitly) provides a partially independent check on diaspora economic activity. If spending is rising, remittance inflows should be consistent with that.

**Bilateral trade data**: Trading partner countries' statistical agencies publish bilateral trade statistics. While incomplete (much trade is informal in developing countries), formal trade flows provide an external check on domestic economic activity.

**IMF, World Bank, and regional body estimates**: International organizations produce their own GDP and inflation estimates for developing countries using cross-country models. These are rough but serve as sanity checks.

### Layer 3: Backtesting Against Known Events

Even without a reliable official benchmark, we know what happened during certain periods:

- **Hyperinflation peaks**: Any price index should show acceleration during known crisis periods, consistent with independent estimates.
- **Dollarization acceleration**: The spending mix should shift toward USD-denominated transactions during currency crises.
- **COVID lockdowns (March-April 2020)**: Spending should show a sharp drop, consistent with global patterns.
- **Partial recovery periods**: Gradual spending recovery, dollarization stabilizing, some sectors rebounding.

If the indicator is backfilled and shows these known patterns, it's calibrated correctly. If it misses a known event (e.g., doesn't show a COVID spending drop), something is wrong with the methodology.

### Layer 4: Validation Lab in Countries with Functional Statistics

Countries with functional statistical agencies create a validation opportunity:

1. **Build the methodology for the target country** (where it's needed most)
2. **Apply the same methodology in a country with reliable official statistics** (where benchmark data exists)
3. **Validate the methodology against official figures** (CPI, retail sales, employment)
4. **Use the validated methodology in the target country with confidence**

If web-scraped prices in a country with a credible statistical agency track official CPI within a reasonable margin (say, ±1-2 percentage points monthly), the same scraping methodology applied to retailers in the target country should produce credible results.

This is the strongest validation path available: **prove the methodology works where ground truth exists, then apply it where ground truth doesn't.**

---

## Validation Metrics

### For the Price Index

| Metric | Target | How to measure |
|--------|--------|----------------|
| Cross-source correlation | >0.85 between web-scraped and delivery app prices | Monthly correlation coefficient |
| Benchmark CPI tracking | Within ±2 ppts monthly | Compare econOS price index to official CPI in validation country |
| Exchange rate consistency | Price movements consistent with local-currency/USD rate changes | Regression of price index on exchange rate |
| Known event detection | Correctly identifies hyperinflation peak, COVID drop, recovery | Visual + statistical verification against timeline |
| Direction accuracy | Correctly identifies inflation increasing/decreasing >80% of months | Directional accuracy against multiple sources |

### For the Spending Signal

| Metric | Target | How to measure |
|--------|--------|----------------|
| Satellite correlation | Positive correlation between spending signal and nighttime lights changes | Regional correlation analysis |
| Seasonal pattern detection | Shows expected patterns (December holiday spending, carnival, etc.) | Seasonal decomposition |
| Benchmark retail tracking | Within ±3 ppts of official monthly retail sales growth | Compare econOS spending signal to official statistics in validation country |
| Internal consistency | Spending categories move in expected directions (e.g., food stable, discretionary volatile) | Category-level coherence analysis |

### For Labor Market Signals

| Metric | Target | How to measure |
|--------|--------|----------------|
| Job posting trends | Directionally consistent with official employment survey changes in validation country | Correlation of job posting growth with employment growth |
| Wage data plausibility | Reported wages consistent with known minimum wage and informal benchmarks | Range checks, percentile analysis |
| Migration flow consistency | Job postings in destination countries correlate with known migration corridors | Cross-country comparison |

---

## What "Success" Means

**Stage 1 (Months 1-3): Internal credibility**
- Multiple data sources are being collected reliably
- Cross-source consistency is demonstrated
- The methodology is documented and reproducible

**Stage 2 (Months 3-6): External validation**
- Methodology validated against official statistics in validation country
- Backtesting correctly identifies known economic events in the target country
- At least one external reference (IMF, World Bank, academic researcher) acknowledges the data

**Stage 3 (Months 6-12): Usage credibility**
- People are actually using the data (measured by website visits, API calls, media citations)
- The data is referenced in economic analysis or reporting about the target country
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

Trust is built by being consistently honest about what you know and what you don't. In countries where official data has been suppressed or manipulated, honesty about uncertainty is itself a radical act of credibility.
