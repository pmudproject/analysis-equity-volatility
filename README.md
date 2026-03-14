# Equity Return and Volatility Modeling

This project analyzes return dynamics and volatility behavior of major technology stocks implementing financial econometric methods in Python.

## Objective

The goal of this project is to examine whether equity returns exhibit predictable structure and to analyze how volatility evolves over time across large-cap technology companies.

## Data

Daily price data for the following stocks were obtained using the Yahoo Finance API:

* Apple (AAPL)
* Microsoft (MSFT)
* Nvidia (NVDA)
* Amazon (AMZN)
* The S&P 500 Index

Sample period: 2020–2026. (used time-frame of only six years instead of usual ten to record volatility better)

## Methods

### CAPM Regression

Estimated the Capital Asset Pricing Model:

R_stock = α + β R_market + ε

to measure systematic market exposure.

### Rolling Beta

Computed 60-day rolling betas to analyze time-varying systematic risk.

### ARIMA Modeling

Used ARIMA models to examine whether past returns contain predictive information about future returns. Realised after running the model that most people do not use ARIMA to examine said stocks, then moved to GARCH (as explained below)

### GARCH Volatility Modeling

Estimated GARCH(1,1) models to capture volatility clustering and persistence in stock returns.

### Volatility Persistence Comparison

Compared volatility persistence across major technology stocks using:

α + β

which measures duration of shocks.

## Key Findings

* Equity returns show minimal predictability, consistent with the efficient market hypothesis.
* Volatility exhibits strong clustering over time.
* Volatility shocks are highly persistent across major tech stocks.
* Apple and Microsoft exhibit the highest persistence (α+β ≈ 0.96), while Amazon shows comparatively faster volatility mean reversion.

## Technologies Used

* Python
* Pandas
* NumPy
* Statsmodels
* ARCH package
* Matplotlib

## Visualizations

The project includes plots of:

* Apple daily returns
* GARCH estimated volatility
* Cross-stock volatility persistence

These illustrate key stylized facts of financial markets including heavy tails and volatility clustering.
![Volatility Persistence](volatility_persistence.png)


