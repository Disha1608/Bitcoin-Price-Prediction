Bitcoin Price Prediction Model

Overview
This project focuses on forecasting Bitcoin closing prices using Time Series (ARIMA), Machine Learning (Gradient Boosting), and Deep Learning (LSTM) models. The goal is to determine the most effective model based on prediction accuracy (measured using RMSE).

Dataset
-  Source: Historical Bitcoin price dataset
-  Size: 3566 rows, 7 columns

Key Features:
  - Date: Timestamp of the recorded price (used as an index)
  - Close: Target variable for prediction
  - Open, High, Low, Adj Close, Volume : Additional price-related attributes

Models Implemented

1.ARIMA (AutoRegressive Integrated Moving Average)

- Conducted stationarity tests (ADF test) and applied differencing
- Selected optimal ARIMA order using AIC/BIC criteria
- Generated forecasts for Bitcoin closing prices

2.Gradient Boosting Regressor

- Preprocessed data by handling missing values and scaling
- Trained a Gradient Boosting model on historical price data
- Tuned hyperparameters using Grid Search
- Evaluated model using RMSE

3.LSTM (Long Short-Term Memory)

- Normalized the dataset to improve training efficiency
- Transformed data into sequences for time series forecasting
- Designed an LSTM network with multiple layers
- Trained the model using Adam optimizer and Mean Squared Error loss
- Evaluated prediction accuracy

Performance Evaluation

 Model 	RMSE
ARIMA	3393
Gradient Boosting	992
LSTM	1307



Key Takeaways

- Gradient Boosting achieves the lowest RMSE, making it the most accurate model.
- LSTM performs better than ARIMA but requires longer training time.
- ARIMA struggles with capturing long-term dependencies in volatile Bitcoin prices.

Installation

Ensure you have Python 3.8+ installed. Install dependencies using:
pip install -r requirements.txt

Future Improvements

- Experiment with Transformer-based models for better long-term forecasting.
- Incorporate market sentiment data to improve predictions.
- Use high-frequency data (minute-by-minute) for more granular forecasting.

Contributors

Disha Chauhan – Data Analyst Intern

License

This project is open-source and available under the MIT License.
