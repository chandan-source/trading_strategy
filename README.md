# trading_strategy
This project implements a stock trading strategy using Alpha Vantage API to fetch intraday stock data and generate trading signals based on moving averages.
pip install pandas alpha_vantage
Usage
To use the Strategy class to generate signals for a particular stock, follow these steps:

Obtain an API key from Alpha Vantage (https://www.alphavantage.co/support/#api-key)

Import the Strategy class from strategy.py:
from strategy import Strategy
Create an instance of the Strategy class with your API key:

strategy = Strategy(api_key='<your_api_key_here>')
Call the get_signals method of the Strategy instance to generate signals for a particular stock:
signals = strategy.get_signals('GOOGL')
Replace 'GOOGL' with the stock symbol for which you want to generate signals.

The get_signals method returns a pandas DataFrame with two columns: timestamp and signal. The signal column can have the values 'BUY' (when the indicator data cuts the close data upwards), 'SELL' (when the indicator data cuts the close data downwards), or 'NO_SIGNAL' (when the indicator data and close data don't cut each other).
