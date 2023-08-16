# Renko Chart-Based Trading Strategy

This repository contains Python code that implements a simple trading strategy based on Renko charts. Renko charts are a type of financial chart that focus on price movements rather than time, using fixed price movements to create patterns.

## Overview

The code uses historical stock price data to analyze price movements and identify Renko candle patterns. It follows a basic strategy to identify both green and red candles, as well as transitions between them. The goal is to recognize potential trends and reversals in the price movement.

## Code Explanation

This code is implementing a trading strategy based on Renko charts, a type of financial chart that focuses on price movements rather than time. Renko charts use fixed price movements (often referred to as "bricks") to create a visual representation of price trends. Here's an explanation of the code in the context of a Renko chart-based trading strategy:

#### 1. Importing Libraries:

- numpy and scipy.stats.norm are imported for mathematical operations.
- yfinance is used to fetch historical stock price data.
- datetime is used for date and time calculations.
- pandas is used for data manipulation.
#### 2. Fetching Data:

- Historical stock price data for a specific stock index (ticker_name) is downloaded from Yahoo Finance using the yf.download function.
- The data is filtered to include only the trading hours of a specific day (ohlcv DataFrame).

#### 3. Data Processing:

- Irrelevant columns ('Adj Close' and 'Volume') are dropped from the data.
- An initial price level (pivot) is set as the closing price of the first data point.

#### 4. Renko Candle Analysis:

1. The code iterates through each closing price i in the dataset.
2. It maintains two flags, green_flag and red_flag, to track the current candle phase (green or red).
3. If the current phase is green (green_flag is True):
  - If the price exceeds the upper threshold (pivot+fix_step), a new green candle pattern is identified, and the pivot is updated to the new price level.
  - If the price drops below a certain threshold (pivot-2*fix_step), a transition from green to red is identified, and the pivot is updated.
4. If the current phase is red (red_flag is True):
  - Similar logic is applied to identify red candle patterns and transitions to green candles.


#### 5. Counting and Output:

- The code keeps track of the number of green and red candle patterns (green and red counters).
- After analyzing the dataset, the code prints the count of green and red candle patterns identified.

- 
This code simulates a trading strategy to identify Renko candle patterns and transitions between green and red candles. The thresholds (fix_step) determine when a candle pattern or transition is recognized. This strategy is based on price movements and can be customized and adjusted to fit market conditions and trading preferences.



## Usage

1. Make sure you have the required libraries installed. If not, you can install them using `pip`:
   ```bash
   pip install yfinance numpy pandas scipy

## NOTE
  This code is for educational and illustrative purposes only. Actual trading decisions should be based on thorough analysis, risk management, and a proper understanding of financial markets. The code can be further customized and enhanced to suit specific trading preferences.


## Creator

This project was created by [Vishwas Joshi](https://github.com/vishwasjoshi2019).


[![GitHub](https://img.shields.io/badge/GitHub-%40vishwasjoshi2019-blue)](https://github.com/vishwasjoshi2019)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%40vishwasjoshi2019-blue)](https://www.linkedin.com/in/vishwasjoshi2019/)
[![Gmail](https://img.shields.io/badge/Gmail-vishwasjoshi2019%40gmail.com-red)](mailto:vishwasjoshi2019@gmail.com)
[![Institute Email](https://img.shields.io/badge/Institute%20Email-vishwas.j%40iitgn.ac.in-red)](mailto:vishwas.j@iitgn.ac.in)
[![Instagram](https://img.shields.io/badge/Instagram-%40cursed__geek-orange)](https://www.instagram.com/cursed_geek/)
[![Twitter](https://img.shields.io/badge/Twitter-%40Vishwas79116150-blue)](https://twitter.com/Vishwas79116150)
