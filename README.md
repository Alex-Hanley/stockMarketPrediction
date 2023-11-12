# Stock Market Prediction
Stock Market Prediction is my first personal machine learning project that uses past data to predict whether the S&P500 will rise or fall on any given day. As this is my first project, I ran into many challenges and faults that will be discussed in the conclusion tab.

# Data Cleaning
I used yfinance to import S&P500 data and matplotlib for plotting. Cleaning the data, I removed all unnecessary information and prepped the data by shifting it left one day to create a hypothetical "tomorrow" value to predict. I only used data from 1990 onward, as to not include irrelevant and unnecessary data from before then. In the "Target" column I created, a value of 1 is shown if the price increased from the previous day and a 0 if vice versa. Now that the data is cleaned and prepped, we can begin developing our ML algorithm to predict the next day's price.

# Original Prediction
This file includes the cleaned data + my original ML model. I used Random Forest Classifier from sklearn for 2 reasons. Firstly, because of its decision tree process with randomized parameters, it is highly resistant to overfitting compared to most models. Secondly, RFC can pick up on non-linear relationships, and since the stock market is almost never linear, this is something we need. Using the last 100 columns to train the modell, we achieved a precision score of ~47%. Not good. In the next section, we will build a backtesting system to improve this number. 
