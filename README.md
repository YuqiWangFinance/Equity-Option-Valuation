# Equity-Option-Valuation
A general framework for valuing European vanilla call options using Black-Scholes-Merton, binomial tree, and Monte Carlo, using AAPL as an example.

## Overview

This project builds an Excel-based valuation framework for European vanilla call options and compares three pricing methods:

- Black-Scholes-Merton (closed-form benchmark)
- Binomial tree (discrete-time cross-check)
- Monte Carlo simulation (simulation-based cross-check)

The workbook uses a listed AAPL $250 call option as an example, with market inputs sourced from Bloomberg. The framework is designed so that the key input cells can be replaced to analyze other European vanilla call options.

## Files

- `European Vanilla Call Option Valuation.xlsx` – main Excel model
- `AAPL Option Valuation Memo.pdf` – one-page summary of methodology, results, and conclusions

## Key Inputs in the AAPL Example

- Underlying: AAPL
- Spot price: $247.99
- Strike price: $250
- Time to maturity: 0.5 years
- Risk-free rate: 3.74%
- Dividend yield: 0.42%
- Implied volatility: 31.07%
- Historical volatility: 22.56%

## Main Findings

- Under a common volatility assumption, the three pricing methods produced broadly similar values.
- The larger valuation difference came from the volatility input rather than the method itself.
- Using implied volatility produced values much closer to the observed Bloomberg market midpoint than using historical volatility.

## How to Use the Excel Model

The workbook is organized into separate sections for:

- Pricing summary
- Black-Scholes-Merton model
- Binomial tree model
- Monte Carlo model
- Sensitivity and scenario analysis
- Supporting data sourced from Bloomberg

### Input convention
**Blue font** denotes user-editable inputs (e.g., strike price, risk-free rate, and dividend yield), which can be updated to re-run the valuation.

To use the framework for another European vanilla call option, replace the blue fonts with new assumptions and data. The black fonts will update accordingly.

## Notes

- This framework is intended for **European vanilla call options** only.
- It does not capture early exercise, path dependency, stochastic volatility, or other more complex option features.
- For listed options, implied volatility is generally the more market-consistent input when comparing theoretical values against observed market prices.

## Possible Extensions

Future extensions could include:

- American option pricing
- Delta-hedged trading interpretation
- Python version of the full framework
