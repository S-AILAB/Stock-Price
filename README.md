# Stock Price Fetcher

This project demonstrates how to fetch and analyze stock prices using Yahoo Finance data. It utilizes the `yfinance` library to retrieve historical market data and stock information.

## Installation

To get started, you'll need to install the required Python packages. You can do this using `pip`. Run the following commands:

```bash
pip install yfinance
pip install yahoofinancials
pip install fix-yahoo-finance
pip install --upgrade yfinance
pip install Yahoo-ticker-downloader

### Usage
Import Libraries
import pandas as pd
import yfinance as yf
from yahoofinancials import YahooFinancials

#### Fetch Historical Stock Data

Retrieve historical stock data for Apple (AAPL) and Infosys (INFY.NS):-

aapl_df = yf.download('AAPL', start='2024-01-01', end='2024-07-12', progress=False)
infy_df = yf.download('INFY.NS', start='2024-01-01', end='2024-06-23', progress=False)

##### Retrieve Latest Stock Data, Stock Information and Historical Data

Fetch the most recent data, stock information and historical market data for LIC (LICI.NS):-

infy_df = yf.download('LICI.NS', progress=True)
lic = yf.Ticker("LICI.NS")
print(lic.info)
hist = lic.history(period="1mo")
print(hist)

###### Access Stock News

Access the latest news for LIC (LICI.NS):-

print(lic.news)

####### Acknowledgments

yfinance for fetching stock data.
YahooFinancials for additional financial data.
fix-yahoo-finance for fixing Yahoo Finance API issues.
