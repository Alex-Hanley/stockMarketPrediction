# Stock Market Prediction
Stock Market Prediction is my first personal machine learning project that uses past data to predict whether the S&P500 will rise or fall on any given day. As this is my first project, I ran into many challenges and faults that will be discussed in the conclusion tab.







# Stock Market Original Prediction
This file includes the cleaned data + my original ML model. I used Random Forest Classifier from sklearn for 2 reasons. Firstly, because of its decision tree process with randomized parameters, it is highly resistant to overfitting compared to most models. Secondly, RFC can pick up on non-linear relationships, and since the stock market is almost never linear, this is something we need. Using the last 100 columns to train the modell, we achieved a precision score of ~47%. Not good. In the next section, we will build a backtesting system to improve this number. 
