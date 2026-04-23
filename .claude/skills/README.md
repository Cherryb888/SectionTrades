# SectionTrades — Claude Code trading skills

Seven skills that encode process, not prediction. They make analysis rigorous and risk bounded. They do not create edge. Edge, if it exists, shows up in the journal over dozens of trades.

## The skills and how they fit together

```
                     +---------------------+
                     |    macro-read       |   world events / big picture
                     +----------+----------+
                                |
                     +----------v----------+
                     |  market-analysis    |   read on a single instrument
                     +----------+----------+
                                |
                     +----------v----------+
                     |   trade-thesis      |   view -> testable trade
                     +----------+----------+
                                |
                     +----------v----------+
                     |   risk-sizing       |   how many units, given the stop
                     +----------+----------+
                                |
                     +----------v----------+
                     | pre-trade-checklist |   final 60-second gate
                     +----------+----------+
                                |
                          (enter trade)
                                |
                     +----------v----------+
                     |   paper-journal     |   log entry, exit, review
                     +---------------------+

     (running alongside at all times)
     +----------------+
     |   tilt-check   |  catches emotional state before damage
     +----------------+
```

## Workflow

1. `macro-read` when a trade idea starts with a world-events thesis (oil + Middle East, Fed cycle, geopolitics).
2. `market-analysis` to turn a vague "what about TSLA" into a structured brief with bear case and invalidation.
3. `trade-thesis` to convert the view into an entry / stop / target / size / horizon.
4. `risk-sizing` to size the position off the stop, respecting per-trade and concurrent-risk limits and correlation between open positions.
5. `pre-trade-checklist` as the last gate. Any fail stops the trade.
6. `paper-journal` at entry, at exit, and at periodic reviews — the only source of truth about whether we have edge.
7. `tilt-check` runs in the background. Any emotional or operational red flag takes priority over every other skill.

## What these skills deliberately refuse

- Win-rate promises. The 70% target is not a target these skills try to hit. The target is survival plus positive expectancy over n ≥ 50 trades.
- Real-money discretion. Claude does not take an account. These skills analyze, structure, and gate — the human enters.
- Validating narratives that can't be falsified. "Eventually", "suppressed", "smart money is quietly buying" — flagged and rejected every time.
- Concentration dressed as diversification. Tesla + Nvidia + long oil in a war scenario is one bet, and the risk skill treats it as one.

## First 90 days

1. Paper trade only. Real broker platform simulator or spreadsheet, not mental accounting.
2. Risk 0.25% per trade, max 1% concurrent.
3. Log every trade and every rejected idea.
4. At 50 logged trades and at 90 days, full review. If expectancy is positive and rules held, consider moving to 0.5% per trade on a small real account. If not, either the strategy or the execution is wrong, and the journal will show which.

No real size until the data earns it. That is the whole game.
