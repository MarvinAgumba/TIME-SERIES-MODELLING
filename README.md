# <p>PREDICTING GDP USING TIME SERIES MODEL<p>

This repository shall host my final phase 5 project where we shall be analyzing & forecasting GDP trends (Case study Kenya - Finance Bill Reaction).

Kenyan Parliament recently, on the 26th of June 2023, passed to law the contentious Finance Bill 2023 proposing a raft of tax policy measures that aim to yield additional revenue and explore more effective measures to enhance the Country's revenue collection.

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING-PROJECT/assets/122484885/9e92cba7-b0cd-4c92-bd18-e962f7baa3bd)

The Government feels the ratio of tax revenue as a percentage of Gross Domestic Product (GDP) being well below acceptable levels to enable spur economic growth & reduce the cost of living in the long term. (***According to the World Bank, tax revenues above 15% of a country’s GDP are a key ingredient for economic growth and, ultimately, poverty reduction***)

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING-PROJECT/assets/122484885/d6ecfb7d-18fc-4181-b934-adb35ac6f6ef)

## <p>BUSINESS UNDERSTANDING<p>

**This project shall aim to analyze the Country's historical GDP trends and forecast future GDP growth. The analysis shall assist provide insights into economic growth patterns, identify emerging trends, and support evidence-based decision-making for various stakeholders.**

## <p>PROJECT OVERVIEW<p>

The following steps were taken into consideration:
- **Data Exploration & Understanding**: Understanding the Distribution of the Dataset; Create visualizations to better understand the distributions of variables in a dataset  (Visualizing Distributions- Histograms & KDE plots);
- **Data Preparation***: Dealing with data types; Detecting & Dealing with Null Values; Checking For Multicollinearity; Normalizing Data; Feature Importance & Selection
- **Modelling & Evaluation**: Detrend Time Series; Plot ACF & PACF; Decide on the AR, MA, and order of the models; Fit the model to get the correct parameters and use for prediction

## <p>SOME IMPORTANT VISUALIZATIONS<p>

**Feature Importance:** Technique that calculates a score for all the features for our dataset — the scores represent the “importance” of each feature. A higher score means that the specific feature will have a larger effect on the model that is being used to predict our target variable. This shall assist us in better understanding our data and model and reducing the number of input features. (Reduces Overfitting; Improves Accuracy; Reduces Training Time

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/3684d435-c416-45d9-84ac-07877e51b58b)

**Time Series Trend Analysis** & visualizing the impact of differencing on the data set (to remove trends & seasonality as we aim to make series stationary)

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/10e55839-6871-4dbf-acb1-cfdf12b34f0d)

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/d8e494b4-8b04-4114-af73-c406589034f8)

**Time Series Decomposition:** Decompose our time series into 3 distinct components: Trend, Seasonality & Residual(Noise); making it easier to quickly identify changing mean or variation in our time series.

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/9ab1315c-1caf-4c80-958d-a948d72e983e)

**The autocorrelation plot** shows the correlation between the time series and its lagged values. 

**The partial autocorrelation plot** shows the partial correlation between the time series and its lagged values, after removing the effect of intermediate lags.

If the autocorrelation plot shows a significant correlation at lag 1 and the partial autocorrelation plot shows a sharp drop at lag 1, it suggests that the time series is stationary. If the autocorrelation plot shows a slow decay and the partial autocorrelation plot shows significant correlations at multiple lags, it suggests that the time series is not stationary and may require differencing.

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/5ca17ac0-2a20-4065-ae8e-2170c1912c04)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/32981098-adb6-49b7-9d09-8d234976c829)

**Modeling**, Prediction & Evaluation (Models: AR, ARIMA & SARIMA)

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/261f68c8-954e-4651-acdf-e476e26d14bb)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/64c4f25d-41c3-4c18-ae89-ab9bb7d2b50c)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/25194413-2dab-4159-b2ff-fcea237c1f55)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/0dc31c8d-3d1f-4d8e-99c3-8dd02af9f936)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/46867283-a634-48b8-87ec-d3f82a895790)
![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING/assets/122484885/0cf78e78-80b0-496e-9e27-26c4ef5bc766)

## <p>MODEL RESULTS<p>

To avoid overfitting, our Best performing algorithm ARIMA

| Model         | MSE   | MAE  |
|:--------------|:----- |:-----|
| AR            | 1.3%  | 0.087|
| ARIMA         | 0.40% | 0.040|
| SARIMA: 1 Step| 0.07% |      |
| SARIMA:Dynamic| 0.43% |      |

An MSE that is close to 0 indicates that the estimator is predicting observations of the parameter with perfect accuracy, which would be an ideal scenario but it is not typically possible.

## <p>MODEL DEPLOYMENT& RESULTS<P>

![image](https://github.com/MarvinAgumba/TIME-SERIES-MODELLING-PROJECT/assets/122484885/561bfe8e-9bf3-4f15-b0ec-970fbb24ed92)

The government should monitor the impact of the new taxes on the economy and make adjustments as needed. They should also be prepared to address any legal challenges to the bill.

## <p>SOURCES<p>

https://www.worldbank.org/en/country/kenya/publication/kenya-economic-update-keu

https://datatopics.worldbank.org/world-development-indicators

http://www.parliament.go.ke/node/19912 https://towardsdatascience.com/feature-selection-techniques-in-machine-learning-with-python-f24e7da3f36e

https://www.centralbank.go.ke/statistics/government-finance-statistics/ https://kra.go.ke/news-center/press-release/1956-kra-sustains-revenue-growth-despite-economic-shocks

I also drew inspiration from Moringa School Flatiron Canvas Content; various available Kaggle notebooks and Github GDP analysis notebooks
