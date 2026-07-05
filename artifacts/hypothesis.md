# Hypothesis — Discipline & Cards Lane

**One-sentence claim:**
Yellow + red cards per game in World Cup matches peaked in the 1986–1994 era and have since dropped by roughly 40%, driven by a discrete rule-change inflection point in 1990 (tackle-from-behind ban + yellow card accumulation penalties), not a gradual trend.

## Decision rule
- GREEN if: ≥35% drop from peak-era (1986–1994) mean to 2010+ mean, AND biggest single-change around 1990
- RED if: <20% drop or no 1990 inflection

## Why it should hold
- 1990 rule changes (tackle-from-behind ban, formalized card accumulation → automatic suspension) were structural and hard
- Pre-1970 WC matches have no cards (introduced at 1970 WC)
- Analysis window: 1970–2022 (post-card era)

## Data source
- joshfjelstul/world-cup-database (CC-BY-SA)
- bookings.csv: 2,466 rows, 1930–2018
- matches.csv: 900 rows

## Honesty guard pre-registration
1. n = 700 WC matches (1970–2018) — adequate
2. One hypothesis, one family (no fishing)
3. Sensitivity: test yellow-only, red-only, total cards
4. Null: constant cards/game across 1970–2018
