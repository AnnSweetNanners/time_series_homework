# A Yen for the Future
Unit 10 Time Series Homework

Machine Learning is developing statistical models that can learn from inputs and predict output. These notebooks attempt to predict price changes in the Yen over specified time periods using quantitative analysis models.

**We analyze the Yen data using the following Models:** 

*ARMA* - "Autoregressive Moving Average" - models future prices based on the price of yen being a function of the price of yen in a prior period combined with errors from the prior and current period.

*ARIMA* - “Autoregressive Integrated Moving Average.” The only difference, between this model and ARMA, is the “integrated” part. Integrated refers to the number of times needed to difference a series in order to achieve stationarity (when statistical properties are constant over time), which is required for ARMA models to be valid.

*GARCH*- "Generalized Autoregressive Conditional Heteroskedasticity." This model also utilizes AutoRegression and Moving Average but accounts for lag variance terms. GARCH also predicts future variance and expects stationarity. 

### Dependencies required
Python 3
Pandas
Numpy
Path Library
Matplotlib


### Assumptions
The summary of findings assumes today is close to the date involved in the statistical modeling. 
### Summary for findings
Based on the time series analysis the price of the Yen is rising. If the risk could be supported in the portfolio, there could be opportunity to make money, specifically in the short term. 

Based on my evaluation, I would believe these models could be valuable in modeling predicted price changes and risk associated with invetments.

#### Answers to questions in the assignment WITH numeric results to back up your answers

#### Time Series 
1. The plot of Yen prices appears cyclical. It appears there is a peak in the Yen Price approximately every 4 years. Followed by a significant decline in price which bottoms out approximately 2 years later, which also occurs every approximately 4 years.

2. Based on the P values in the Summary for the ARMA model,I believe the model needs work. The P Values (not less than .05) show a statistically high likelyhood that the co-efficients different than what is modeled, but may actually be 0. While the co-efficients used are numerically close to 0, the model would change.

3. Based on the Summary data for the ARIMA model, the P Values reflect in 3 of the 5 lags, there is 40% chance or less (one lag as low as 4%) that the co-efficient values are correct. All P values were higher than .05. This model is not a good fit. The total lags seem high, and likely need to be reduced.

4. The Summary data for the GARCH model shows it also needs work. The P-Value for Alpha-1 appears to be a good fit. The P values are less than 0.05, they represent almost a 99%  likelihood that the co-efficients are what they are, or are numerically 0. The P-value for Alpha-2 though is 100%, which means the co-efficient in the model may be incorrect. Given the co-efficient used is 0, I believe this model to be the most accurate of the group.

#### Regression Analysis
1. The model performs better on In-Sample data than Out-of-Sample data, having a lower RMSE. The RMSE should be lower for the test data than the training data. Additionally, the RMSE's for test and training data should be closer to each other, which would illustrate the model is working well. Since the model is performing better on training data than testing data, it appears to be overfit.