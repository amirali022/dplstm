### DP-LSTM Differential Privacy inspired LSTM for Stock Prediction Using Financial News

#### Implementation of article (https://arxiv.org/pdf/1912.10806.pdf)

#### Requirements

- Python 3.8
- Jupyter notebook

#### Libraries

- numpy
- pandas
- sklearn
- nltk ( + vader_lexicon )
- tensorflow
- matplotlib

#### Notebooks

1. [Browse Data and Features](src/01_browse_data_and_features.ipynb)
	- examine and analysis input data
	- examine some features such as tf-idf & bow
2. [Sentiment Analysis](src/02_sentiment_analysis.ipynb)
	- calculate sentiment scores (compound, negative, neutral, positive) of news title using VADER package
3. [Data Process](src/03_data_process.ipynb)
	- concat all news sources sentiment data with S&P500 index price
4. [LSTM without news on S&P500](src/04_lstm_without_news_on_sp500.ipynb)
	- training lstm with only S&P500 historical data
5. [LSTM with news on S&P500](src/05_lstm_with_news_on_sp500.ipynb)
	- training lstm with S&P historical data and news compound sentiment score