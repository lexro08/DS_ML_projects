#  Forecasting taxi orders

The company "Chetenkoe taxi" collected historical data on taxi orders at airports. To attract more drivers during peak load, you need to predict the number of taxi orders for the next hour. Build a model for such a prediction.

The value of the *RMSE* metric in the test sample should be no more than 48.

You need to:

1. Download the data and resample it one hour at a time.
2. Analyze the data.
3. Train different models with different hyperparameters. Make a test sample of 10% of the original data.
4. Check the data on the test sample and draw conclusions.

# Results of the research

Basing on the previously provided data on taxi orders , we can arrive at the conclusion:

1) Taking into account the fact that the dataset was resampled for 1 hour and aggregated by the amount of orders, we see a trend towards an increase in the number of orders in the period from March to the end of August.

2) Taking into account the prepared data, as well as the analyzed regression analysis models, the LGBMRegressor model with the following parameters proved to be the most successful ({'boosting_type': 'gbdt', 'max_depth': 6}). On the test sample, the RMSE target metric value of 42.06 was achieved with a target threshold of 48, which is consistent with the project conditions.

**Libraries** - pandas, seaborn, matplotlib, TimeSeriesSplit, sklearn, LinearRegression, RandomForestRegressor, CatBoostRegressor, LGBMRegressor, GridSearchCV
