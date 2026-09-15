# Inflation Signal Monitor

A Python-based macroeconomic monitoring tool that analyzes U.S. inflation
compensation and cross-market financial signals using data from the Federal
Reserve Economic Data (FRED) API.

## Overview

The Inflation Signal Monitor tracks movements in the 5-year breakeven
inflation rate and compares them with changes in Treasury yields and
cross-market indicators.

The project analyzes:

- 5-Year Breakeven Inflation Rate
- 5-Year Nominal Treasury Yield
- 5-Year Real Treasury Yield
- WTI Crude Oil
- VIX
- U.S. High-Yield Credit Spread
- Broad U.S. Dollar Index

## Features

- Downloads current macroeconomic and financial data from FRED
- Decomposes 5-year Treasury yields into real yields and inflation compensation
- Creates interactive Plotly visualizations
- Normalizes cross-market indicators for comparison
- Calculates correlations with daily breakeven inflation changes
- Detects the largest breakeven inflation movements
- Classifies major episodes using real-yield and breakeven movements
- Exports analysis results to CSV and interactive HTML

## Tech Stack

- Python
- pandas
- NumPy
- Plotly
- FRED API
- Google Colab

## Methodology

The monitor focuses on the relationship:

Nominal Treasury Yield ≈ Real Treasury Yield + Inflation Compensation

The 5-year breakeven inflation rate is used as a market-based measure of
inflation compensation. It should not be interpreted as a pure inflation
expectation because it can also reflect inflation-risk and TIPS-liquidity
premiums.

Daily changes in the breakeven rate are compared with movements in oil,
volatility, credit spreads, the dollar, and Treasury yields.

## Running the Project

1. Open the notebook in Google Colab.
2. Create a FRED API key.
3. Add the key to Colab Secrets as `FRED_API_KEY`.
4. Run the notebook from top to bottom.

## Outputs

The notebook produces:

- Latest market readings
- Treasury yield decomposition
- Cross-market stress visualization
- Daily-change correlation analysis
- Largest breakeven-move episodes
- CSV exports
- Interactive HTML charts

## Disclaimer

This project is for educational and analytical purposes only. Correlations
and episode classifications are descriptive and should not be interpreted
as causal relationships or investment advice.
