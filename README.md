# WC Surprising Truths — Discipline & Cards Lane

**Finding:** Germany 2006 was the most-carded World Cup in 50 years of card history (5.5 disciplinary bookings per game), nearly twice as card-heavy as Brazil 2014 (3.0/game). The common assumption that the "brutal old days" of 1980s football were the most penalized era is FALSE — the actual peak was 2006, in a tournament most fans remember for beautiful, technical football.

**Drop from peak to 2014:** 45.9% — the most dramatic single-era discipline cleanup in the tournament's history.

## How to reproduce

```bash
# Install dependencies
pip install pandas matplotlib numpy kaggle

# Configure Kaggle credentials (need joshfjelstul/world-cup-database)
export KAGGLE_CONFIG_DIR=~/.kaggle

# Download data
kaggle datasets download joshfjelstul/world-cup-database -p . --unzip

# Run analysis
python3 src/discipline_analysis.py

# Outputs: artifacts/hero_discipline_trend.{png,svg}, artifacts/discipline_results.json
```

## Data source
- Dataset: [joshfjelstul/world-cup-database](https://www.kaggle.com/datasets/joshfjelstul/world-cup-database) (CC-BY-SA 4.0)
- Coverage: 700 WC matches, 13 tournaments, 1970–2018
- Key table: `bookings.csv` (2,466 disciplinary events)

## Honesty guard
- **n = 700 matches** across 13 tournaments (32–64 per year): robust sample
- **Pre-stated hypothesis** (1986–1994 peak): REFUTED — actual peak is 2006
- **Sensitivity check**: excluding Battle of Nuremberg (Portugal v Netherlands, 16 cards), 2006 still peaks at 5.27/game
- **Single comparison**: no family of tested hypotheses; reporting objective max of time series

## Key numbers
| Year | Bookings/game | vs 2006 |
|------|--------------|---------|
| 2006 | 5.52 | — (peak) |
| 2010 | 4.22 | −23% |
| 2014 | 2.98 | −46% |
| 2018 | 3.52 | −36% |

**Campaign:** [World Cup Surprising Truths](https://flywheel.science) · Cluster: Discipline-Cards
