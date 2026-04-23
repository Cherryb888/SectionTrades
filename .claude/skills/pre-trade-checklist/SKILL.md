---
name: pre-trade-checklist
description: The final 60-second gate before a trade is entered. Invoke immediately before execution, after market-analysis, trade-thesis, and risk-sizing have already been run. Binary pass/fail on each line — any fail means no trade.
---

# Pre-trade checklist

The previous skills produced the trade. This skill is the gate that stops the trade from being entered while something is still wrong. It is short on purpose. Every item is a yes/no. A single no means stand down.

## The checklist

Read each line and answer out loud (or in writing). Do not mentally skim.

### Thesis
- [ ] I can state the thesis in one sentence without using the words *should*, *eventually*, or *obviously*
- [ ] I can state the single most likely reason this trade loses, and I accept it

### Price and levels
- [ ] The entry price/trigger is specific and is where I am actually entering (not 2% away, hoping)
- [ ] The invalidation is a price, written down, and I will act on it without renegotiating
- [ ] The first target is a price, not a feeling; R:R is ≥ 1.5

### Size and risk
- [ ] Size was computed from (account × risk%) / (entry − invalidation), not from gut
- [ ] Risk on this trade is within my per-trade % rule
- [ ] Adding this trade keeps my total concurrent risk within my concurrent-risk rule (correlation included — see risk-sizing)
- [ ] I am not above my drawdown tripwire. If I am, I am not trading today, period.

### State
- [ ] I am not entering because I just lost on another trade and want it back
- [ ] I am not entering because I am bored and want something to do
- [ ] I am not entering because everyone on the feed is talking about it
- [ ] I slept. I ate. I am not drunk, high, or running on two hours.

### Mechanics
- [ ] The stop order is entered with the position, not "I'll watch it"
- [ ] I know the spread, the slippage I expect, and the fee on this instrument
- [ ] For a leveraged or options trade: I know the margin required and the liquidation level
- [ ] For a news-driven trade: I know the exact scheduled event, the time, and whether my stop respects the expected move

### Journal
- [ ] Entry has been logged with thesis, levels, size, horizon, and honest emotional state

## What to do on any fail

- Thesis fail → go back to the `trade-thesis` skill. The trade is not ready.
- Size or risk fail → shrink size until the math passes, or pass on the trade. Do not move the stop.
- State fail → close the platform for 30 minutes minimum. Go outside. This is the cheapest loss you will ever take.
- Mechanics fail → fix the mechanics. This is a 2-minute problem, not a reason to skip the gate.

## The 60-second version (for a trader who already knows the rules)

1. One-sentence thesis, no weasel words
2. Entry, stop, target — three numbers on screen
3. Risk = X% of account, concurrent risk within rule
4. Not tilted, not fomo, not revenging
5. Stop and journal in place
6. Go.

If that takes more than a minute once the habit is built, the chart wasn't ready or the trader wasn't.
