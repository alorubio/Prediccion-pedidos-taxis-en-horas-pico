# Predicting Taxi Orders During Peak Hours

Sweet Lift Taxi has collected historical data on taxi orders at airports. To attract more drivers during peak hours, we need to predict the number of taxi orders for the next hour. Build a model for this prediction.

The RECM metric on the test set should not exceed 48.

### The project structure is based on the following steps:
1. Data download and resampling for one hour.
2. Data analysis.
3. Training different models with different hyperparameters. The test sample should be 10% of the initial dataset.
4. Data testing using the test sample, and a conclusion is provided.

### Analysis
During the analysis, it was observed that the records tend to increase over time. This same situation is seen in the trend, which is observed to be slightly upward. However, in the seasonality section, nothing concrete can be defined since no information is clearly observed with all the data. In the residuals, it can be seen that the mean remains at 0, although it has some peaks at certain times. However, the peaks do not clearly indicate anything, that is, there may be events that clarify whether they are due to a trend or seasonality, so there is no stationarity.

When analyzing the extract of days, we had the opportunity to visualize in the seasonality graph, if we compare the results from 6:00 to 00:00, it is quite similar, and the residues remain linear.

### Tests and Conclusions
Tests were performed for each of the trained models, and it was concluded that the most suitable model for the application would be CatBoostRegressor. Although all models performed below the metric proposed in the project description, the CatBoostRegressor model yields the smallest RECM error for the test set and also a low error for the training set, making it the most suitable model for use in this taxi ordering project.

**Explore the details in the [complete project](https://github.com/alorubio/Prediccion-pedidos-taxis-en-horas-pico/blob/d743a93b202b592f95990dad237eaca28c8e069a/Proyecto%20Sprint15%20(1).ipynb).**
