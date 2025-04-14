# Quantamental-Investment-Agent-Project

## Trading Strategy

# ETF Trading Strategy Analysis

## Overview
This project explores trading strategies for two different ETFs:
1. **SPY** – Represents large-cap blue-chip stocks.
2. **QQQ** – Represents large technology companies.

We use historical data from **January 1, 2005, to January 1, 2025**, and reference risk-free rates from the **Federal Reserve Economic Data (FRED)**. The **20-year average 3-month Treasury bill rate (2005-2025) is 1.64%**, which serves as the risk-free return benchmark.

---

## SPY Strategy
We tested multiple models for SPY and found that the **classic SME (Simple Moving Average with Exponential Smoothing)** model yielded the best performance. The key parameters for this strategy were:
- **Initial Capital:** $100,000
- **Risk per Trade:** 2% (0.02)
- **Stop Loss Percentage:** 5% (0.05)

### Results:
- **Sharpe Ratio:** 0.32 (using the 1.64% risk-free rate)
- **Win Rate:** 52%
- **Maximum Drawdown:** 40.12%
- **Annualized Return:** 6.13%

---

## QQQ Strategy
For QQQ (NASDAQ ETF), we implemented a **Gaussian Channel combined with Bollinger Bands** strategy, ensuring a **minimum holding period of 5 days**. To maintain a weekly trading frequency, all trades were executed on **Mondays**.

The key parameters for this strategy were:
- **Initial Capital:** $100,000
- **Risk per Trade:** 4% (0.04)
- **Stop Loss Percentage:** 5% (0.05)

### Results:
- **Sharpe Ratio:** 0.31 (20-year period)
- **Win Rate:** 1.33%
- **Maximum Drawdown:** 5.381%
- **Annualized Return:** 2.75%

---

## Key Insights
- Implementing a **5-day minimum holding period and weekly trading** reduced overall returns and imposed stricter requirements on trading strategies.
- Despite the lower annualized returns, both strategies still outperformed the **risk-free rate (1.64%)**.
- Over the 20-year period, **Sharpe ratios remained above 0.3**, indicating a stable risk-adjusted return.

This study highlights the trade-offs between holding period constraints and trading frequency in ETF strategies, providing insights for further optimization.

