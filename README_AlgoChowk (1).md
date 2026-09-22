# AlgoChowk — NIFTY Event Study

This repository/notebook investigates whether a significant one-day fall in NIFTY 50 is followed by recovery over the next few trading days.

## Run
1. Open `AlgoChowk_NIFTY_Event_Study.ipynb` in Jupyter or Google Colab.
2. Run all cells.
3. The notebook downloads NIFTY 50 daily OHLC data, validates it, detects events, calculates forward returns, compares against a baseline, performs statistical and robustness checks, creates an out-of-sample split, and runs a simple event-driven backtest.

## Default assumptions
- Event: NIFTY one-day close-to-close return <= -2%.
- Entry: next trading day's Open, avoiding look-ahead bias.
- Holding periods: 3, 5 and 10 trading days.
- Transaction cost assumption: 5 bps per round trip (configurable).
- Overlapping events are skipped in the simple 5-day backtest.

## Data
NIFTY 50 historical index data is available through NSE's historical index-data resources. The notebook uses Yahoo Finance's `^NSEI` feed for convenient reproducibility; for final submission, retain/export the downloaded OHLC data and document the source and date range.

## Important
The notebook is a research tool, not investment advice. Results should be interpreted with the baseline, out-of-sample results and limitations rather than by maximizing historical return.
