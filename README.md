# REAL TIME CANDLESTICK CHART ANALYSIS FOR INDONESIAN STOCKS

In this program, linear regression is used to predict stock price trends in a simple manner. Linear regression is a statistical method used to determine the linear relationship between two variables, namely the independent variable (X) and the dependent variable (Y). In the context of this program, the independent variable (X) is time or the data index, while the dependent variable (Y) is the closing stock price. By using linear regression, this program helps users identify stock price trends in a straightforward manner, which can be a valuable tool in investment decision-making. These trends are represented by the trend line in the candlestick chart, which is continuously updated in real-time.

Here is the algorithm used for linear regression in the program:
## 1. Data Collection
   - Stock price data is obtained from Yahoo Finance and stored in a DataFrame. This data includes time (index) and closing stock prices (Y).
## 2. Data Preparation
   - The data index is used as the independent variable (X), and the closing stock prices are used as the dependent variable (Y).
## 3. Linear Regression Calculation
   - Linear regression is performed by calculating two parameters: the slope (m) and the intercept (c) in the linear equation Y = mX + c. This is done using the Least Squares Regression (LSR) method, which seeks the values of m and c that minimize the sum of squared errors between actual data points and linear predictions.
   - This step is carried out using numpy: m, c = np.linalg.lstsq(A, y, rcond=None)[0], where A is a matrix containing X and a unit vector, and y is a vector of stock closing prices.
## 4. Creating a Trend Line
   - After obtaining the values of m and c, the program creates a trend line with the linear equation Y = mX + c. Data X (time) and predicted Y (stock prices) are used to create the trend line.
## 5. Adding the Trend Line to the Chart
   - The generated trend line is added to the candlestick chart using Plotly. This allows users to visualize stock price trends in the real-time updating candlestick chart.
