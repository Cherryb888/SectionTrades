# Active trading plan — v1 (2026-04-23)

## Account
- Size: £100
- Phase: first-20-trades evaluation sprint
- Rules: full risk and journal discipline per `.claude/skills/`

## Instruments (active)
- **TSLA** — US equity, fractional shares
- **NVDA** — US equity, fractional shares
- **BTC** — spot, fractional

## Instruments (parked)
- **Crude oil** — dropped for now. UK retail access is via leveraged CFD/spread-bet, spreads eat small-account scalps, contract sizing doesn't fit £100. Revisit when account is ≥ £2,000 and we can use /MCL-equivalent exposure responsibly.

## Risk parameters (per `risk-sizing` skill, phase 1 / paper-equivalent)
- Risk per trade: **0.5%** of current account = 50p at £100
- Max concurrent risk: **1%** of account
- Max trades per session: **5**
- Max losers per session: **2** (session ends on second)
- Daily loss limit: **1.5%** of account (£1.50 at £100) → platform closes
- Cooldown between trades: **5 minutes minimum**

## Setups (per `scalp-intraday` skill — only these)
1. Opening range break (ORB)
2. VWAP reclaim / reject
3. Failed breakout (trap)
4. News reaction (scheduled events only)

Any trade outside these four setups is not taken.

## Review trigger
- After 20 logged trades: interim review, sample-size caveats noted
- After 30–50 logged trades: meaningful review, rules may change based on journal data

## Broker
- **Trading212 Invest account** (unleveraged, commission-free, fractional shares and fractional BTC)
- Do **not** use the CFD account — leverage breaks the sizing math on a £100 stake

## Session windows
- **TSLA / NVDA**: US cash session 14:30–21:00 UK. Optionally first hour of pre-market (13:00–14:30 UK) only if spread is within tolerance that day.
- **BTC**: 24/7 in principle; prefer US open (14:30 UK) and Asia open (~01:00 UK) for cleanest setups.
- **Session definition**: one trading session = one sit-down block. Max one session per 12-hour window. 5-trades / 2-losers rule is per session and does not reset by taking a break.
- **Trader sleep/state rules stand** per `tilt-check`: no trading below 6h sleep, no trading when the last session hit its loss limit within the cooldown window.
