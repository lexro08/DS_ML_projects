The service for the sale of used cars "Not beaten, not painted" is developing an application to attract new customers. In it, you can quickly find out the market value of your car. Historical data is at your disposal: technical specifications, complete sets and prices of cars. You need to build a model to determine the cost.

Important to the customer:

- prediction quality;
- prediction speed;
- training time.


# Results of the research

According to the results of preprocessing the initial data and preparing samples for training and prediction, the LGBMRegressor model proved to be the best. The target RMSE metric (below 2500) has been reached.

Best LGBMRegressor parameters: learning_rate=0.0956621333321235, max_depth=7.

**Libraries** - pandas, matplotlib, sklearn, CatBoost, lightgbm
