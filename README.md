
# RealTime TradeBot

RealTime TradeBot is a cryptocurrency trading bot designed to simulate real-time trading and predict future price movements using Linear Regression. The bot fetches real-time cryptocurrency price data, simulates buy/sell actions based on predicted future prices, and tracks overall performance, allowing users to visualize both price changes and trade history in real-time.


## Features

- Real-time Price Fetching: Uses CCXT library to fetch real-time price data from cryptocurrency exchanges (e.g., Binance).
- Historical Data Analysis: Collects historical price data to predict future price trends.
- Price Prediction: Implements Linear Regression to forecast future prices based on historical price trends.
- Simulated Trading: Buys and sells cryptocurrency based on predicted price movements, ensuring a dynamic and realistic simulation.
- Visualization: Real-time plotting of price data and trade signals, providing a clear and interactive graphical representation.


## How it Works

1. Historical Data Fetching: The bot fetches historical price data (by default, for the last 30 days) using the CCXT library.

2. Price Prediction:
- Uses Linear Regression to predict future prices based on the collected historical data.
- The number of future days to predict can be adjusted (default: 5 days).

3. Real-Time Data Fetching:
- Continuously fetches real-time price data for a chosen cryptocurrency trading pair (default: BTC/USDT).
- Updates every 5 seconds for a duration of 60 seconds (configurable).

4. Simulated Trading:
- The bot generates buy or sell signals based on the difference between real-time prices and predicted prices.
- Executes trades automatically based on the signal: buy when real-time price < predicted price, sell when real-time price > predicted price.

5. Visualization:
- The bot visualizes real-time price changes using a line graph.
- It updates the graph every 5 seconds, showing price trends over time.

## Libraries and Tools Used
- CCXT: Used for fetching historical and real-time cryptocurrency price data from multiple exchanges.
- Pandas: For managing and processing historical and real-time price data.
- NumPy: Used for mathematical operations, including data manipulation for the Linear Regression model.
- Matplotlib: Visualizes price changes and trade signals in real-time
- Seaborn: Enhances visualization aesthetics.
- Sklearn: Implements the Linear Regression model for price prediction.
- IPython Widgets: Provides interactive elements for dynamic real-time updates in notebooks.

