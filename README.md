# reddit-stock-sentiment

This repository contains code for the dissertation project "Exploring the Relationship between Stock Returns and Social Media Sentiments" by Inje Kim. The research aims to explore the impact of sentiments from Reddit posts on the explanatory power of the Fama French three-factor model for seven popular stocks (AAPL, GME, MCD, MSFT, NFLX, NVDA, TSLA).

## Data Sources

* Reddit post data was collected from Pushshift and then filtered using a [simple keyword search script](https://github.com/injekim/PushshiftDumps) based on [Watchful1's script](https://github.com/Watchful1/PushshiftDumps).

* The Fama French three-factors were collected from the [Kenneth R. French - Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)

* Historic stock data was collected from Yahoo Finance using [yfinance library](https://github.com/ranaroussi/yfinance).

* Reddit subscriber counts were collected using RedditAPI.

## How to Run

If you're interested in replicating the tests, follow these steps:

1. **Setup Data**: Download `posts.csv`, `stock_index.csv`, and `subreddit_subscribers.csv` from this Kaggle link: [Reddit-Stock related posts](https://www.kaggle.com/datasets/injek0626/reddit-stock-related-posts?datasetId=3431669). Place the files in the root directory of the repository.
2. **Prepare Post Data**: Execute `prepare_posts.ipynb` to preprocess the post data and categorise them by stocks for sentiment analysis.
3. **Calculate Sentiments**: Launch `get_sentiment.ipynb` to calculate sentiment scores from the post data.
4. **Explanatory Data Analysis**: `eda.ipynb` contains explanatory data analysis (EDA) related to the research.
5. **Model & Results**: Run `model.ipynb` to perform the tests and view the results.