# Portfolio-Quantitative-Risk-Analysis

This program analyzes risk and return to build an investment portfolio for a client. The program uses quantitative analysis to run through the key risk-management metrics to determine the fund (out of four) with the best potential. This includes calculating daily returns, standard deviations, Sharpe ratios, and betas as well as plotting visualizations for each.

----

## Technologies
This application is written in Jupyter Lab Notebook in the Python programming language. The Python libraries used in this application are Pandas (DataFrame and NumPy) and Matoplotlib. Official documentation shown below:

[Pandas](https://pandas.pydata.org/docs/index.html)

[pandas.DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html)

[NumPy](https://numpy.org/doc/)

[Matplotlib](https://matplotlib.org/stable/index.html)

----

## Installation Guide
This program uses the Pandas library. If the user is not already running an environment that includes Pandas, then they will need to intall the library. Installation guide shown below:

[Pandas Installation](https://pandas.pydata.org/docs/getting_started/install.html)

----

## Usage
For the program to run correctly, the user must make sure that all libraries and dependencies are correctly imported in the beginning of the code. This looks like:

> import pandas as pd

> import numpy as np

> from pathlib import Path

> %matplotlib inline

The user must also make sure that their reference to the whale_navs.csv file reflects the correct location in their directory.

The program is comprised of 6 parts:

1.Import the Data

Using the Pandas read_csv function and the Path module, the program will import the data from the whale_navs.csv file and creates a DataFrame. This DataFrame contains portfolio data with net asset value pricing, as well as data about the S&P 500 index which will be the market benchmark for the analysis. 

2.Analyze the Performance

This section analyzes the data to determine if any of the portfolios outperform the broader stock market. The program will caluculate daily and cumulative returns for both the four funds and the S&P. It will also plot both returns to help the user visualize the funds performance versus the S&P 500.

3.Analyze the Volatility

This section analyzes the volatility of each of the four fund portfolios and the S&P 500. The program will create box plots to visualize the volatility, or spread, of all funds against the S&P 500, and then all funds against each other.

4.Analyze the Risk

This section evaluates the risk profile of each portfolio. To do so, the program will first caluclatate the standard deviation and the annualized standard deviation (using 252 trading days) of each portfolio and the S&P 500. The program will then plot the 21 day rolling standard deviations of all.

5.Analyze the Risk-Return Profile

This section determines the risk-return profiles for each portfolio by calculating Sharpe ratios. To calculate the Sharpe ratios, the program will first caluclate the annualized average return data by multiplying the mean of the daily returns by 252 trading days. Then, the program will divide the average annual return by the annualilzed standard deviation (caluclated earlier) to get the Sharpe ratio. The program will then plot the Sharpe ratio data as a bar chart to show negative returns versus positive returns.

6.Diversify the Portfolio

This section evaluates how two portfolios (*Berkshire Hathaway and Tiger Global Management in this case, but the user can change the code to evaluate the portfolios of their choice*) react relative to the S&P 500. First, the program will calculate the 60 day rolling variance of the S&P 500. Then for each portfolio, the program will calculate the covariance, then the beta (covariance of portfolio / variance of S&P 500), and then the mean to calculate the average value of the 60-day rolling beta. The program will plot the 60-day rolling beta for each portfolio to show that funds sensitivity to movements in the S&P 500.

----

## Contributors

Arlie Jones

[E-mail](arliejones98@gmail.com)

[LinkedIn](https://www.linkedin.com/in/arlie-jones-020092159/)

----

## License

None
