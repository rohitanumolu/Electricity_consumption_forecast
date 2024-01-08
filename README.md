# Household Electric Power Consumption forecasting
The dataset is obtained from UCI Machine Learning Repository. It contains 9 features and 2,075,259 measurements of electric power consumption of a house located in Sceaux (7km of Paris, France), spanned from December 2006 to November 2010, total 47 months.

[Data Source](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)

### Problem Statement
The increasing demand for electricity, particularly during peak consumption periods such as hot summer days when air conditioners are in heavy use, poses significant challenges for energy providers. Balancing the supply and demand of electricity under these conditions is complex and crucial. Inaccurate predictions of electricity consumption can strain energy grids, leading to blackouts, brownouts, and increased operational costs. Furthermore, this demand volatility makes it difficult to integrate renewable energy sources efficiently.

### Goal and motivation
The goal is to develop a robust time series regression models to forecast household electric power consumption. This will help us in determining how much energy is likely to be consumed in the future. With this, the energy providers can better plan the integration of renewable energy sources into the grid and reduce reliance on non-renewable and greenhouse gas-emitting sources such as fossil fuels. This will help in reducing the environmental damage, improving reliability, and supporting sustainable development.

### Models developed
The data was sampled to hourly from minute level keeping in mind the computation power. This can be found [here](data/hourly.csv)
1. ARIMA
2. SARIMA
3. TBATS
4. Prophet

### Results
| Model| RMSE | MAE |
| -----| ---- | --- |
| ARIMA | 358.99 | 279.34 |
| SARIMA | 319.87 |215.56 |
| TBATS | 302.08 | 211.44 |
| Prophet | 285.22 | 183.5 |

### Conclusions
1. ARIMA fails to capture any seasonal information and predicts a straight line with some fluctuation.
2. SARIMA, has caught daily seasonality pretty well but cannot capture higher seasonality (yearly in this case).
3. TBATs captures multiple seasonality well, but has extremely high execution time and computation power needed. 
4. Prophet model is quick and grasps multiple seasonality details the best in comparison to other models. Hence, best model in our exploration.
5. Adding exogenous variable like temperature, humidity, etc. to Prophet would give much lower RMSE and MAE values leading to better predictions. 