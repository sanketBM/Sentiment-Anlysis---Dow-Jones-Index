# Sentiment-Anlysis---Dow-Jones-Index

•	This project aims to incorporating sentiment derived from news articles into pricing models, can improve the accuracy of trading signals
•	In this Model Natural Language Processing (NLP) techniques are used to obtain significant and quantitative metrics from news articles

Abstract
From the last twenty years, the application of Internet based technologies had brought a significant impact on the Indian stock market. Use of the Internet has eliminated the barriers of brokers and geographical location because now investors can buy and sell their shares by accessing the stock market status from anywhere at any time. Before investing money, it is very important for investors to predict the stock market. In today's digital world Internet based technologies such as Cloud Computing, Big Data analytics, and Sentiment analysis have changed the way we do business. Sentiment analysis or opinion mining makes use of text mining, natural language processing (NLP), in order to identify and extract the subjective content by analyzing user's opinion, evaluation, sentiments, attitudes and emotions. In this research work importance of sentiment analysis for stock market indicators such as Sensex and Nifty has been done to predict the price of stock. Finally, we draw conclusions and provide suggestions for future work.

1.INTRODUCTION
In the finance field, stock market and its trends are extremely volatile in nature. It attracts
researchers to capture the volatility and predicting its next moves. Investors and market analysts
study the market behaviour and plan their buy or sell strategies accordingly. As stock market
produces large amount of data every day, it is very difficult for an individual to consider all the
current and past information for predicting future trend of a stock. Mainly there are two methods
for forecasting market trends. One is Technical analysis and other is Fundamental analysis.
Technical analysis considers past price and volume to predict the future trend where as 
Fundamental analysis On the other hand, Fundamental analysis of a business involves analyzing
its financial data to get some insights. The efficacy of both technical and fundamental analysis is
disputed by the efficient-market hypothesis which states that stock market prices are essentially
unpredictable.

3. METHODOLOGY
3.1. System Design
Following system design is proposed in this project to classify news articles for generating stock
trend signal.

3.1.1. News Collection
We collected Apple Inc. Company’s data for past three years, from 1 Feb 2013 to 2 April 2016.
This data includes major key events news articles of the company and also daily stock prices of
AAPL for the same time period. Daily stock prices contain six values as Open, High, Low,
Close, Adjusted Close, and Volume. For integrity throughout the project, we considered
Adjusted Close price as everyday stock price. We have collected this data from major news
aggregators such as news.google.com, reauters.com, finance.yahoo.com.

3.1.2. Pre Processing
Text data is unstructured data. So, we cannot provide raw test data to classifier as an input.
Firstly, we need to tokenize the document into words to operate on word level. Text data
contains more noisy words which are not contributing towards classification. So, we need to
drop those words. In addition, text data may contain numbers, more white spaces, tabs,
punctuation characters, stop words etc. We also need to clean data by removing all those words.
For this purpose, we created own stop-word list which specifically contains stopwords related to
finance world and also general English stop words. We built this using reference from [16]. This
stop words list contains general words including Generic, names, Date and numbers,
Geographic, Currencies.
Also, to ignore words that appear in only one or two documents, we are considering minimum
document frequency which considers words that appear in minimum three documents.
Stemming is also important to reduce redundancy in words. Using stemming process, all the
words are replaced by its original version of word. For example, the words ‘developed’,
‘development’, ‘developing’ are reduced to its stem word ‘develop’. Some of the pre-processing
is done before applying polarity detection algorithm. And some of them are applied after
applying polarity detection algorithm

3.1.3. Sentiment Detection Algorithm
For automatic sentiment detection of news articles, we are following Dictionary based approach
which uses Bag of Word technique for text mining. This method is based on the research of J.
Bean in his implementation of Twitter sentiment analysis for airline companies [6]. To build the
polarity dictionary, we need two types of words collection; i.e. positive words and negative
words. Then we can match the article’s words against both these words list and count numbers
of words appears in both the dictionaries and calculate the score of that document.
We created the polarity words dictionary using general words with positive and negative
polarity. Also addition to this, we used Finance specific words with its polarity using
McDonald’s research [16]. In this dictionary, we collected 2360 positive words and 7383
negative words.
For the news article, we are considering the string which contains headline and news body, both.
