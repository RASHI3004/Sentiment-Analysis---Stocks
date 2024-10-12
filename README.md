# Sentiment-Analysis---Stocks
This repo contains my solutions to CapX Business Analyst Intern problem statement

This repository contains a Python-based solution for analyzing and predicting stock movements using social media sentiment analysis. The project focuses on extracting data from Telegram channels, performing sentiment analysis, and correlating social media discussions with stock price movements.

This project aims to analyze social media discussions, especially from Telegram channels, to detect sentiment trends and their correlation with stock price movements. By analyzing these discussions, we aim to provide insights that can help in predicting potential buy/sell signals for specific stocks based on social media sentiment.

## Data Sources:
This analysis primarily uses data scraped from Telegram channels using the Telethon API. In addition to Telegram data, the notebook can be extended to include stock price data sourced from Yahoo Finance (via the yfinance library).

## Platforms for Data Collection:
Telegram: Using the Telethon library, messages are scraped from specified Telegram channels that discuss stock market trends, predictions, or specific stocks.

Yahoo Finance: Historical stock price data is fetched for various companies like Tesla, Apple, Amazon, etc.

## Requirements:
To run this notebook, you will need the following Python libraries:

telethon: To scrape messages from Telegram.

pandas: For data manipulation and analysis.

matplotlib and seaborn: For data visualization.

vaderSentiment: For sentiment analysis.

yfinance: To get stock data.

wordcloud: For visualizing topic modeling results.

plotly: (Optional) For interactive graphs.

Install the necessary dependencies using the following command:

```pip install telethon pandas matplotlib seaborn vaderSentiment yfinance wordcloud plotly```


#### Data Scraping:

The notebook uses the Telethon API to scrape Telegram messages from selected channels or groups discussing stock market trends.

#### Data Preprocessing:

Text data is cleaned, and preprocessed, and unnecessary elements like noise, symbols, or stopwords are removed.

#### Sentiment Analysis:
Sentiment scores (positive/negative/neutral) are calculated using the VADER Sentiment Analyzer to gauge the mood around specific stocks.

#### Stock Price Data:

Stock price data is fetched using the yfinance library, which is then plotted alongside the sentiment scores.

#### Visualization:

Sentiment trends, stock price movements, and correlations between them are visualized using both matplotlib and seaborn.

#### Topic Modeling:

Latent Dirichlet Allocation (LDA) is used to extract topics from social media discussions, with word clouds generated for better topic interpretation.

## Usage:

#### Clone the repository:

```git clone <repo_url>```

#### Run the Jupyter Notebook:

Open the Sentiment Analysis .ipynb notebook and follow the instructions to run each section.

Ensure you have your Telegram API ID and Hash to log in to Telegram for scraping messages.

#### Customize the stock list:

You can modify the list of tracked stocks by changing the stocks list variable in the notebook. 

#### Plot sentiment and stock data:

The notebook generates plots of sentiment trends and stock price movements and allows you to visualize correlations between them.

## Findings and Insights:

#### Stock Sentiment Trends:

Sentiment analysis on Telegram messages shows that Tesla and Amazon experience significant fluctuations in sentiment. These fluctuations often correlate with stock price changes.

#### Buy/Sell Signals:

Negative sentiment spikes have shown a noticeable correlation with stock price drops, particularly for Tesla, suggesting potential sell signals for traders.

#### Topic Modeling:

Topic modeling identified key themes in social media discussions. Topics related to earnings reports and new product launches tend to trigger positive sentiment spikes.

## Future Improvements

#### Cross-Platform Data:

Extend the data scraping to include other platforms like Reddit (e.g., r/wallstreetbets) and Twitter to obtain a more comprehensive dataset.

Advanced Sentiment Analysis:
Incorporate more sophisticated sentiment analysis techniques, such as using pre-trained models like BERT, to capture more nuanced sentiments in discussions.

Real-Time Monitoring:
Implement a real-time monitoring system that tracks social media sentiment and generates alerts for significant changes in sentiment and potential stock price movements.
