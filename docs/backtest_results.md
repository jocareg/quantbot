# Backtest Results — 60 Days (March 17 – May 16, 2026)

**Configuration:** Walk-Forward + Monte Carlo | 5 strategies | 18 symbols | Alpaca 5-min bars

---

## Summary

| Metric | Value |
|---|---|
| Period | 2026-03-17 → 2026-05-16 |
| Trading days | 43 |
| Total signals | 1,500 |
| Win Rate | 31.8% |
| Profit Factor | 1.08 |
| Portfolio ρ vs SPY | **+0.032** (target: < 0.15) |

---

## By Strategy

| Strategy | Trades | Win Rate | Profit Factor | PnL pts |
|---|---|---|---|---|
| GAP_AND_GO | 660 | 35.7% | 1.12 | +41.6 |
| VWAP | 735 | 28.2% | 1.04 | +13.9 |
| EMA_TREND | 84 | 35.7% | 1.10 | +5.5 |
| ORB | 22 | 22.7% | 1.10 | +1.6 |

---

## By Symbol (Tier 1 Universe)

| Symbol | Trades | Win Rate | Profit Factor | Avg Win | Avg Loss |
|---|---|---|---|---|---|
| LABU | 45 | 35.6% | **1.70** | $1.87 | -$0.70 |
| MSFT | 84 | 35.7% | 1.23 | $2.55 | -$1.27 |
| AMD | 98 | 30.6% | 1.30 | $3.28 | -$1.17 |
| AMZN | 90 | 37.8% | 1.28 | $1.58 | -$0.77 |
| GOOGL | 86 | 33.7% | 1.14 | $2.18 | -$1.02 |
| AAPL | 97 | 35.1% | 1.14 | $1.70 | -$0.86 |
| NVDA | 84 | 33.3% | 1.11 | $1.52 | -$0.71 |
| META | 88 | 33.0% | 1.08 | $4.07 | -$2.00 |
| TQQQ | 98 | 30.6% | 1.01 | $0.60 | -$0.28 |
| RIOT | 85 | 34.1% | 1.06 | $0.26 | -$0.13 |
| MSTR | 84 | 33.3% | 1.02 | $1.77 | -$0.88 |
| SMCI | 77 | 31.2% | 1.19 | $0.41 | -$0.17 |
| SOXL | 82 | 34.1% | 1.00 | $1.28 | -$0.68 |

---

## Correlation vs SPY (ρ)

Portfolio-level ρ = **+0.032** — near-zero market correlation achieved.

| Symbol | ρ vs SPY | Classification |
|---|---|---|
| TQQQ | −0.225 | Alpha (inverse) |
| MSTR | −0.268 | Alpha (inverse) |
| AMD | −0.176 | Alpha |
| NVDA | −0.180 | Alpha |
| MSFT | −0.066 | Alpha |
| AMZN | +0.076 | Alpha |
| LABU | +0.082 | Alpha |
| COIN | +0.128 | Marginal |
| RIOT | +0.147 | Marginal |
| META | +0.159 | Marginal |
| SOXL | +0.185 | Marginal |
| GOOGL | +0.257 | Correlated |
| AAPL | +0.341 | Correlated |

---

## Tier Classification (updated 2026-05-16)

### Tier 1 — Active universe (PF ≥ 1.00, N ≥ 45 trades)
NVDA · AMD · AMZN · GOOGL · MSFT · AAPL · META · TQQQ · SOXL · LABU · MSTR · RIOT · SMCI

### Tier 3 — Excluded (PF < 0.85, N ≥ 70 trades)

| Symbol | Trades | PF | Reason |
|---|---|---|---|
| MARA | 73 | 0.71 | Wide spreads, erratic movement |
| PLTR | 89 | 0.82 | Strong trend breaks mean reversion |
| TSLA | 80 | 0.81 | High volatility destroys ATR stops |
| COIN | 87 | 0.90 | Crypto vol incompatible with VWAP |
| IONQ | 73 | 0.90 | Low liquidity outside catalyst days |

*Tier 3 assets are re-evaluated monthly. Promotion to Tier 2 requires PF > 0.90 over 30+ new trading days.*

---

## Methodology Notes

- **Day quality filter:** Only simulates signals on days where the asset would pass the live scanner (relative volume ≥ 1.2×, ATR% ≥ 0.5%). Eliminates low-activity noise.
- **Fill assumption:** Bar-close price. No commissions (paper trading). Monte Carlo adds 0–15 bps slippage and 85–100% fill rates stochastically.
- **Statistical caveat:** With N < 100 trades per symbol, profit factor estimates carry ±0.15 confidence bands. Results are directional, not definitive.
