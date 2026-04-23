---
name: trade-thesis
description: Convert a market view into a specific, testable trade with entry, invalidation, target, sizing, and time horizon. Invoke after market-analysis when the user says "so should I buy" or "let's take this trade." Refuses to produce a trade from a narrative that can't be falsified.
---

# Trade thesis

A view is not a trade. A trade is a view with a price at which it is wrong, a price at which it is right, a size that survives being wrong, and a clock.

## The eight required fields — if any is missing, no trade

1. **Instrument** — exact ticker, expiry if derivative
2. **Direction** — long, short, or structure (spread, options)
3. **Entry** — a specific price or a specific trigger (e.g. "break and hold above 185 on 1h close")
4. **Invalidation** — the price at which the thesis is wrong and the position is cut. Not "I'll see how I feel." A number.
5. **Target(s)** — price(s) at which I take profit, partial or full
6. **Risk per unit** — entry minus invalidation, in currency
7. **Size** — units such that max loss = the pre-agreed % of account (see risk-sizing skill)
8. **Time horizon** — how long I give the thesis to work before I cut for being wrong on time, not just price

## The thesis paragraph

Before filling in the fields, write 3–5 sentences in plain language:

- What do I believe will happen
- Why — what specifically will cause it
- Over what window
- What would prove me wrong
- Why the market hasn't already priced this in (if I can't answer this, I probably don't have an edge; I have a story)

## Reward to risk — the floor

- Minimum acceptable R:R on any trade: 1.5:1. Prefer 2:1 or better.
- R:R below 1.5 means I need a win rate above the realistic ceiling to be profitable. Pass.
- Calculation: (target − entry) / (entry − invalidation). Use the *first* target, not the dream target.

## Falsifiability check — the hard gate

Before the trade is accepted, both must be true:

1. The invalidation is a price or a dated event, not a feeling
2. There is at least one observable outcome in the time horizon that would make me say "the thesis was wrong" — not "we just need more time"

If either fails, the trade is rejected as a narrative. Common narrative traps to catch:
- "It's being suppressed / manipulated" — unfalsifiable by construction
- "It has to go up eventually" — no clock, can't be wrong
- "Smart money is accumulating" — who, at what price, sourced how
- "The charts are setting up" — setups are necessary, not sufficient

## Output format

```
TRADE: <long/short> <instrument>
THESIS (3–5 sentences):

ENTRY: <price or trigger>
INVALIDATION: <price> — risk per unit: <currency>
TARGET 1: <price> — R:R <x.x>:1
TARGET 2 (optional): <price> — R:R <x.x>:1
SIZE: <units> (risks <% of account> = <currency>)
HORIZON: <days/weeks> — revisit on <date> if neither entry nor invalidation hit

WHY NOT PRICED IN:
WHAT WOULD MAKE ME FLAT EARLY: (news, correlation break, vol regime change)
```

## Rules

- I write the invalidation *before* I write the target. Risk first, greed second.
- I do not move the invalidation after entry to avoid being stopped. That is a losing habit with a friendly name ("giving it room").
- Adding to losers is allowed only if it was specified in the plan at entry. Not in the moment.
- If I want to take a trade that fails this checklist, I do not take it. I write it in the paper journal as a "wanted to take" and move on. Over time, that list is information.
