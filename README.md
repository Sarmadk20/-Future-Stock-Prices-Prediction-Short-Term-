# -Future-Stock-Prices-Prediction-Short-Term-

----------Overview-----------

This project focuses on predicting the next day's closing price of a stock using machine learning.
Historical stock data is fetched using Yahoo Finance, preprocessed, visualized, and then used to train a regression model.

-----------Objective-----------

-Retrieve historical stock data using yfinance
-Explore and visualize the dataset
-Build a regression model to predict next-day closing prices
-Evaluate and explain model performance
-Plot actual vs predicted values

-----------Dataset-----------

-Source: Yahoo Finance
-Stock: Apple (AAPL)
-Period: Last 2 years
-Key Columns Used:
-Open
-High
-Low
-Volume
-Close (target)

-----------Methodology-----------
1. Data Collection

Data is fetched using:

stock = yf.Ticker("AAPL")
df = stock.history(period="2y")

2. Data Preprocessing

Checked for null and duplicate values

Split data into features (X) and target (y)

Used a 70:30 train-test split

3. Model Used

RandomForestRegressor
Chosen because it handles non-linear stock patterns well and is robust with noisy financial data.

4. Evaluation
-The model is evaluated using:
-Mean Absolute Error (MAE)
-Mean Squared Error (MSE)
-R² Score

Scatter plot: Actual vs Predicted closing prices

 -----------Visualizations-----------

-The notebook includes:
-Closing price trend over time
-Volume trend
-Actual vs Predicted closing price plot
-These help understand both the dataset behavior and model accuracy.

----------Explanation of Results------------
The evaluation metrics show that the model predicts the next-day closing price with reasonable accuracy.
A low MAE and MSE mean the model’s errors are small and stable, while a higher R² score indicates it captures most of the stock’s price patterns.
Overall, the model tracks general trends well, though sudden market movements remain difficult to predict—which is normal for financial data.
The Random Forest model performs well, but more advanced time-series methods could improve forecast accuracy.

-----------Final Insights-----------
-The model learned patterns from 2 years of Apple stock data.
-Scatter plot shows how closely predictions follow actual closing prices.
-MAE/MSE indicate the typical prediction error in dollars.
-Random Forest performed well for short-term movement prediction, but stock prices remain highly volatile and not perfectly predictable.
