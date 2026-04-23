# Trading journal

Append-only. One file per month, named `YYYY-MM.md`. Never edit past entries — append a correction entry dated today referring to the original.

Entry types: `ENTRY`, `EXIT`, `NOT TAKEN`, `REVIEW`. Templates in `.claude/skills/paper-journal/SKILL.md`.

## The only stats that matter

After n ≥ 30 trades:

```
win_rate       = wins / (wins + losses)
avg_winner     = mean(winning trades P&L)
avg_loser      = mean(losing trades P&L, as a negative)
expectancy     = win_rate * avg_winner + (1 - win_rate) * avg_loser
                 -> must be positive, and positive by enough to survive fees/slippage
profit_factor  = sum(winners) / abs(sum(losers))   -> must be > 1.3 to be meaningful
max_drawdown   = worst peak-to-trough in %         -> within tripwire rules
```

Below n = 30, numbers are noise and do not drive strategy changes.
