---
name: scalp-intraday
description: Short-timeframe trading (1m–15m candles, minutes-to-hours hold) with defined setups, session windows, and stricter-than-swing risk rules. Invoke when the user wants to day-trade or scalp TSLA, NVDA, crude futures, or BTC. Rejects "see what happens" entries; only pre-defined setups are taken.
---

# Scalp and intraday

Short-timeframe trading looks like more opportunity; it is actually the same edge (or lack of it) applied to more noise, with fees and slippage scaled up proportionally. The only way it works is: fewer, better setups, smaller size, harder stops on the day, mechanical execution.

Most of the people who tell you they scalp for a living either don't, or sit at desks with rebates, co-located order routing, and level-2 depth you don't have. That is not a reason to never trade intraday — it is a reason to be disciplined about *which* intraday trades.

## Session windows only

Most intraday noise lives in the middle of the session. Trade the windows where liquidity and information are concentrated; avoid the rest.

| Window (US time) | Instruments | Why |
|---|---|---|
| 09:30–10:30 ET | TSLA, NVDA | Opening range, gap resolution, highest volume of the day |
| 14:00–16:00 ET | TSLA, NVDA | Afternoon trend, close dynamics, FOMC days |
| 02:00–04:00 ET + US open | /CL crude | EIA report days (Wed 10:30 ET), European open liquidity |
| Fixed high-volume hours | BTC | First 2h of US open, Asia open (20:00 ET) |

Outside these windows: smaller size, tighter setups, or don't trade.

**Hard avoid:** first 90 seconds after FOMC / CPI / NFP print (spreads are garbage), the last 2 minutes before cash close (MOC imbalance), and the 11:30–13:30 ET "lunch" chop for equities.

## The only setups I trade intraday

If the chart in front of me does not match one of these, I am not in a trade, I am in a gamble. Screenshot or annotate the setup at entry and attach to the journal entry.

### 1. Opening range break (ORB)
- First 15- or 30-minute high and low marked
- Trade: break of the range *with volume above the 20-period average*, hold above/below on the next candle
- Invalidation: back inside the range
- Target: 1× range width (minimum), 2× stretch target

### 2. VWAP reclaim / reject
- Price has been on one side of session VWAP, tests it from the other side
- Trade: reclaim with a higher low (for longs), or reject with a lower high (for shorts), on the 5m
- Invalidation: 0.5–1.0 ATR (5m) through VWAP the other way
- Target: prior session high/low or next visible liquidity level

### 3. Failed breakout (trap)
- Price breaks a prior day high/low by a small distance, stalls, fails back inside within 2 candles
- Trade: short the failure (or long the failed breakdown), entry on re-entry of the range
- Invalidation: new high/low beyond the failure wick
- Target: opposite side of the range

### 4. News reaction fade or follow
- Only on known scheduled events (earnings for equities, EIA for oil, FOMC for everything)
- Wait for the first full 5m candle to close after the print
- Trade follow-through on volume *or* fade of an extreme wick with confirmation
- Never chase the spike in real time

That's the whole list. "The chart looks like it wants to go up" is not on the list. If a setup I want to add to this list shows itself repeatedly in the journal, I add it deliberately after review, not on the fly.

## Risk rules — tighter than swing

| Rule | Swing | Scalp/intraday |
|---|---|---|
| Risk per trade | 0.25–1.0% | **0.15–0.5%** |
| Max concurrent risk | 1–3% | **1%** |
| Max trades per session | no hard limit | **5** |
| Max *losers* per session | n/a | **2 — session ends** |
| Min time between trades | none | **5 minutes** |
| Fees + slippage into R:R | yes | **yes, explicitly — add 2× spread to entry cost** |
| Daily loss limit | drawdown tripwires | **1.5% of account — platform closes** |

The "max 2 losers, session ends" rule is non-negotiable. It is the single rule that separates a bad day from a blown week.

## Fees and spread math

On a scalp, if the target is 30 cents and the spread is 4 cents plus 2 cents slippage, a "1.5:1 trade" is actually closer to 1:1 after costs. The R:R calculation *must* use post-cost numbers:

```
effective_entry = entry + (spread/2) + expected_slippage
effective_exit  = target − (spread/2) − expected_slippage
effective_stop  = stop   + (spread/2) + expected_slippage   (stops slip through)
effective_RR    = (effective_exit − effective_entry) / (effective_entry − effective_stop)
```

If effective R:R falls below 1.3, the trade is not worth taking no matter how clean the setup looks on a replay.

## Execution mechanics

- **Stop order always entered with the position.** Never "mental stop" on a 1m chart. The whole point of intraday is speed, and a manual exit is always late.
- **Bracket orders** (entry + stop + target) where the broker supports them.
- **One-click trading only after 50 logged paper scalps.** Hot keys on an unproven account turn small mistakes into fast disasters.
- **Instrument sizing reminder (oil specifically):** /CL is $1000 per $1 move. /MCL is $100. On accounts under $50k, scalping full /CL contracts violates risk rules instantly. Use /MCL.

## Mandatory per-trade log fields (intraday)

In addition to the standard journal fields, every scalp logs:

```
setup: ORB / VWAP / trap / news — one of the four, or the trade should not have been taken
session_window: <which window>
spread_at_entry:
expected_slippage:
effective_RR:
time_in_trade:
```

Over 50 scalps, this data tells us which setup actually pays, which session wastes our time, and whether costs are eating the edge. That is the only way to improve intraday — measurement, not intuition.

## What this skill refuses

- Taking a trade that doesn't match one of the four setups, regardless of how "obvious" the move looks
- Raising per-trade risk % beyond 0.5% on an unproven account
- Taking a third loss in a session
- Trading in the "hard avoid" windows
- Chasing price after it has already moved more than 1× the planned risk without a fresh setup
- Entering without a pre-placed stop

## What it does do

- Give you a short, defined menu of setups to hunt
- Keep the session from becoming 40 clicks and a tired trader
- Make the costs of fast trading visible, so they stop being invisible drag
- Produce data, in the journal, that after 50 trades will say either "this setup pays" or "it doesn't, stop taking it"

"Quicker trades" done this way have a shot. Quicker trades done by loosening the rules are the fastest way to find out the account wasn't ready.
