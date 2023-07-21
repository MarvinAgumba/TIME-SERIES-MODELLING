# <p>PREDICTING COUNTRY'S GDP USING MACHINE LEARNING ALGORITHMS<p>

This repository shall host my final phase 5 project where we shall be analyzing & forecasting GDP trends (Case study Kenya - Finance Bill Reaction).\
Kenyan Parliament recently, on the 26th of June 2023, passed to law the contentious Finance Bill 2023 proposing a raft of tax policy measures that aim to yield additional revenue and explore more effective measures to enhance the Country's revenue collection.\
The Government feels the ratio of tax revenue as a percentage of Gross Domestic Product (GDP) being well below acceptable levels to enable spur economic growth & reduce the cost of living in the long term. (***According to the World Bank, tax revenues above 15% of a country’s GDP are a key ingredient for economic growth and, ultimately, poverty reduction***)

## <p>BUSINESS UNDERSTANDING<p>

**This project shall aim to analyze the Country's historical GDP trends and forecast future GDP growth. The analysis shall assist provide insights into economic growth patterns, identify emerging trends, and support evidence-based decision-making for various stakeholders.**

## <p>PROJECT OVERVIEW<p>

The following steps were taken into consideration:
- **Data Understanding**: Processes involved: Loading dataset generated from the world bank website; Bivariate/Multivariate analysis;
- **Data Preparation***: Data cleaning; Removing Duplicates; Dealing with missing values; Stationarity Check; Feature Importances
- **Data Visualization**:
- **Modelling**: Plot ACF/PACF plots, AR, ARIMA & SARIMA Models, Testing accuracy (MSE & MAE scores)
- **Model Evaluation, Prediction & Forecating**

## <p>SOME IMPORTANT VISUALIZATIONS<p>

Feature Importance: Technique that calculates a score for all the features for our dataset — the scores represent the “importance” of each feature. A higher score means that the specific feature will have a larger effect on the model that is being used to predict our target variable. This shall assist us in better understanding our data and model and reducing the number of input features.
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/d371e747-0a44-4979-b967-0ee6d143be65) 

Time Series Trend Analysis & visualizing the impact of differencing on the data set (to remove trends & seasonality as we aim to make series stationary)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/6ab038e6-2e4f-4d88-a970-764338681a74)  ![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/313dbaf5-abe1-4d3c-b839-bc07120026bd) 

Time Series Decomposition: Decompose our time series into 3 distinct components: Trend, Seasonality & Residual(Noise); making it easier to quickly identify changing mean or variation in our time series.
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/d00f2ed5-5f03-44ef-9585-76a1cc24ab1d) 

The autocorrelation plot shows the correlation between the time series and its lagged values. The partial autocorrelation plot shows the partial correlation between the time series and its lagged values, after removing the effect of intermediate lags.

If the autocorrelation plot shows a significant correlation at lag 1 and the partial autocorrelation plot shows a sharp drop at lag 1, it suggests that the time series is stationary. If the autocorrelation plot shows a slow decay and the partial autocorrelation plot shows significant correlations at multiple lags, it suggests that the time series is not stationary and may require differencing.
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/7427d4cd-71be-4206-8347-72a84843cd07) 
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/8286a5d8-3696-40b9-982f-036e8dcf0aa1)

Modelling, Prediction & Evaluation (Models: AR, ARIMA & SARIMA)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/e9ca719f-e67f-40d8-9b60-62401f6277af)  
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/624896ce-9ce5-4cc8-8bbe-6c294ffa5391)  ![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/798a5e00-7bd0-4552-9588-811f22d39587)

## <p>MODEL RESULTS<p>

To avoid overfitting, our Best performing algorithm is the Random Forest Regression

| Model | MSE   | MAE  |
|:------|:----- |:-----|
| AR    | 0.013 | 0.087|
| ARIMA | 0.004 | 0.040|
| SARIMA| 0.0043|      |

An MSE that is close to 0 indicates that the estimator is predicting observations of the parameter with perfect accuracy, which would be an ideal scenario but it is not typically possible.
