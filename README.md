# RNN-LSTM-with-Cross-Validation-for-Bitcoin-Price-Prediction
Python

Bitcoin is widely used cryptocurrency for digital market. It is decentralised that means it is not own by government or any other company.Transactions are simple and easy as it doesn’t belong to any country.Records data are stored in Blockchain.Bitcoin price is variable and it is widely used so it is important to predict the price of it for making any investment.This project focuses on the accurate prediction of cryptocurrencies price using neural networks.
We’re implementing a Long Short Term Memory (LSTM) model using keras; it’s a particular type of deep learning model that is well suited to time series data (or any data with temporal/spatial/structural order e.g. movies, sentences, etc.).We have used different activation function for analysing the efficiency of the system.Instead of historical data we are using live streaming data for better accuracy.


First we get the data from the website coinmarketcap. Further data cleaning and normalization is done where the values of close price and volume ranges from -1 to 1.
Some new columns are creates i.e. price volatility (simple means difference between high and low price divided by the opening price) and price high for that day (i.e. (difference between high and close divided by difference between high and low)-1).
Randomly select the window length of the model. Also choose the best activation function for this model for better accuracy.
Now fit the close price and volume in the model. After getting the MAE (Mean absolute Error) of the training data, do similarly for the test data.
Then calculate the Mean Absolute Error and Mean Square Error for the test data. Verify the result for every activation function and choose one which shows highest accuracy.
For the second model, first apply a 10-fold cross validation on the same. Then split and train the model into 10 folds or groups and run the model for each fold. After fitting the model we calculate mae for each fold.
After calculating mae of each fold total mae (in percent) is calculated. Now we repeat the process with a different model i.e. linear regression and compare if our model is the best or not.


By comparing all the models we can conclude that cross validation in Rnn with LSTM helps in increasing the efficiency of the model for bitcoin prediction because the bitcoin data is unstable and so by using cross validation results are more enhanced as it estimate the mean of all mae and taking different test and train data every time .It maintains the consistency of data.
