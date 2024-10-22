# BTC Futures Data for Systemic Backtesting

This repository contains various BTC Futures datasets formatted for use in systemic backtesting models. The data includes a variety of metrics across different time intervals, facilitating comprehensive analysis and strategy testing for BTC Futures contracts.

## Data Overview

The dataset is designed to help traders and developers backtest trading strategies using historical data of BTC Futures. The core data points include:

- **Open Interest (OI)**
- **Sum of Open Interest Value**
- **Close Price (OHLC Data)**

Additionally, the data is available in various intervals such as 5-minute, 4-hour, and more, making it suitable for high-frequency and medium-term backtesting.

### Main Files:

1. **BTC Oldata-4h-interval**: Contains 4-hour interval data with fields for `open interest`, `sumOpenInterestValue`, and `close`.
   
2. **BTC Oidata (01-06-2024 - 01-07-2024)**: A collection of open interest data for BTC Futures from June 1, 2024, to July 1, 2024, broken down in various time intervals.

3. **BTC Price (5min interval)**: High-frequency price data of BTC Futures with 5-minute interval granularity, including `open`, `high`, `low`, and `close` (OHLC) data for backtesting short-term strategies.

4. **BTC Funding**: Funding rate data relevant for analyzing trends in futures markets and its potential impact on price movements.

### Key Fields:

- `symbol`: BTCUSDT, denoting Bitcoin against USDT pair.
- `openInterest`: Reflects the total number of outstanding futures contracts.
- `sumOpenInterestValue`: Cumulative value of the open interest contracts.
- `close`: The closing price of the BTC Futures at the specified interval.
- `timestamp`: Unix timestamp in milliseconds.

## Usage

The data in this repository is useful for:

1. **Backtesting**: Use the historical data to test trading strategies, assess risk management techniques, and optimize trade executions.
2. **Analysis of Open Interest**: Open interest can indicate momentum and provide insights into the market direction.
3. **Funding Rate Analysis**: Correlate funding rates with price movements to assess potential liquidation points.
4. **Systematic Trading Models**: Build and test systematic strategies using multiple data sources and various metrics (price, OI, funding, etc.).

### Example Code for Data Loading

```python
import json

# Load BTC Futures data
with open('path_to_data_file.json', 'r') as file:
    btc_data = json.load(file)

# Example of accessing a specific data point
print(btc_data[0]['symbol'])  # Output: BTCUSDT
print(btc_data[0]['sumOpenInterest'])  # Output: Total open interest value
