# The "Dollar Smile": A Quantitative Analysis of USD Regimes and Their Impact on Cross-Asset Performance

## Project Description

This project provides a quantitative framework to validate the "Dollar Smile" theory through data-driven analysis of USD market regimes and their impact on cross-asset performance. Using 2020-2024 financial data, we developed a rule-based model that **successfully validates all three core predictions** of the Dollar Smile theory with statistically significant results.

## Key Findings Summary

**Dollar Smile Theory VALIDATED** - All three predictions confirmed with statistical significance  
**4 Distinct Regimes Identified** - Clear historical patterns aligned with major market events  
**Dramatic Performance Differences** - Up to 115% annualized return spread between regimes

## Research Questions and Answers

### 1. Can we quantitatively define USD market regimes?
**YES** - Successfully identified four distinct regimes:
- **Risk-Off Dollar Strength**: 168 days (16.7%) - COVID crash, 2022 stress
- **Pro-Growth Dollar Strength**: 128 days (12.7%) - 2021 bull market  
- **Dollar Weakness**: 394 days (39.2%) - 2022-2023 period
- **Neutral/Sideways**: 266 days (26.4%) - baseline conditions

### 2. How do asset classes perform within each regime?

| Regime | SPY Return | EEM Return | GLD Return |
|--------|------------|------------|------------|
| **Risk-Off Dollar** | -22.1% | **-48.9%** | -8.0% |
| **Pro-Growth Dollar** | **+66.7%** | +34.8% | +7.5% |
| **Dollar Weakness** | +28.1% | **+35.1%** | +17.6% |

### 3. Do relationships remain stable across cycles?
**YES** - Statistical significance confirmed (EEM p-value = 0.047)

## Regime Classification Model

```python
# Rule-based classification using dynamic thresholds
Risk-Off Dollar Strength:    VIX > 26.3 AND DXY_ROC_50d > 0
Pro-Growth Dollar Strength:  VIX < 17.3 AND DXY_ROC_50d > 0  
Dollar Weakness:             DXY_ROC_50d < 0
Neutral/Sideways:           All other periods
```

## Dataset & Implementation

**Data Sources**: Yahoo Finance (SPY, EEM, GLD, DXY, VIX)  
**Time Period**: 2020-2024 (~1,000 trading days)  
**Tools**: Python, pandas, yfinance, matplotlib, scipy

## Investment Applications

### Tactical Asset Allocation
- **Risk-Off**: Reduce emerging market exposure
- **Pro-Growth**: Overweight U.S. equities (7.43 Sharpe ratio)
- **Dollar Weakness**: Tilt toward emerging markets (+35% vs +28%)

### Risk Management
- Monitor VIX (26.3/17.3 thresholds) and DXY 50-day ROC as early indicators
- Implement regime-specific hedging strategies
- Dynamic position sizing based on regime volatility

## Key Visualizations

- **Regime Timeline**: SPY price evolution colored by regime type
- **Performance Comparison**: Cross-regime return and Sharpe ratio analysis  
- **Statistical Validation**: ANOVA results and significance testing

- **Final Project Paper**: [View PDF](./Project-Final-Report.pdf)
