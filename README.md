# Stock Market Prediction
Stock Market Prediction is my first personal machine learning project that uses past data to predict whether the S&P500 will rise or fall on any given day. As this is my first project, I ran into many challenges and faults that will be discussed in the conclusion tab.

# Data Cleaning
I used yfinance to import S&P500 data and matplotlib for plotting. Cleaning the data, I removed all unnecessary information and prepped the data by shifting it left one day to create a hypothetical "tomorrow" value to predict. I only used data from 1990 onward, as to not include irrelevant and unnecessary data from before then. In the "Target" column I created, a value of 1 is shown if the price increased from the previous day and a 0 if vice versa. Now that the data is cleaned and prepped, we can begin developing our ML algorithm to predict the next day's price.

# Original Prediction
This file includes the cleaned data + my original ML model. I used Random Forest Classifier from sklearn for 2 reasons. Firstly, because of its decision tree process with randomized parameters, it is highly resistant to overfitting compared to most models. Secondly, RFC can pick up on non-linear relationships, and since the stock market is almost never linear, this is something we need. Using the last 100 columns to train the modell, we achieved a precision score of ~47%. Not good. In the next section, we will build a backtesting system to improve this number. 

# Back Testing
Needing to improve on the poor number from the first prediction, I implemented some fixes. I first broadened the range of dates we used instead of just the last 100 days. I used increments of 2, 5, 60 (1 months), 250 (year) and 1000 (4 years) days, calulcated the ratio between todays closing price and the closing price of that long ago, and averging them. Doing this allows the model to see "hey, is the market in a significant downturn or upturn?" because then, we can better predict a turn in the future. Secondly, I altered some of the parameters and implemented predict_proba to get an actual probably estimate of the market increasing or decreasing tomorrow. With these fixes alone, I improved the model to ~57%, which is pretty good for predicting a relatively unpredictable market.

# Conclusion
Though this was my first experience with ML, I learned so much and actually loved doing it. In this, I gained many skills in the process:

  # 1. Data Collection and Cleaning:
    Acquiring large sums of data
    Cleaning, processing, and handling data with inconsistencies, missing values, etc.
  # 2. Presenting relevant data using multiple Python libraries:
     Used Matplotlib and Pandas to create visually appealing and relevant graphs.
  # 3. Model Selection:
    Choosing appropriate machine learning models for time series forecasting.
    Experimenting with regression models, decision trees, ensemble methods, and           neural networks.
  # 4. Backtesting and Validation:
    Implementing backtesting techniques to assess the performance of the model on         historical data.
    Validating the model on out-of-sample data to gauge its real-world predictive         ability.
  # 5. Real World Application:
    Gaining insights into the challenges of implementing machine learning models in       real trading scenarios.
    Understanding the impact of transaction costs, slippage, and market liquidity on      model performance.

I will definitely be doing more ML and AI projects in the future. I think this was a great start!

# Thanks
I would like to thank @Dataquest on YouTube for his video "https://www.youtube.com/watch?v=1O_BenficgE&t=149s" and source code that helped with the creation and implementation of this model. 
  
