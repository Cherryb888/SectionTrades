# SectionTrades

Process-first trading project for disciplined analysis of a small number of instruments (initial focus: TSLA, NVDA, crude oil, BTC) on day-to-swing timeframes.

## What is here

- `.claude/skills/` — eight Claude Code skills that encode the full workflow: macro read, single-instrument analysis, thesis construction, risk sizing, scalp/intraday setups, pre-trade checklist, trade journal, tilt check. See `.claude/skills/README.md` for how they fit together.
- `journal/` — append-only trade log, one file per month.
- `plan.md` — current active plan (instruments, broker, risk parameters).
- `wiki/index.html` — single-page visual reference. Open in a browser, or run `python -m http.server` from repo root and visit `/wiki/`.

## First 90 days

Paper trading only, 0.25% risk per trade, every trade (taken and rejected) logged. Review at 50 trades and at 90 days. No real size until the journal shows positive expectancy.

## What this project is not

- A signal service. The skills do not produce buy/sell calls; they produce structured analysis with an invalidation level.
- A bot. No code here trades an account. A human reads the analysis, decides, executes, and logs.
- A promise of a win rate. The target is positive expectancy and account survival, measured over n ≥ 50 trades.
