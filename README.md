# About
Python implementation of simple algorithmic trading strategies using Momentum and Trend following technical indicators used by traders and investors in financial markets to analyze past market data and identify potential trends or patterns in the price and volume of an asset.

# Setup

On a Macbook, if you are having issues when installing ta-lib with pip and requirements file.

Use the following commands.

```
conda create -n finance python=3
conda activate finance
brew install ta-lib
conda install -c conda-forge ta-lib # do not use: pip install ta-lib
```


Check your installation on terminal with the following commands

```
python
import talib
talib.__ta_version__
```

You should see your talib version printed !

Workaround reference link : https://github.com/TA-Lib/ta-lib-python/issues/408#issuecomment-855438491


## 1. MACD - Moving Average Convergence Divergence

This Notebook presents a comprehensive analysis of investment strategies using the performance metrics of GAFAM stocks - Google, Apple, Facebook(now Meta), Amazon, and Microsoft. The project evaluates two distinct approaches: an active strategy utilizing **Moving Average Convergence Divergence (MACD) for trading signals**, and a **passive strategy employing dollar-cost averaging (DCA) with the SPDR S&P 500 ETF Trust (SPY) as a benchmark**.

<img src="../main/images/MACD/fast_slow_ema.png">
<img src="../main/images/MACD/buy_sell_signals.png">
<img src="../main/images/MACD/bullish_bearish_signals.png">

Implementation of MACD is double-checked with Ta-Lib, a widely used open-source trading software to perform technical analysis of financial market data. (Reference : https://machinelearning-basics.com/)

<img src="../main/images/MACD/MACD_implementation.png">

The analysis spans a two-year period, with an initial investment capital of $\$100,000$, focusing on the daily allocation of $500 to understand the effectiveness of dollar-cost averaging in mitigating market volatility. The inclusion of transaction costs provides a realistic touch to the simulation, highlighting the impact of trading expenses on investment returns.

For simplicity here, we decided to use stock closing prices, however as always, these analysis can be done using opening prices or intra-day trading data as well, provided one has access to them.

Data come from Yahoo Finance API.

The evolution of portfolio values is visualized through Matplotlib graphs, illustrating the trajectories of GAFAM Portfolio stocks and its cumulative value over time.

<img src="../main/images/MACD/portfolios_evolution_overtime.png">
<img src="../main/images/MACD/portfolio_distribution.png">

We utilize a various performance metrics such as **total and annualized returns, maximum drawdown, Sharpe Ratio, Sortino Ratio, beta, and alpha** to offer a multifaceted view of the strategies' outcomes. 

<img src="../main/images/MACD/performance_metrics.png">


The findings offer insightful revelations about the benefits and limitations of active versus passive investment strategies in the context of a highly volatile market, highlighted by the tech sector's performance (here Big Tech Giants in particular). 

This notebook serves as both a strategic introduction guide and an education template for financial analysis in making informed decisions backed by quantitative data.

**Caveat : Please note that I am not a financial advisor, and this analysis should not be taken as financial advice. The study may presents potential biases inherent in historical data analysis, model assumptions or implementations errors, and readers are advised to conduct further research and seek professional advice before making investment decisions.**


More details regarding the implementation at : https://github.com/Mortiniera/algorithmic-trading-technical-indicators/blob/main/MACD/An%20Introduction%20to%20Algorithmic%20Trading%20-%20MACD.ipynb


# References
References :

- https://machinelearning-basics.com/blog/ for MACD explanations and implementation.

- https://www.investopedia.com/ for Performance metrics, backtests and all other financial instruments used