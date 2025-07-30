**📈 Stock Trend Prediction Web App**

The code presents an interactive web app that uses a trained LSTM neural network to forecast stock prices based on historical market data.

<img width="2469" height="1222" alt="image" src="https://github.com/user-attachments/assets/2ca0ec56-33fd-41ec-94d8-3b5b4c83437e" />

**Overview**
This project combines deep learning with financial data analysis to build a predictive system that anticipates stock trends. Using an LSTM model trained on historical stock prices, it generates future price predictions and displays them alongside actual data in a clean, interactive Streamlit interface. 

**Features**
- Ticker-based Input: Enter any valid stock symbol (e.g. AAPL, GOOG, TSLA) to fetch historical stock data automatically
- Visual Time Series Charts: Raw Closing Prices, 100-day & 200-day Moving Averages, Actual vs Predicted Prices
- LSTM-Powered Predictions: Trained model (keras_model.h5) uses sequence learning to predict stock prices based on trends
- Streamlit Interface: Deploys instantly as a modern, interactive web app with a smooth UX

**How It Works**
1. Data Collection
Historical daily stock prices from 2010 to 2019 are pulled from Yahoo Finance via the yfinance API.

2. Visualization
Several plots help users understand historical trends:
- Raw prices over time
- Prices with moving averages
- Predicted vs real prices

3. Data Preprocessing
- Split 70% training / 30% testing
- Normalized using MinMaxScaler
- 100-day sliding windows are created for time-series prediction

4. Model Prediction
- Pretrained LSTM model is loaded (keras_model.h5)
- Takes in the last 100 days of the training set + testing data
- Predicts stock closing prices over time

5. Results Display
- Rescales predictions to real price range
- Final plot compares predicted vs. original prices


<p align="center">
  <b>Tech Stack & Responsibilities Breakdown</b>
</p>

<table align="center">
  <tr>
    <th>Technology / Library</th>
    <th>Purpose in the Project</th>
    <th>How It’s Used</th>
  </tr>
  <tr>
    <td><b>Python</b></td>
    <td>Core programming language</td>
    <td>Powers backend logic including data handling, model inference, visualization</td>
  </tr>
  <tr>
    <td><b>Streamlit</b></td>
    <td>Web app framework</td>
    <td>Turns Python script into interactive UI</td>
  </tr>
  <tr>
    <td><b>yFinance</b></td>
    <td>Financial data API</td>
    <td>Fetches stock data like closing price, volume, etc.</td>
  </tr>
  <tr>
    <td><b>Keras</b><br>(TensorFlow backend)</td>
    <td>Deep learning framework</td>
    <td>Loads and runs LSTM model for time-series forecasting</td>
  </tr>
  <tr>
    <td><b>LSTM Model</b></td>
    <td>Neural network</td>
    <td>Predicts stock prices by learning temporal patterns</td>
  </tr>
  <tr>
    <td><b>Pandas</b></td>
    <td>Data manipulation</td>
    <td>Splits and preps training/testing datasets</td>
  </tr>
  <tr>
    <td><b>NumPy</b></td>
    <td>Numerical ops</td>
    <td>Creates 100-day time windows for model input</td>
  </tr>
  <tr>
    <td><b>scikit-learn</b></td>
    <td>Preprocessing</td>
    <td>Normalizes data using <code>MinMaxScaler</code></td>
  </tr>
  <tr>
    <td><b>Matplotlib</b></td>
    <td>Charting</td>
    <td>Visualizes original & predicted stock price trends</td>
  </tr>
</table>

<img width="2735" height="1243" alt="image" src="https://github.com/user-attachments/assets/7b0691d0-57bb-416d-b2d8-4df8f682049e" />

**Running the Application**
1) Clone the Repository:
git clone https://github.com/EthanPoon25/stock-predictor-app.git
cd stock-predictor-app

2) Install Dependencies
Make sure you have Python and pip installed.
pip install -r requirements.txt

3) Run the App
Launch the Streamlit web app in your browser.
streamlit run app.py

