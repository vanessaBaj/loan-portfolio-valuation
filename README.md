# loan-portfolio-valuation

This repository contains the code and resources for valuing a loan portfolio for a global online lending platform. The valuation process follows a detailed methodology to ensure the balance sheet values are correct, focusing on the loan portfolio's value as of December 31, 2020.

## Project Overview

The value of the loan portfolio depends on future cash flows, which are stochastic. This project aims to verify that the client's portfolio has been valued correctly by computing the historical repayment percentages, forecasting future cash flows, and determining the present value of these cash flows.

## Data

The data provided by the client ranges from June 2019 until December 2020. Each month constitutes a vintage, and the data includes the loan amount originated per vintage and the repayments observed up to and including December 2020.

## Methodology

1. **Inspect Historical Data**: Load and inspect the historical data.
2. **Compute Historical Repayment Percentages**: Calculate the repayment percentages for each vintage.
3. **Compute Expected Repayment Percentages**: Based on the provided assumptions, compute the expected repayment percentages over the loan's lifetime.
4. **Forecast Cash Flows**: Use the expected repayment percentages to forecast future cash flows.
5. **Compute Present Value**: Using the assumed discount rate, derive the present value of the forecasted cash flows and the portfolio.
6. **Comparison with Client Estimate**: Compare the computed portfolio value with the client's estimate and determine if the difference falls within the acceptable threshold.

## Requirements

- Python 3.x
- pandas

## Files
Data.csv: Historical loan data provided by the client.
valuation.py: Main script for performing the valuation.
assumptions.pdf: PDF document detailing the assumptions used for computing expected repayment percentages.

## Detailed Steps
Step 1: Inspect Historical Data
Load and inspect the historical data provided by the client. The data ranges from June 2019 until December 2020 and includes the loan amounts originated per vintage and the repayments observed up to and including December 2020.

Step 2: Compute Historical Repayment Percentages
Calculate the historical repayment percentages, i.e., each repayment’s share of the origination amount. This can be done using Python and pandas.

Step 3: Compute Expected Repayment Percentages
Based on the assumptions provided in the assumptions.pdf, compute the expected repayment percentages for all vintages over the lifetime of the loans.

Step 4: Forecast Cash Flows
Use the expected repayment percentages to compute the forecasted cash flows using the origination amounts.

Step 5: Compute Present Value
Using the assumed discount rate, derive the present value of the forecasted cash flows and of the portfolio. Don't forget to convert the annual interest rate to a monthly interest rate.

Step 6: Comparison with Client Estimate
Compare the computed portfolio value with the client's estimate of CHF 84,993,122.67. Compute both the absolute and relative differences. Determine if the difference falls below the acceptable threshold of CHF 500,000.
