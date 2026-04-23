---
name: risk-sizing
description: Account-level risk rules — position size per trade, correlation between open positions, drawdown tripwires, leverage limits. Invoke before any trade is entered, and whenever the user asks "how much should I put on." Enforces the math that keeps an account alive long enough for edge (if it exists) to show up.
---

# Risk and position sizing

The first job is not making money. It is not going broke. An edge of any size compounds if the account survives; a great edge with bad sizing dies in the first drawdown.

## The core sizing formula

```
size = (account × risk_per_trade_pct) / (entry − invalidation)
```

Where:
- `account` = current liquid account value (not peak, not starting)
- `risk_per_trade_pct` = fixed fraction set in advance (see below)
- `entry − invalidation` = risk per unit in the instrument's currency

Size is computed *from* the stop, never the other way around. If the stop is wide, size is small. Do not widen the stop to fit a bigger size — that inverts the whole discipline.

## Default risk levels

| Phase | Risk per trade | Max concurrent risk | Notes |
|---|---|---|---|
| First 3 months / paper trading | 0.25% | 1.0% | Learning phase, real or simulated |
| After 50+ logged trades with documented positive expectancy | 0.5% | 2.0% | Only if the journal proves an edge |
| Experienced, consistent, year+ of data | 1.0% | 3.0% | Upper bound for retail day trading |

Never above 1% per trade on a discretionary day-trading book, regardless of confidence. "High conviction" is where overconfidence lives.

## Correlation — the hidden leverage

Three longs on Tesla, Nvidia, and oil-in-a-war-scenario are **not three trades**. They are one macro risk-on bet expressed three ways. Rule:

- Treat positions with correlation > 0.6 as a single aggregated position for risk purposes
- Tesla + Nvidia + QQQ longs = one tech/growth exposure, sized together
- Long oil + short USD + long defense names in a war scenario = one geopolitics bet
- BTC + high-beta tech longs often correlate > 0.7 in risk-off — not independent

Before adding a position, ask: *if my macro view is wrong, how many of my open positions lose at the same time?* That number × per-trade risk is the real drawdown in the bad scenario.

## Drawdown tripwires

These are not suggestions. They are rules written now, when calm, to be obeyed later, when not.

- **−5% from peak equity**: review every losing trade in the journal. Is there a pattern? Size halves until back within 3% of peak.
- **−10% from peak equity**: stop trading for 48 hours. Full journal review. No new trades until a written note identifies what broke.
- **−15% from peak equity**: stop trading for 2 weeks minimum. The strategy or the operator is impaired — probably both. Return to paper trading until the journal shows consistency again.
- **−25% from peak equity**: the strategy is not working. Stop. Do not re-enter until a substantively different approach is documented and paper-traded.

## Leverage

- Default leverage: 1x. Cash or unlevered futures-equivalent.
- Leverage only enters the picture after the journal proves edge on an unlevered book over 100+ trades.
- Even then, leverage on day trades stays ≤ 3x notional, and position risk is still capped at the % rules above — leverage does not expand risk per trade, it just allows finer position sizing.
- Crypto perps: funding is a cost. Pay it consciously, not by accident.

## Per-instrument size caps

No single name is more than 15% of account notional, regardless of what the risk math says. Single-name blowup risk (fraud, trading halt, gap through stop) is not in the stop-loss calculation.

For oil futures specifically: contract size is large. One /CL contract = 1000 barrels. A $1 move = $1000. A stop 50 cents away on a 10k account is 5% of account per contract — already over the limit. Micro contracts (/MCL) exist for a reason; use them until account size makes full contracts proportionate.

## The pre-trade size check (one-line version)

Before pressing the button, say out loud:
*"If this stops out, I lose <currency>, which is <%>of my account, and that is within my rule."*

If either number is a surprise, the trade is not ready.
