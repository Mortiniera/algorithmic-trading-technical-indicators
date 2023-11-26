# algorithmic-trading-technical-indicators
Python implementation of some Momentum and Trend following technical indicators used by traders and investors in financial markets to analyze past market data and identify potential trends or patterns in the price and volume of an asset.
Python implementations are double-checked and compared against Ta-lib implementations.


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

Python implementation of MACD indicators to understand their mecanism and how they can be useful for algorithmic trading using 
data from Yahoo Finance API, with Google Stock.

<img src="../main/images/MACD_plot.png">

More details regarding the implementation at : https://github.com/Mortiniera/algorithmic-trading-technical-indicators/blob/main/MACD/Moving_Average_Convergence_Divergence.ipynb



# References

Thanks to Hanane D. for explanations and undersanding regarding algorithmic trading strategies.

Reference : https://machinelearning-basics.com/blog/