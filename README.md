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

1. browse_data_and_features
	- examine and analysis input data
	- examine some features such as tf-idf & bow
2. sentiment_analysis
	- calculate sentiment scores (compound, negative, neutral, positive) of news title using VADER package
3. data_process
	- concat all news sources sentiment data with S&P500 index price
4. lstm_without_news_on_sp500
	- training lstm with only S&P500 historical data
