# Recovery of gold from ore

It is necessary to prepare a prototype of a machine learning model for the "Digit". The company develops solutions for the efficient operation of industrial enterprises.

The model should predict the recovery rate of gold from gold-bearing ore. We use data with extraction and purification parameters.

The model will help optimize production so as not to launch an enterprise with unprofitable characteristics.

We need to:

1. Prepare the data;
2. Conduct a research analysis of the data;
3. Build and train a model.

# Results of the research

According to the results of the study, it can be seen that
The proportion of gold at each stage of purification becomes higher, therefore this processing technology is effective.
The random forest model in regression proved to be the best.
The final sMAPE on the test sample was 9.184776942388709, which is 0.02 less than in DummyRegressor.

**Libraries** - pandas, matplotlib, sklearn, LinearRegression, DecisionTreeRegressor, RandomForestRegressor, GridSearchCV
