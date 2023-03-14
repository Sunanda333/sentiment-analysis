# Project 2 - Group # 4

## Predicting stock market movements using sentiment analysis as a tool

### Project Description:

In this thesis, we analysed Twitter dataset to investigate if there is any correlation between tweets and fluctuation of the stock market. We analysed a much bigger dataset compared to the studies done in the past, selecting top ten most tweeted stocks for analysis, ranging from various domains. Out of total days for which we performed our experiment, we find out that for 78.3 % of days the values are positively correlated and the average distance between stocks volume and tweets volume, on correlated days, is lower than 16%. We also performed sentiment analysis on the tweets to find correlation among the sentiment and fluctuation in the stock price. To understand the correlation between the daily sentiment about one specific stock and the performance of that stock in the markets we performed sentiment analysis on the tweets. As a supplement, we also analyzed the network structure of the dataset to understand the relation among users of the Twitter dataset.

Some [statistics](
    https://blog.hootsuite.com/twitter-statistics/) regarding Twitter:

* Twitter has 145 million monetizable daily active users.

* 30 million (or 20%) of Twitter’s daily users are American.

* 92% of the U.S. population is familiar with Twitter (even if they don’t use it).

* According to a recent survey by [Pew Research Center](https://www.pewresearch.org/fact-tank/2019/08/02/10-facts-about-americans-and-twitter/), around one-in-five U.S. adults (22%) say they use Twitter.

* Twitter stands out as one of the social media sites with the most news-focused users.

Behavioural economics tell us that people are  not rational consumers and individual behaviours and decisions are greatly affected by emotions and indeed  by the opinions of others. Twitter  sentiment  analysis  can  be  extremely  helpful  for predicting  emotions  or  opinion  on a certain  stock.  So examining  the trending mood on Twitter  and observing its relationship to the movement in stock price can help predict the future trend in the market.

### Model training and evaluation

Different machine learning techniques were used to train and evaluate models to analyze and determine the correlation between twitter sentiment and Apple stock price. 

Two approaches for analyses were used:

1. **Classification:** In this approach the twitter polarity scores were used to classify tweets into positive, negative and neutral sentiment. The adjusted closing prices of Apple stock were converted to a binary form (0 and 1), where 0 means that the value of the company stock price is less than the day before, and 1 means that the value is greater than the day before. This provided a trend for stock price movement. 

    Algorithms used for analysis:

    **Random Forest Classifier**

    Random Forest Classifier is an ensemble method, meaning that a random forest model is made up of a large number of small decision trees, called estimators, which each produce their own predictions. The random forest model combines the predictions of the estimators to produce a more accurate prediction.


    **Gradient Boosting Classifier**

    Gradient Booster algorithm builds trees one at a time, where each new tree helps to correct errors made by previously trained tree. With each tree added, the model becomes even more expressive. There are typically three parameters - number of trees, depth of trees and learning rate, and each tree built is generally shallow.

2. **Regression:** In this approach the twitter polarity scores, twitter volume and the adjusted closing prices were used to predict the future movement in Apple stock price. The adjusted closing prices data was stuctured such that previous time steps were used as input variables and the next time step as the output variable.

    Algorithms used for analysis:

    **Random Forest Regressor**

    Random Forest Regression is a supervised learning algorithm that uses ensemble learning method for regression. Ensemble learning method is a technique that combines predictions from multiple machine learning algorithms to make a more accurate prediction than a single model.


    **LSTM RNN**

    Long short-term memory (LSTM) is an artificial recurrent neural network (RNN) architecture used in the field of deep learning. LSTM networks are well-suited for making predictions based on time series data, since there can be lags of unknown duration between important events in a time series.

    **XGBoost Regressor**

    XGBoost is short for Extreme Gradient Boosting and is an efficient implementation of the gradient boosting machine learning algorithm.

### Limitations/ What could have been done differently?

1. Twitter API has limitations on the amount of data that can be accessed. Therefore, a document with Twitter information regarding Apple stock from Kaggle was used.

2. The Kaggle dataset also had limited data (Jan'16 - Aug'19) which restricted our analysis to limited number of trading days.

3. NewsAPI headlines besides Twitter could also have been used for sentiment analysis.

4. Identifying optimum hyperparameters to fine tune the model outputs.



