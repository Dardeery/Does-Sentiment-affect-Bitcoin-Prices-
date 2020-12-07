# Case Study 

## Does Sentiment affect Bitcoin Prices? 
Motivation: 
As bitcoin value determined by people perception, this study is an attempt to validate whether there is a correlation between the two variables or not. 

### Data Sources: 
Twitter data:
I used sentiment analysis covers 16 Million Tweet ranging covering the time 2016-01-01 to 2019-03-29 which include bitcoin as a keyword. 
Bitcoin Data:
And for Bitcoin prices I connect to yahoo finance api to get it’s historical data volume and prices. 
### Data pre-processing: 
1. Data cleansing:
	Tokenization: and Stopword elimination :removing stop-words and special characters of the tweets ,like (@),(#), etc.
	changing the date format (timestamp to a full date).
	Adding weighted sentiment field, which means a tweet weight is increased by its impact represented in the format of (like, retweet or comment). 
	Remove natural tweets, as it doesn’t assist in providing a positive nor negative correlation with the bitcoin prices. 

1. Getting the sentiments of the tweets: 
Sentiment analysis is a system of extracting the polarity of individuals’ subjective opinions from plain normal language texts. Sentiment analysis includes characterizing opinions in text into categories, which is a decimal range of polarity,  Positive (polarity >0), Negative (polarity <0) and Neutral (polarity =0). 
I used for it TextBlob It provides a simple API for diving into common natural language processing (NLP) tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, classification, translation, and more.
Afterwards, I have taken the average polarity per day.

###  Merging the two databases: 
 
The following diagram shows the basic ETL process starting from extracting the data from twitter API and Yahoo finance, into transforming and cleaning it through sentiment analysis model until loading the data into the data model and present it. 

###  Data Visualization: 
1. output of the data is presented on tableau



### References : 
Sentiment : https://textblob.readthedocs.io/en/dev/
Karalevičius, Vytautas. (2017). Using sentiment analysis to predict interday Bitcoin price movements. The Journal of Risk Finance. 19. 00-00. 10.1108/JRF-06-2017-0092.
Twitter data : https://www.kaggle.com/alaix14/bitcoin-tweets-20160101-to-20190329
Bitcoin prices :https://finance.yahoo.com/quote/BTC-USD/
