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
	- input files:
		```
			[
				us_financial_news_data.csv
			]
		```
2. [Sentiment Analysis](src/02_sentiment_analysis.ipynb)
	- calculate sentiment scores (compound, negative, neutral, positive) of news title using VADER package
	- input files:
		```
			[
				us_financial_news_data.csv
			]
		```
	- output files:
		```
			[
				us_financial_news_data_with_sentiment.csv
			]
		```
3. [Data Process](src/03_data_process.ipynb)
	- concat all news sources sentiment data with S&P500 index price
	- input files:
		```
			[
				us_financial_news_data_with_sentiment.csv,
				SP500.csv
			]
		```
	- output files:
		```
			[
				wsj.csv,
				cnbc.csv,
				fortune.csv,
				reuters.csv,
				source_price.csv
			]
		```
4. [LSTM without news on S&P500](src/04_lstm_without_news_on_sp500.ipynb)
	- training lstm with only S&P500 historical data
	- input files:
		```
			[
				source_price.csv
			]
		```
	- output files:
		```
			[
				lstm_without_news_on_sp500_denormalized_prediction_all.npy
			]
		```
5. [LSTM with news on S&P500](src/05_lstm_with_news_on_sp500.ipynb)
	- training lstm with S&P500 historical data and news compound sentiment score
	- input files:
		```
			[
				source_price.csv
			]
		```
	- output files:
		```
			[
				lstm_with_news_on_sp500_denormalized_all.npy
			]
		```
6. [DP-LSTM](src/06_dp_lstm.ipynb)
	- predicting stock price using DP-LSTM method with news compound sentiment score and S&P500 historical data
	- input files:
		```
			[
				source_price.csv
			]
		```
	- output files:
		```
			[
				dp-lstm_with_news_on_sp500_denormalized_all.npy
			]
		```
7. [Plot Prediction](src/07_plot_prediction.ipynb)
	- plot all prediction result of all models
	- input files:
		```
			[
				source_price.csv,
				lstm_without_news_on_sp500_denormalized_prediction_all.npy,
				lstm_with_news_on_sp500_denormalized_all.npy,
				dp-lstm_with_news_on_sp500_denormalized_all.npy
			]
		```

#### credits

- [DP-LSTM-Differential-Privacy-inspired-LSTM-for-Stock-Prediction-Using-Financial-News](https://github.com/Xinyi6/DP-LSTM-Differential-Privacy-inspired-LSTM-for-Stock-Prediction-Using-Financial-News/tree/master)