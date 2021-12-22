# Problem Statement:
As a Data Scientist I have been hired by Coinbase to find if and when there are seasonal patterns in the crypto market to create a predictive model for clients to use on the trading platform. 


# Executive Summary
### I.Data Collection
   In order to successfully create a predictive model for classifying subreddit posts, there are several steps in my methodology. First, I imported data from a kaggle data set of crypto price data between 2018-2021 with observations by the minute. Since this data set was larger than any I have ever dealt with, I had to face the challenge of splitting each crypto up into seperate data frames and fitting models individually. The folder containing the dataset totaled at 2.8 gigabytes. 
### II.Data Cleaning and EDA
   Next I imported the data for cleaning and EDA. To clean I made sure to drop any null values. There were hundreds of thousands of null values because the data set was intentionally using a missing data set for a competition in which a predictive model would need to find the 15 minute changes in the price data. I also made sure to change the column containing the asset id number, and replace the values with the associated names of the crypto currencies. I then split the data up by cryptocurrency. I also generated dataframes that resampled the original data to make hourly,daily,and weekly data. Once this was done I had a total of 36 smaller dataframes, which I used to create data visualization and some to model on. 
### III.Preprocessing, Models, and Evaluation
Once the data was spilt up I was able to start modelling. The baseline model I used was the seasonality model that included shifting the data by the number of seasonal periods by timeframe. This was difficult to do quickly, but I was able to split the data up and fit models. I decided to use a SARIMA model because I am testing for seasonality and SARIMA uses autoregression to test for it. I tried to fit on hourly,daily,and weekly iterations, but I ran into servaral issues. One issue was the fact that some values were appearing as null, and would not allow me to drop them or adjust the data in order foor the model to work. Since it is time series data, the sequential index needs to be in a straightforward time period for each value. I learned the model would not take anything else. Additionally, I had run into the issue of my model showing RMSE of 0 for certain cryptocurrencies. It is likely due to the fact that some crypto prices were below 1 dollar and the models do not work well with values that low. The last issue I ran into was the fact that the models could not even iterate a single time on the daily and hourly data, but it worked with the weekly data. Once I got the model working I used RMSE to measure the accuracy of the predictions. I did not adjust the hyperparamaters other than to change the expected seasonal period for each respective time period. In my case weeks had a value of 52 since there are 52 weeks in a year. 
### IV. Conclusions
After running many models with different parameters I was able to find some that worked better than others on predicting price. The SARIMA models only were able to run with the weekly timeframe. Hourly and daily time frames were incredibly sluggish and could not even make 1 iteration of the model for over and hour. The best model out of all of the cryptocurrencies was the weekly Cardano closing price data, which had a baseline RMSE of 2.0, beaten by the model with a 1.0. Seasonality in crypto is incredibly rare, given how volatile the markets are. The results were not conclusive of seasonal patterns in the cryptocurrency market and it will always have unpredictability. 

