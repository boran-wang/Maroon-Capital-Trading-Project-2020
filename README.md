Trading project I did as part of the Quant Cohort of Maroon Capital (Finance Club @ UChicago) in Winter 2020.

Optimized and backtested a simple pair-trading strategy between WTI Crude prices and CAD/JPY in iPython.

Intuition:\
Canada is one of the biggest exporters of oil, while Japan is one of the biggest importers of oil.\
So as oil price rises more Japanese Yen has to be sold to buy Canadian dollar.\
Thus Japanese Yen depreciates while Canadian dollar appreciates when oil prices increase.\
Hence CAD/JPY correlates positively with oil prices.\

Data:\
Hourly data of CAD/JPY prices and WTI Crude from 3/1/2019 to 3/2/2020.\
Training: before 1/1/2020\
Testing: after 1/1/2020\
p-value for cointegration test for Training Data: 0.0551\

Implementation of Strategy:\
Select Hedge Ratio to minimize Standard Deviation of Spread.\
Sell the Spread whenever it goes a certain amount above its EWMA.\
Buy the Spread whenever it goes a certain amount below its EWMA.\
Optimize Parameters: Normalizer & EWMA Lookback Period.\

Limitations of Strategy:\
Well-known strategy.\
High Standard Deviaiton of Spread.\
Low PnL even before considering transaction costs.