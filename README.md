# Intelligent Stock Ranking and Real-Time Alert System for the Colombo Stock Exchange

This repository contains the data analysis and preprocessing work for a stock ranking and real-time alert system for the Colombo Stock Exchange (CSE).

## Current Work

The current stage includes:

- Exploratory Data Analysis of S&P SL20 stock data
- Data quality assessment
- Stale and unchanged price analysis
- Validation and correction of daily return calculations
- Handling discontinuities and large gaps in historical stock data
- Recalculation of gap-aware time-series features
- Pearson and Spearman correlation analysis

## Key Data Validation Findings

During additional validation, the original daily return variable was found to contain inconsistencies caused by different security types being included in the original time sequence.

Returns were therefore recalculated after restricting the analysis to ordinary shares.

Large historical gaps were also identified. To prevent observations separated by long periods from being treated as consecutive trading days, each company's history was divided into continuous time segments.

The following final time-series variables were recalculated within these continuous segments:

- DailyReturn_Pct_Final
- LogReturn_Final
- MA_30d_Final
- MA_90d_Final
- Volatility_30d_Ann_Final

## Repository Structure

```text
CSE_Group_Project/
├── CSE_SP20_EDA_Consolidated.ipynb
├── README.md
├── requirements.txt
└── .gitignore