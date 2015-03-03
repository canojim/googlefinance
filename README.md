# googlefinance
Python module to get stock data from Google Finance API

This module provides **no delay**, **real time** stock data in NYSE & NASDAQ.  [yahoo-finance](https://github.com/lukaszbanasiak/yahoo-finance)'s data is delayed by 15 min, but it provides apis to fetch historical day-by-day stock data.

##Install
From PyPI with pip:
	
	$pip install googlefinance

From development repo (requires git)

	$git clone https://github.com/hongtaocai/googlefinance.git
	$cd googlefinance
	$python setup.py install

##Usage example

	>>> from googlefinance import getQuotes
	>>> import json
	>>> print json.dumps(getQuotes('AAPL'), indent=2)
	[
	  {
    	"Index": "NASDAQ", 
 	    "LastTradeWithCurrency": "129.09", 
        "LastTradeDateTime": "2015-03-02T16:04:29Z", 
        "LastTradePrice": "129.09", 
        "Yield": "1.46", 
        "LastTradeTime": "4:04PM EST", 
        "LastTradeDateTimeLong": "Mar 2, 4:04PM EST", 
        "Dividend": "0.47", 
        "StockSymbol": "AAPL", 
        "ID": "22144"
      }
    ]
    >>> print json.dumps(getQuotes(['AAPL', 'GOOG']), indent=2)
    [
      {
        "Index": "NASDAQ", 
        "LastTradeWithCurrency": "129.09", 
        "LastTradeDateTime": "2015-03-02T16:04:29Z", 
        "LastTradePrice": "129.09", 
        "Yield": "1.46", 
        "LastTradeTime": "4:04PM EST", 
        "LastTradeDateTimeLong": "Mar 2, 4:04PM EST", 
        "Dividend": "0.47", 
        "StockSymbol": "AAPL", 
        "ID": "22144"
      }, 
      {
        "Index": "NASDAQ", 
        "LastTradeWithCurrency": "571.34", 
        "LastTradeDateTime": "2015-03-02T16:04:29Z", 
        "LastTradePrice": "571.34", 
        "Yield": "", 
        "LastTradeTime": "4:04PM EST", 
        "LastTradeDateTimeLong": "Mar 2, 4:04PM EST", 
        "Dividend": "", 
        "StockSymbol": "GOOG", 
        "ID": "304466804484872"
      }
    ]
