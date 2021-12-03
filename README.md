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
