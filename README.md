# Automotive Equity Return & Volatility Analysis (2021–2026)

A quantitative time-series analysis comparing historical equity performance, liquidity, volatility regimes, and cross-asset correlations for **Tesla (`TSLA`)**, **Ford (`F`)**, and **General Motors (`GM`)** from **January 1, 2021 to September 1, 2026** using split- and dividend-adjusted daily data via `yfinance`.

## Key Quantitative Findings

| Ticker | Daily Mean Return | Daily Volatility ($\sigma$) | Annualized Volatility | Sharpe Ratio ($R_f=0$) | Growth of $1 Invested | Total Return |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **TSLA** | 0.0984% | 3.73% | 59.24% | 0.42 | $1.51 | +51.26% |
| **F** | 0.0878% | 2.50% | 39.62% | 0.56 | $2.23 | +123.11% |
| **GM** | 0.0829% | 2.32% | 36.85% | 0.57 | $2.22 | +121.85% |

* **Volatility Drag:** Tesla achieved the highest arithmetic daily mean return (`0.0984%`), yet produced the lowest compounded total return (`+51.26%`) and Sharpe ratio (`0.42`) due to elevated annualized volatility (`59.24%`).
* **Cross-Asset Correlation:** Daily returns between legacy automakers Ford and GM are strongly correlated ($r = 0.74$), while Tesla shows much weaker correlation with both Ford ($r = 0.33$) and GM ($r = 0.34$).
* **Liquidity & Tail Risk:** Tesla dominates daily dollar volume (`Open × Volume`) and exhibits heavier return tails, with single-day outliers exceeding `+20%` and `-15%`.

## Tech Stack & Libraries
* **Python 3**
* `pandas` & `numpy` — time-series indexing, rolling moving averages, return & volatility modeling
* `yfinance` — automated retrieval of split- and dividend-adjusted OHLCV market data
* `matplotlib` & `mplfinance` — price/volume charts, KDE/histogram distributions, box plots, scatter matrices, and OHLC candlestick visualizations

## How to Run
```bash
pip install pandas numpy matplotlib yfinance mplfinance jupyter
jupyter notebook Automotive_Stock_Analysis_2021_2026.ipynb
