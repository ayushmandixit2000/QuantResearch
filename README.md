# QuantResearch

The code in the Jupyter notebook is part of a Quantitative Research Lab assignment, and it demonstrates a methodical approach to discovering potential trading ideas based on historical financial data. The workflow of the code can be broadly described in the following steps:

## Importing Libraries: 
Essential Python libraries for data manipulation, analysis, and visualization are imported, such as yfinance, pandas, numpy, and matplotlib.pyplot. Warnings are suppressed for a cleaner output.

## Data Collection: 
Using the yfinance library, historical data for the TLT ETF (iShares 20+ Year Treasury Bond ETF) is downloaded from Yahoo Finance. The time period for data collection spans from December 31, 2002, to January 1, 2023. The data is stored in a pandas DataFrame for further analysis.

## Data Visualization: 
The notebook visualizes the closing price and the adjusted close price of TLT over time using line plots. The adjusted close price accounts for stock splits and dividends, reflecting the price an investor would receive from trading.

## Log vs. Simple Returns: 
It defines functions to calculate both simple and logarithmic returns. It then calculates the log returns for TLT and plots the cumulative sum of these returns over time to visualize the compound growth.

## Exploring Effects Based on Time of Month: 
The code investigates the 'end-of-month' effect by grouping data based on the day of the month and analyzing average log returns for each day. This part of the analysis is intended to reveal any patterns or anomalies associated with specific days of the month.

## Developing a Trading Strategy: 
The code outlines a basic trading rule by grouping the data by months and calculating the sum of log returns for the first and last five days of each month. It posits a trading strategy where an investor would be long (buying) in the last five days and short (selling) in the first five days of the month.

## Backtesting the Strategy: 
A function is created to generalize the trading strategy across all months in the dataset. It applies this function to each month and aggregates the results to analyze the overall performance of the strategy.

## Visualizing Strategy Performance: 
The notebook includes a bar chart to visualize the monthly returns and a line plot to show the cumulative performance of the trading strategy over time. It discusses periods where the strategy did well or poorly.

## Discussion of Missing Elements in the Backtest: 
It brings up limitations and considerations that are not accounted for in the analysis, such as transaction costs, slippage, market impact, capital limitations, and data biases.

## Risk Premia Hypothesis Testing: 
It tests the hypothesis whether higher returns at the end of the month could be attributed to higher risks (risk premia) by examining the absolute mean log returns and discussing their implications.

## Extending the Analysis to Other Assets: 
The notebook generalizes several functions used in the analysis to make them reusable for other financial assets. It demonstrates this by downloading and processing data for the SPY ETF (SPDR S&P 500 ETF Trust) and applying the same end-of-month trading strategy analysis to it.

## Further Exploration: 
Finally, the notebook encourages users to use the provided functions and the workflow to explore the data and the end-of-month effect further for different assets or hypotheses.

This notebook serves as a guide for conducting quantitative finance research with Python, illustrating how to work with financial data APIs, perform time series analysis, develop and test trading strategies, and visualize data-driven insights.
