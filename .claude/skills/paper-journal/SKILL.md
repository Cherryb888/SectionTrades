---
name: paper-journal
description: Log every trade idea (taken and not taken) with enough structure to measure edge honestly over time. Invoke when the user enters a trade, exits a trade, wants to add a "wanted-to-take" idea, or asks "how am I actually doing." Produces append-only journal entries and periodic honest reviews.
---

# Paper trade journal

Edge is invisible in single trades. Over 50+ trades it shows up — or doesn't. Most retail traders never find out which, because they remember winners and forget losers. This skill exists to make that impossible.

## File layout

Journal lives in the repo at `journal/` and uses append-only markdown files, one per month:

```
journal/
  2026-04.md
  2026-05.md
  ...
  README.md           # methodology, rules, stats template
```

Never edit a past entry. If a mistake was made in logging, append a correction entry dated today referring to the original.

## Entry templates

### ENTRY — when a trade is taken

```
## 2026-04-23 09:14 UTC — ENTRY — #042
instrument: TSLA
direction: long
entry: 243.10
invalidation: 239.50   (risk 3.60/share)
target_1: 250.50       (RR 2.06)
target_2: 257.00       (RR 3.86)
size: 120 shares       (risked: $432 = 0.43% of $100k account)
horizon: 3 trading days
thesis: <one paragraph, copied from the trade-thesis output>
confidence: medium
emotional state at entry: calm / excited / fomo / revenge / bored — pick one honestly
```

### EXIT — when the position is closed (fully or partially)

```
## 2026-04-24 14:02 UTC — EXIT — #042
exit: 249.80           (partial, 60 shares)
pnl: +$402 (0.40% account)
reason: target_1 hit, trailing remainder to target_2 with stop at 245
thesis held up: yes / partially / no — one sentence why
```

### WANTED-TO-TAKE — ideas rejected by the checklist

```
## 2026-04-23 10:30 UTC — NOT TAKEN — #W019
instrument: NVDA
direction: long
why considered: breakout above 920 on volume
why rejected: no defined invalidation below 905; RR would be 1.2 at best
what happened after (filled in 1 week later): tagged 940 then fell to 890 — would have been stopped or small win
```

The wanted-to-take log is where overconfidence gets caught. Over time it answers: *would I have made money on the trades I wasn't disciplined enough to specify?* Usually the honest answer is no.

### REVIEW — required every 20 trades and monthly

```
## 2026-04-30 — MONTHLY REVIEW

trades taken: 18
wins: 9 / losses: 8 / scratches: 1
gross P&L: +$1,240
win rate: 53%
avg winner: +$310
avg loser: −$160
expectancy per trade: +$69
largest loss: −$340 (within rule? yes)
largest drawdown this month: −$890 (−0.9%)

what worked:
what didn't:
rules broken (be specific, no excuses):
patterns in the losses (setup, time of day, instrument, emotional state):
adjustments for next month (max 2 — more than that is over-fitting to noise):
```

## Rules I enforce

- **Log at entry, not after.** Logging a trade after it wins is not journaling, it is celebrating. Every trade is logged before it is taken or within 15 minutes of entry.
- **Log losses first.** The discipline is proven by how promptly the losers get written down.
- **No hidden trades.** Every click that moves real size is logged. A trade you didn't want to log is the trade you most need to log.
- **Emotional state is mandatory.** "Revenge," "fomo," "bored" — these words in the entry are worth more than any indicator. Clusters of losses tagged with the same state are the finding.
- **Stats only matter past n=30.** Before that, everything is noise. Do not change strategy based on 5 trades; do change it based on 50.

## What the journal is for

After 50–100 trades, the journal answers the only question that matters: *do I have an edge, or am I paying tuition?*

- Win rate × avg win > (1 − win rate) × avg loss → positive expectancy, the math works
- Otherwise → either the strategy is losing, or the execution is losing the edge the strategy has. The journal tells us which.
- Either way, no real size goes on until the data says go. That is not pessimism. That is the only path where the account is still around in year two.
