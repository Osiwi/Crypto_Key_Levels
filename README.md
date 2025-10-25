# Crypto Key Levels (10Y Support/Resistance Map)

This tool pulls long-horizon daily price data for a crypto pair (e.g. BTC/USDT from Binance, Kraken, etc.), builds rolling "fair value", "support", and "resistance" bands, and shows where today's price sits relative to those historically important levels.

## What it does
- Fetches up to ~10 years of daily OHLCV candles via `ccxt`.
- Computes:
  - 90-day rolling average price ("fair value")
  - Rolling lower/upper bands using quantiles (support/resistance zones)
  - Bull vs bear regime (price vs SMA200)
  - Annualized rolling volatility (risk)
  - Typical bull/bear run length in days
- Derives multiple key support/resistance levels from history.
- Plots:
  1. Price + average bands + key levels,
  2. A clean “live overlay” chart showing current price vs those key levels.

## How to run
```bash
python crypto_key_levels.py --symbol BTC/USDT --exchange binance --years 5
