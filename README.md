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

## Usage
Import Libraries
import pandas as pd
import yfinance as yf
from yahoofinancials import YahooFinancials

## Fetch Historical Stock Data

Retrieve historical stock data for Apple (AAPL) and Infosys (INFY.NS):-

aapl_df = yf.download('AAPL', start='2024-01-01', end='2024-07-12', progress=False)
infy_df = yf.download('INFY.NS', start='2024-01-01', end='2024-06-23', progress=False)

## Retrieve Latest Stock Data, Stock Information and Historical Data

Fetch the most recent data, stock information and historical market data for LIC (LICI.NS):-

infy_df = yf.download('LICI.NS', progress=True)
lic = yf.Ticker("LICI.NS")
print(lic.info)
hist = lic.history(period="1mo")
print(hist)

## Access Stock News

Access the latest news for LIC (LICI.NS):-

print(lic.news)


Sure! Here’s a README.md file for your project. You can copy the following text and save it as README.md in your project directory:

markdown
Copy code
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
Usage
Here's a brief overview of how to use the code provided in this project.

Import Libraries

python
Copy code
import pandas as pd
import yfinance as yf
from yahoofinancials import YahooFinancials
Fetch Historical Stock Data

Retrieve historical stock data for Apple (AAPL) and Infosys (INFY.NS):

python
Copy code
aapl_df = yf.download('AAPL', start='2024-01-01', end='2024-07-12', progress=False)
infy_df = yf.download('INFY.NS', start='2024-01-01', end='2024-06-23', progress=False)
Retrieve Latest Stock Data

Fetch the most recent data for LIC (LICI.NS):

python
Copy code
infy_df = yf.download('LICI.NS', progress=True)
Get Stock Information and Historical Data

Retrieve stock information and historical market data for LIC (LICI.NS):

python
Copy code
lic = yf.Ticker("LICI.NS")
print(lic.info)
hist = lic.history(period="1mo")
print(hist)
Access Stock News

Access the latest news for LIC (LICI.NS):

python
Copy code
print(lic.news)
Fetch Data for Multiple Tickers

Retrieve data for multiple tickers:

python
Copy code
tickers = yf.Tickers('msft aapl goog')
print(tickers.tickers['MSFT'].info)
print(tickers.tickers['AAPL'].history(period="1mo"))
print(tickers.tickers['GOOG'].actions)
Download Data for Multiple Symbols

Download data for multiple symbols like SPY and AAPL:

python
Copy code
import yfinance as yf
data = yf.download("SPY AAPL", period="1mo")
print(data.head())
Example Output
After running the above code snippets, you can expect to see:

Historical stock data in a DataFrame format.
Detailed stock information, including market data and news.
Historical data for specified periods.
License
This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

yfinance for fetching stock data.
YahooFinancials for additional financial data.
fix-yahoo-finance for fixing Yahoo Finance API issues.