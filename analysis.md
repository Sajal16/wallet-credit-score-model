# 📊 Analysis of Wallet Credit Score

## Dataset Overview
- Total wallets analyzed: 3497
- Common columns:
  - `repay_borrow_ratio`
  - `deposit_count`
  - `active_days`
  - `liquidation_count`

## Feature Insights
- Many wallets had **0 active days** and **0 deposits**.
- `repay_borrow_ratio` shows extreme outliers (handled by log-scaling).
- Liquidation is low for most users, but a few have many.

## Score Distribution
- Most scores were **very low**.
- A few wallets had very high scores due to perfect repay/deposit behavior.

## Risk Classification
- Majority of wallets fell into **High Risk**.
- Very few had low risk due to better financial behavior.

## Suggestions
- Consider adding more behavioral features (like wallet age or asset diversity).
- Better normalization for extreme ratios may help.

