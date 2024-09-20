# Stock Price Variance Analysis Using Regression Models

## Project Overview
This project explores the relationship between company-specific financial parameters and stock price variance using regression models. The goal was to help retail investors better understand which factors influence stock price movements, aiding them in making more informed decisions in the stock market.

In this study, I employed **Multiple Linear Regression** and **Hypothesis Testing** techniques to analyze over 200 financial indicators and their impact on stock price variance for a dataset covering US stocks from 2018. Additionally, advanced statistical methods such as **Broken-Stick Regression** and **Box-Cox Transformation** were used to improve the model's performance.

## Dataset
The dataset used for this project was sourced from [Kaggle](https://www.kaggle.com/datasets/cnic92/200-financial-indicators-of-us-stocks-20142018?select=2018_Financial_Data.csv) and contains financial data from over 4,400 US stocks, with 200+ financial indicators. The primary target variable was the **Stock Price Variance** for the year 2019, compared to 2018.

### Key Dataset Details:
- **Source:** Kaggle - [200+ Financial Indicators of US Stocks (2018 Financial Data.csv)](https://www.kaggle.com/datasets/cnic92/200-financial-indicators-of-us-stocks-20142018?select=2018_Financial_Data.csv)
- **Number of Records:** 4,400+ stock data points
- **Number of Features:** 200+ financial indicators

## Methodology

### 1. Data Cleaning
- **Handling Missing Values:** Missing values were imputed using the median of the respective columns.
- **Outliers and Influential Points:** identified and removed extreme outliers and influential points using quantiles and leverage statistics.

### 2. Running the Linear Model
- **Initial Model:** A multiple linear regression model was fitted using all the financial indicators. However, the model's residual plots revealed the presence of influential points and non-normal errors.

### 3. Broken-Stick Regression
- As the dataset displayed distinct groups (stock price variance < 0 and > 0), we applied two separate regression models to better fit the data.

### 4. Box-Cox Transformation
- The errors in regression models were non-normal, which violated linear regression assumptions. So used **Box-Cox Transformation** to normalize the errors and improve the model's performance.

### 5. Variable Selection
- Reduced the number of variables using **Backward Elimination** based on the AIC (Akaike Information Criterion) to retain only significant predictors. The final model contained around 70 variables.

### 6. Hypothesis Testing
- Conducted hypothesis tests on key parameters to evaluate their impact on stock price variance. Some key findings include:
  - **Revenue vs. Long-term Debt:** Revenue has a lesser or equal effect compared to long-term debt on stock price.
  - **EBIT Margin vs. Profit Margin:** EBIT margin has a lesser impact on stock price than profit margin.

## Results
The final linear regression model provided an **Adjusted R-squared value** of **0.2863** for Model A and **0.1269** for Model B, indicating a relatively poor fit for predicting stock price variance. However, the model was useful for identifying which factors influence price variance, even if it was not optimal for prediction.

### Key Findings:
- Out of 225 variables, only 70 significantly impacted stock price variance.
- Hypothesis testing confirmed that certain company parameters, such as debt ratio and market capital, have a meaningful impact on stock prices.

## Future Work
Given the limitations of linear regression in predicting stock price variance, exploring more advanced techniques such as **Robust Regression** or **Neural Networks** to improve predictive accuracy can be suggested.

## Conclusion
While the regression models used in this study were not highly effective for predictive purposes, they provided valuable insights into the financial parameters that affect stock price variance. These findings can assist retail investors in making more rational decisions based on company fundamentals rather than market sentiment.


