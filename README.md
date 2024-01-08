# Household Electric Power Consumption forecasting
The dataset is obtained from UCI Machine Learning Repository. It contains 9 features and 2,075,259 measurements of electric power consumption of a house located in Sceaux (7km of Paris, France), spanned from December 2006 to November 2010, total 47 months.

[Data Source](https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption)

### Problem Statement
The increasing demand for electricity, particularly during peak consumption periods such as hot summer days when air conditioners are in heavy use, poses significant challenges for energy providers. Balancing the supply and demand of electricity under these conditions is complex and crucial. Inaccurate predictions of electricity consumption can strain energy grids, leading to blackouts, brownouts, and increased operational costs. Furthermore, this demand volatility makes it difficult to integrate renewable energy sources efficiently.

### Goal and motivation
The goal is to develop a robust time series regression models to forecast household electric power consumption. This will help us in determining how much energy is likely to be consumed in the future. With this, the energy providers can better plan the integration of renewable energy sources into the grid and reduce reliance on non-renewable and greenhouse gas-emitting sources such as fossil fuels. This will help in reducing the environmental damage, improving reliability, and supporting sustainable development.

### Models developed
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
