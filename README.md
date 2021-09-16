# Project-2
Mike & Jess
## Project Proposal
Our project is to predict Cryptocurrency prices. We will use sentiment from Twitter API and NewsApi sources to determine the effect on Bitcoin and Litecoin prices. We will use a Dual Moving Average Crossover Trading Signal using historical prices to determine whether they will be good investments.

## Finding Data
Gathered data from two sources to pull historical prices for two Cryptocurrencies.

- Yahoo Finance API (YFinance): pulled all available historical prices Litecoin (LTC)

- Coingecko API: pulled all available historical Bitcoing (BTC) prices

### **Scope of Data:**
- BTC: historical daily closing prices dating back to April 2013
- LTC: historical daily closing prices dating back to August 1992

## **Libraries Used**

- Nltk library
- Nltk vader lexicon
- Sentiment Intensity Analyzer
- OS library
- DotENV Variable
- Pandas Library
- Numpy Library
- [Yahoo Finance API](https://pypi.org/project/yahoo-finance/) (No Key Needed)
- [CoinGeckoAPI](https://github.com/man-c/pycoingecko) (No Key Needed)
- [NewsAPI](https://newsapi.org/docs)(API Key Needed)
- [Tweepy Twitter API](https://developer.twitter.com/en/docs/twitter-api/tools-and-libraries)(API Key & developer account needed)
- Path Library
- HV Plot Library
- HV Plot Pandas Library
- Markdown library
- Mathplotlib inline Library
- Spacy library en_core_web_sm
- Tweepy Library
- Pycountry Library
- json Library
- pprint Library

## **Analysis Notebooks**
Our data collection, cleaning, and analysis are contained in the following notebooks:

### **Data_Prep.ipynb (base environment)** 
- Imported historical stock prices for Litecoin (LTC) into Pandas dataframes using the Yahoo Finance API, and exported the historical prices into a csv file.
- Imported Bitcoin (BTC) historical prices into Pandas dataframe using the CoinGeckoAPI and exported the historical prices into a csv file.
- Imported tweets from the Tweepy API and used pandas and pprint to pull the data and export to a csv file for a few of the days.

### **crypto_sentiment.ipynb (base environment)**
- Imported the newsapi to pull all of the news articles for Bitcoin & Litecoin.
- Used Natural Language Processing to determine the positive, negative, and neutral scores for the news articles
- Used 2 n-grams to come up with the top 10 words for each coin.
- Used Word Clouds to summarize the news for each coin.
- Used Name Entity Recognition model and used spacy to visualize the tags
- Imported the tweepy API to pull the recent 1,000 tweets relating to Bitcoin and Litecoin

### **btc_vader_sentiment.ipynb**
- Used the vader lexicon sentiment Intensity analyzer library
- Downloaded news articles for Bitcoin and Litecoin using the newsapi api. 
- Created a Facebook Libra sentiment score dataframe and listed out the stats.
- Downloaded sentiment score to csv.

### **ltc_vader_sentiment.ipynb**
- Used the vader lexicon sentiment Intensity analyzer library
- Downloaded news articles for Bitcoin and Litecoin using the newsapi api. 
- Created a Facebook Libra sentiment score dataframe and listed out the stats.
- Downloaded sentiment score to csv.

### **SentimentAnalysis-Bitcoin.ipynb**
 - Used Tweepy Twitter API to use Tweets to determine sentiment.

### **SentimentAnalysis-Litecoin.ipynb**
 - Used Tweepy Twitter API to use Tweets to determine sentiment.

### **BTC_trading_dashboard.ipynb (pyvizenv)**
- Imported CSV files from above notebook into Pandas dataframe.
- Generated a dual moving average crossover trading signal.
- Plot the entry and exit points of the dual moving average crossover trading strategy.
- Backtest the trading strategy.
- Plot the entry and exit points of the trading strategy and backtest results
- Prepared the portfolio evaluation metricx dataframe
- Calculate and assign the portfolio evaluation metrics
- Preparted Trade Evaluation metrics dataframe
- Generated Trade Evaluation metrices
- Created HVPlot line charts for both the SMA50, SMA100, and Metrics
- Created HVPlot tables
- Created a trading dashboard with hvplot

### ** btc_stock_predictor_closing.ipynb (pyvizenv)**
- Imported numpy random and tensorflow random libraries.
- Imported the sentiment csv file from the btc_vader_sentiment
- Imported the Bitcoin historical prices.
- Joined the two datasets together.
- Predicted closing prices using a 10 day window size.
- Use 70% of the data for training and the remaineder for testing
- Use the MinMaxScaler to scale data between 0 and 1.
- Build and Train the LSTM RNN
- Show Model Performance

### ** ltc_stock_predictor_closing.ipynb (pyvizenv)**
- Imported numpy random and tensorflow random libraries.
- Imported the sentiment csv file from the btc_vader_sentiment
- Imported the Bitcoin historical prices.
- Joined the two datasets together.
- Predicted closing prices using a 10 day window size.
- Use 70% of the data for training and the remaineder for testing
- Use the MinMaxScaler to scale data between 0 and 1.
- Build and Train the LSTM RNN
- Show Model Performance

### ** btc_stock_predictor_closing (pyvizenv)**
- Imported numpy, pandas, hvplot, numpy.random, & tensorflow random libraries.
- imported the sentiment from the Vader sentiment notebook
- Imported the historical prices and indexed by date.
- Joined the two dataframes.
- Trained and Tested the combined dataset with the window_data function.
- Split the data with a 70/30 split for the training and testing datasets.
- Used the MinMaxScaler to scale the data.
- Built the LSTM model.
- Predicted the next days price using the last 10 and ploted out the results.

### ** ltc_stock_predictor_closing (pyvizenv)**
- Imported numpy, pandas, hvplot, numpy.random, & tensorflow random libraries.
- imported the sentiment from the Vader sentiment notebook
- Imported the historical prices and indexed by date.
- Joined the two dataframes.
- Trained and Tested the combined dataset with the window_data function.
- Split the data with a 70/30 split for the training and testing datasets.
- Used the MinMaxScaler to scale the data.
- Built the LSTM model.
- Predicted the next days price using the last 10 and ploted out the results.
