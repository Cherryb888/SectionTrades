---
name: market-analysis
description: Systematic read on a single instrument (equity, commodity, crypto) before forming a view. Invoke when the user asks "what do you think about X," "should I be long/short X," or wants a fundamental + technical read. Produces a structured brief, not a trade recommendation.
---

# Market analysis

Purpose: turn a vague "what about X" into a disciplined brief that surfaces what is known, what is priced, and what would change the view. The output is an opinion only after the process is followed, never before.

## The checklist — work through every section, skip nothing

### 1. What am I looking at
- Ticker, exchange, primary listing, relevant derivatives (options, futures)
- Market cap / open interest, average daily volume, typical bid-ask spread
- Trading hours and liquidity windows that matter for this instrument

### 2. Price and positioning (what the market already believes)
- Price now, 1d / 1w / 1m / YTD / 1y / 5y returns
- Distance from 52-week high and low (both as % — this shows mood)
- Short interest (equities), COT positioning (futures), funding rate (crypto perps)
- Implied volatility vs realized — is the option market expecting a move
- For equities: forward P/E, EV/EBITDA, PEG, vs sector median. For oil: spot vs 3m/12m futures curve (contango or backwardation). For BTC: funding, basis, ETF flows

### 3. Fundamentals (what the business or asset actually does)
- Equities: last 4 quarters of revenue, gross margin, op margin, FCF, guidance vs prints
- Oil: supply (OPEC+ quotas, US production, inventories — EIA weekly), demand (IEA/EIA forecasts), refining margins
- BTC: on-chain holder cohorts, ETF net flows, miner behavior, regulatory state

### 4. Catalysts in the next 0–90 days
- Earnings date (equities), FOMC / CPI / NFP, OPEC meetings, election/geopolitical events
- Known product launches, drug approvals, expiries, unlocks
- Tag each catalyst: bullish / bearish / unknown, and whether price already reflects it

### 5. The bear case, stated fairly
Before forming a view, write the strongest case against the position I'm drifting toward. If I can't make the other side sound reasonable, I don't understand the trade yet.

### 6. What would change my mind
Write two or three specific, observable things that, if they happened, would flip the view. If the view can't be falsified, it's a narrative, not a thesis — stop here and say so.

### 7. Output format
A brief that looks like this, in this order:

```
INSTRUMENT: <ticker> — <name>
PRICE: <last> (<1d %>, <YTD %>, <% from 52wk high>)

READ: <one sentence, neutral / bullish / bearish, with confidence low|med|high>

KEY FACTS (5 bullets max, numbers not adjectives)
•
•

CATALYSTS (next 90d)
• <date>: <event> — priced in? yes/no/partially

BEAR CASE (the strongest argument against my lean)

INVALIDATION (what would prove me wrong)
• <specific, observable>
• <specific, observable>

WHAT I DON'T KNOW (list the gaps — this section must not be empty)
```

## Rules I hold myself to

- No recommendation without the full checklist. If I'm missing data, I say which data and why it matters, not "based on general trends..."
- Numbers, not adjectives. "Up 40% YTD" beats "has been strong." "Gross margin fell from 72% to 68%" beats "margin pressure."
- Cite source and date for every number. Stale data is wrong data.
- Confidence is low by default. "Medium" requires the bear case to be weak on its own terms. "High" requires a catalyst that is specific, dated, and underpriced.
- If the user is already positioned, I give the same read I'd give a flat observer. I do not adjust the view to protect their P&L.
