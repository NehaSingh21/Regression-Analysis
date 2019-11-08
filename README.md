# Regression-Analysis

**Data :** 

We have a list of 9 ETFs as given below - 

1) Utilities SPDR (XLU)
2) Vanguard Communication Services (VOX)
3) VanEck Semiconductors (SMH)
4) Biotech SPDR (XBI)
5) Financial Select Sector SPDR (XLF)
6) SPDR S&P Oil & Gas (XOP)
7) VanEck Vectors Oil Service (OIH)
8) SPDR Retail (XRT)
9) Health Care SPDR (XLV)

For each ETF, we will find its top 40 US stock holdings. Next for all the stocks and ETFs plus the SPY and QQQ, we will 
download daily adjusted closing prices for Jan, Feb & March 2019. 


**Model :**

For each stock we define a linear model of the form 

 > r_S ~ r_SPY + r_QQQ + r_ETF1 + ... + r_ETFk
  
where ETF1, ETF2,.. ,ETFk are all the ETFs that the stock is top 40 member of. Each value represents the daily returns.  

We are going to estimate the linear models using 

1. OLS
2. The Huber penalty function
3. The Tukey Bisquare penalty function

We train the models on the first 30 days of returns and analyse their performance. The performance is measured by out-of-sample
R_squared and out-of-sample R_squared normalized by in-sample standard distribution.  
