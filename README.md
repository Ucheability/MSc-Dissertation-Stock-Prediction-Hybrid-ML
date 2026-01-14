# MSc-Dissertation-Stock-Prediction-Hybrid-ML
A hybrid Machine Learning model combining LSTM and Random Forest to forecast stock trends for Google, Meta, and NVIDIA, integrated with NLP-driven sentiment analysis
# Forecasting Stock Price Trends Using Sentiment Analysis and Machine Learning

## 1. Introduction

Accurate stock price forecasting remains a significant challenge in dynamic financial markets due to high volatility, non-linear relationships, and the influence of both quantitative and behavioural factors. Traditional statistical models often struggle to capture these complex temporal dependencies, limiting their effectiveness in real-world investment decision-making.
This MSc project presents an integrated forecasting approach that combines advanced machine learning techniques with Natural Language Processing (NLP)-based sentiment analysis. By leveraging historical price data alongside qualitative market sentiment, the study aims to develop a more holistic understanding of stock price movements.
The research focuses on three major technology firms—Google (Alphabet Inc.), Meta, and NVIDIA—and explores how hybrid modelling techniques, including Long Short-Term Memory (LSTM) networks and Random Forest algorithms, can enhance predictive accuracy and reliability. The resulting framework is designed to support more informed financial analysis, risk assessment, and strategic decision-making.

## 2. Problem Statement

The central challenge in financial forecasting is that stock prices are highly volatile and influenced by a vast array of interconnected factors. Conventional statistical models frequently struggle to capture these intricate, non-linear dependencies, often resulting in inaccurate forecasts. This research addresses the gap by investigating whether combining cutting-edge machine learning techniques with qualitative sentiment analysis can enhance the precision of stock price predictions

## 3. Aim and Objectives

**Aim:** The primary aim of this project is to develop an integrated machine learning model that incorporates sentiment analysis to predict the stock prices of Google, Meta, and NVIDIA, while conducting a cross-sector analysis of these leading technology firms.

**Objectives:**

- **Literature Review:** Conduct an extensive review of current machine learning applications in financial analysis.

- **Data Acquisition:** Gather and clean a 10-year historical dataset (2013–2023) for the target companies from Yahoo Finance.

- **Sentiment Processing:** Employ Natural Language Processing (NLP) to process financial news and categorize sentiment as positive, negative, or neutral.

- **Hybrid Model Development:** Design and implement a hybrid architecture merging Long Short-Term Memory (LSTM) networks with Random Forest (RF) algorithms.

- **Performance Evaluation:** Assess the integrated model's effectiveness using metrics like MSE, RMSE, MAE, and R-squared, comparing it against standalone models.

## 4. Dataset Description

This project utilizes a multi-dimensional dataset to capture both market mechanics and investor mood:

- **Historical Stock Data:** 10 years of daily data (Jan 2013 – Jan 2023) including Open, High, Low, 
    Close, Adjusted Close, and Volume.

- **Sentiment Data:** Derived from financial news articles. Due to accessibility hurdles with real-world 
    news archives, an innovative synthetic sentiment dataset was developed to emulate genuine market trends, 
    company-specific events, and economic indicators.

- **Target Variable:** The primary feature for prediction is the 'Close' price, shifted by one day to represent the next day's forecasted value.

## 5. Methodology

The research followed a structured data science lifecycle, integrating quantitative financial modeling with qualitative sentiment analysis. The process was divided into the following key phases:

- **Phase 1: Data Collection & Preprocessing:** 

    - Historical stock data (Open, High, Low, Close, Volume) was extracted for Google, Meta, and NVIDIA via the yfinance API.
    
    - Data was normalized using MinMaxScaler to fit a range of [0, 1] for efficient neural network training.

- **Phase 2: Sentiment Engineering:**
    - Financial news headlines and market reports were processed using Natural Language Processing (NLP).
    - Sentiment scores were generated and integrated as a separate feature to capture market "mood"
      alongside technical indicators.

- **Phase 3: Hybrid Model Architecture:** 
    - LSTM (Long Short-Term Memory): Employed to capture long-term temporal dependencies and patterns in time-series data.
    - Random Forest (RF): Used as an ensemble learner to handle non-linear relationships and provide robust feature   
      importance.

- **Phase 4: Evaluation:**
    - Models were tested on a separate test set (20% of data) using MSE, RMSE, and R-squared metrics to validate accuracy
  
## 6. Tools and Technologies

This project was built entirely in Python using industry-standard libraries for Data Science and Deep Learning:

  - **Programming Language:** Python 3.x.
  - **Deep Learning:** TensorFlow & Keras (for building the LSTM architecture).
  - **Machine Learning:** Scikit-learn (for Random Forest Regressor and data scaling).
  - **Data Manipulation:** Pandas and NumPy.
  - **Data Visualization:** Matplotlib and Seaborn (for EDA and performance plots).
  - **API / Data Source:** Yahoo Finance (yfinance).
  
## 7. Exploratory Data Analysis (EDA)

Before model development, an extensive EDA was conducted to understand the underlying patterns, trends, and statistical properties of the stock data for Google, Meta, and NVIDIA.

- **Time-Series Visualization:**
  
    - Daily closing prices were plotted over a 10-year period (2013–2023) to identify long-term trends, cyclical patterns,         and periods of high volatility.
      
![Price Trends Over Time](Price%20over%20Time.jpg)
*Figure 1: 10-Year historical closing price trends for Google, Meta, and NVIDIA.*

- **Statistical Profiling:**
    - Summary Statistics: Calculated mean, median, and standard deviation to assess data distribution. For instance,
      Google's stock showed a mean closing price of approximately $59.52 with a high standard deviation of 34.63, indicating       significant growth and volatility over the decade.
    - Distribution Analysis: Skewness and Kurtosis were measured to identify deviations from a normal distribution. Most
      stock features exhibited positive skewness (approx. 1.04), suggesting a right-leaning tail common in growth stock

- **Volatility and Volume Analysis:**
-  Trading volumes were analyzed alongside price changes to detect correlations between market activity and price movements.     The analysis revealed that major price shifts often coincided with spikes in trading volume

  ![Trading Volume Over Time](Trading Volume%20over%20Time.jpg)
*Figure 2: 10-Year historical stock Trading Volume over Time for Google, Meta, and NVIDIA.*
## 8. Model Development

## 9. Results and Evaluation

## 10. Key Insights

* **Hybrid Advantage:** Combining LSTM and Random Forest provided more stable predictions.
* **Sentiment Value:** Sentiment analysis acted as a leading indicator for price shifts.
* **Robustness:** The model remained accurate across different tech stocks (Google, Meta, NVIDIA).
## 11. Limitations

## 12. Recommendations and Future Work
