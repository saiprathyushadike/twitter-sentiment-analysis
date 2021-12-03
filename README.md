# twitter_sentiment_analysis
I applied sentiment analysis on twitter data using texthero and textblob and used xgb as our base regressor with bagging in pipeline with minmax scaler and passes pipeline through multi output regressor to obtain the given rmse score of 16.7 which was ranked 6th in datadash competition of fischer jordan model development round.

# PROBLEM STATEMENT:

 

Twitter text data has always proved to be a crucial information source for sentiment analysis. Companies use this text data for various operational decisions and analysis such as predicting social media impact, analysing customer reviews and automating feedback. One such case is the analysis of tweet data to determine the social media presence and following.

 

The Problem Statement involves developing an algorithm which will compare the performance of top 93 companies in handling their customer base on twitter over a certain period of time.

 

Create a model to calculate the rank of the company for the next 3 consecutive days.
Here the rank is calculated based on % change of the number of followers in the last 24 hours.

 

Let f(n) be the number of followers on nth day
% change in followers= {f(n) − f(n − 1)} * 100/f(n − 1)

 

Eg. If the given date is 23rd October, 2021.
Based on the inputs of this particular day the Model needs to predict the ranks of all the companies for 24th, 25th and 26th October, 2021.

Data Description:

 

| Sr No. | Column Name | Description |
| --- | --- | --- |
| 1 | name | It consists of company label for the top 93 companies | 
| 2  | date | Date on which the tweets from the company were created. | 
| 3  | tweets | It is a stringified list of tweet data tweeted by the company. (consisting of the tweet text, tweet created_at, tweet likes and the tweet retweets) | 
| 4 | count_tweets | Number of tweets tweeted by that company on a particular day. | 
| 5 | avg_tweet_likes | Average tweet likes for all tweets on a particular day. | 
| 6 | avg_tweet_retweets | Average tweet retweets for all tweets on a particular day. | 
| 7 | chatter | It is a stringified list of tweet data tweeted about the company by any other user. (consisting of the tweet text, tweet created_at, tweet likes and the tweet retweets) | 
| 8 | followers | Follower count of the company on a particular day. | 
| 9 | following | Following count of the company on a particular day. | 
| 10 | change | absolute change in followers = {f(n) − f(n − 1)}/f(n − 1), where f(n) is the number of followers on nth day | 
| 11 | rank | The rank of the company based on the change in the number of followers for a particular day. | 
| 12 | 	rank on the following day (dpv1) | 	The rank of the company for the next day from the given date. ( Dependent Variable - 1 ) | 
| 13 | 	rank 2 days later (dpv2)	 | The rank of the company 2 days later from the given date. (Dependent Variable - 2) | 
| 14	| rank 3 days later (dpv3)	| The rank of the company 3 days later from the given date. (Dependent Variable - 3) | 

# Note:
Please avoid using the company_name and the date as a feature for training the model as it won't be provided in the test dataset.
