---
name: macro-read
description: Structured process for macro / geopolitical questions (oil and Middle East, rates, FX, crypto flows, elections). Invoke when the user asks "what does X mean for Y" or presents a thesis built on world events. Forces sourcing, priced-in analysis, and a falsifiability gate so narratives don't masquerade as trades.
---

# Macro and geopolitics read

Macro is where stories feel smartest and lose the most money. A compelling narrative about oil, war, or dirty money is not an edge — by the time it is compelling to a retail reader, it has usually been priced by desks paid to price it weeks ago. The job here is to separate the parts of the story that are new, the parts that are priced, and the parts that are unfalsifiable.

## The five-step read

### 1. State the claim in one sentence
Before any analysis, write the user's thesis in a single neutral sentence. Example: *"Prolonged Strait of Hormuz disruption plus Iran conflict will cause a sharp spike in oil prices in the UK over the coming weeks."*

If it takes a paragraph to state, it is more than one claim. Break it into claims and run this process on each. Package deals hide the weak parts.

### 2. Map the claim onto observable data
For each claim, list what would be visible in public data if it were true *right now*:

- Oil spike coming: backwardation in the Brent curve, rising IV on crude options, widening physical spreads, tanker rates (Baltic Dirty Tanker Index), inventory draws in EIA/IEA data, refined product cracks
- Money-flowing-to-BTC: ETF net inflows, stablecoin supply growth, exchange reserve changes, funding rates, BTC/gold ratio
- War escalation: shipping insurance (war-risk premiums for Hormuz transits), re-routing data, oil in transit vs lifted

If the claim has no observable tell, it cannot be traded — it can only be hoped for. Note that and stop.

### 3. What is already priced
For each observable from step 2, compare current levels to:
- 30-day average
- 1-year range
- Levels seen during prior analogous events (2019 tanker attacks, 2020 Qasem Soleimani, 2022 Russia invasion, 2023 Red Sea)

If the observables are already at or above historical crisis levels, the market has priced the scenario. The trade from here requires something *more* than the current situation — not just the current situation continuing. Say that explicitly.

### 4. The steelman of the other side
Write the strongest version of why the thesis is wrong, using current data:

- Global spare capacity (Saudi, UAE) and SPR levels
- US shale response function and current rig counts
- Demand side: China growth, EU recession risk, EV penetration
- Diplomatic off-ramps that are cheap for both sides

If after writing the steelman the original thesis still looks strong, note specifically *why* — what does the thesis see that the steelman misses.

### 5. Falsifiability — the hard gate

State two or three specific, dated outcomes that would prove the thesis wrong:

- "Brent does not close above $X within 60 days"
- "Hormuz transit volumes recover to Y mbpd by Z date"
- "BTC spot ETF net inflows do not exceed $W over Q period"

If the thesis cannot be falsified by any observable outcome in any time window, it is a belief, not a thesis, and must not be sized. Common unfalsifiable macro traps:

- **"Eventually"** — no clock, so always defensible. Flag and reject.
- **"Suppressed / manipulated"** — price staying flat becomes evidence for, not against. Flag and reject.
- **"Smart money is quietly positioning"** — unsourceable, unfalsifiable. Flag and reject.
- **"Once this breaks, it goes parabolic"** — conditional on an unspecified trigger. Tighten the trigger to a specific observable or reject.

## Sourcing rules

- Every macro claim with a number attached needs a source and a date. Bloomberg headline without a date is not a source.
- Primary data over commentary: EIA, IEA, OPEC monthly reports, BIS, IMF, central bank statements, company filings. Pundits are for flavor, not evidence.
- Twitter / X is signal about *what people are talking about*, not evidence about *what is true*. Use accordingly.
- If a claim depends on a single source, the confidence drops by one level automatically.

## Output format

```
CLAIM: <one-sentence neutral restatement>

OBSERVABLES (what would show this is happening, and current reading):
• <metric> — current: <value> — vs 30d avg: <delta> — vs analogous crisis: <context>
• ...

ALREADY PRICED: <what portion of the thesis the market has absorbed>
STILL UNDERPRICED (if anything): <specific>

STEELMAN (strongest case against):

FALSIFIABLE BY:
• <specific, dated outcome>
• <specific, dated outcome>

CONFIDENCE: low / medium / high
IF TRADEABLE — WHICH INSTRUMENT EXPRESSES IT BEST AND WHY:
IF NOT TRADEABLE — WHY NOT (and what would change that):
```

## Rules I enforce

- A good macro read often ends with *"interesting view, not tradeable yet."* That is a correct outcome, not a failure.
- Geopolitics on a 24/7 short-candle day-trade timeframe is mostly noise interrupted by headline shocks. Macro views belong on position trades with days-to-weeks horizons, not on 5-minute candles.
- Narratives I already agree with get the hardest steelman. Agreement is a signal to look harder, not to relax.
