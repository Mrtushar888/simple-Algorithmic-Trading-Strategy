
# Design a simple Algorithmic Trading Strategy


A brief description of what this project does and who it's for

the project combines fetching intraday historical data, calculating an indicator, generating trading signals, and visualizing the data using a candlestick chart to implement and analyze a trading strategy for a given stock script.
## API Reference

#### Get all items from alpha_vantage

```http
 https://www.alphavantage.co/support/#api-key
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `api_key` | `string` | **Required**. 'T3CPJ71CAKFIEYI6' |





## Appendix

Any additional information goes here


## Usage/Examples

To get data from the API, simply import the library and call the object with your API key. Next, get ready for some awesome, free, realtime finance data. Your API key may also be stored in the environment variable ALPHAVANTAGE_API_KEY.

from alpha_vantage.timeseries import TimeSeries
ts = TimeSeries(key='YOUR_API_KEY')

data, meta_data = ts.get_intraday('GOOGL')
You may also get a key from rapidAPI. Use your rapidAPI key for the key variable, and set rapidapi=True

ts = TimeSeries(key='YOUR_API_KEY',rapidapi=True)
Internally there is a retries counter, that can be used to minimize connection errors (in case that the API is not able to respond in time), the default is set to 5 but can be increased or decreased whenever needed.

ts = TimeSeries(key='YOUR_API_KEY',retries='YOUR_RETRIES')
The library supports giving its results as json dictionaries (default), pandas dataframe (if installed) or csv, simply pass the parameter output_format='pandas' to change the format of the output for all the API calls in the given class. Please note that some API calls do not support the csv format (namely ForeignExchange, SectorPerformances and TechIndicators) because the API endpoint does not support the format on their calls either.

ts = TimeSeries(key='YOUR_API_KEY',output_format='pandas')
The pandas data frame given by the call, can have either a date string indexing or an integer indexing (by default the indexing is 'date'), depending on your needs, you can use both.

 # For the default date string index behavior
ts = TimeSeries(key='YOUR_API_KEY',output_format='pandas', indexing_type='date')
# For the default integer index behavior
ts = TimeSeries(key='YOUR_API_KEY',output_format='pandas', indexing_type='integer')



## Authors

- Tushar Varun(https://github.com/Mrtushar888)


## 🚀 About Me
I'm a Data Science Professional
## 🛠 Skills
Python,SQL,PowerBI,Tableau,A/B testing, Data Science, Data Analysis,Mathematics,Statistic,R,Machine Learning,Advance Excel


## Installation

Install my-project

```bash
   pip install Pandas
   pip install requests
   pip install mplfinance
   pip install alpha_vantage
```
    