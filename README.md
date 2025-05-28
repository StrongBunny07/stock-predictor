# Stock Predictor

This project contains a Jupyter notebook for predicting stock prices using machine learning techniques.


## Code Overview

- **Library Installation**  
  The necessary Python libraries (`yfinance`, `keras`, `matplotlib`, and `scikit-learn`) are installed to download data, build and train the model, and visualize results.

- **Data Downloading**  
  Uses `yfinance` to fetch historical stock data (`AAPL`) from 2010 to 2023.

- **Data Preprocessing**  
  The closing prices are scaled between 0 and 1 using `MinMaxScaler` to normalize the data for better model performance.

- **Sequence Creation (`create_sequence`)**  
  This function generates input-output sequences of length 60 days to train the LSTM model. Each input sequence contains 60 days of stock prices, and the output is the price on the next day.

- **Model Building and Training**  
  A sequential LSTM model with two LSTM layers and a Dense output layer is created and trained to predict stock prices based on historical data.

- **Prediction and Visualization**  
  The model's predictions on the test data are inverse-transformed back to the original scale, and then actual vs predicted prices are plotted to visualize performance.

- **Today's Price Output**  
  Prints the predicted stock price for the last day in the test set.

- **Tomorrow's Price Prediction**  
  Uses the most recent 60 days of data to predict the stock price for the next day.


## Files

- `stock_price_predictor.ipynb` — Main notebook with the prediction code.

## How to use

Open the notebook in Jupyter Notebook or VS Code and run the cells.
