# Bloomberg Data Scientist Case Study: Flight Delay Analysis

Analysis of 2024 U.S. flight operations from the BTS Reporting Carrier
On-Time Performance dataset (~7M completed flights), with a pre-flight
model predicting whether a flight will arrive 15+ minutes late.

## Files

- `Flight_EDA_Bloomberg_takehome_CynthiaCao.ipynb` — Full analysis notebook
  with EDA, feature engineering, model training, and evaluation
- `Bloomberg_Takehome_Challenge_CynthiaCao.pdf` — Summary report

## Key Findings

- 20.8% of completed flights arrived 15+ minutes late in 2024
- Delay rates rise from ~9% (early morning) to ~30% (7-8 PM departures)
- XGBoost with threshold tuned to 0.20 achieves ROC-AUC 0.62 on
  Oct-Dec holdout, catching 67% of delays at 21% precision

## Methodology Highlights

- Strict pre-flight feature constraint (no leakage from actual departure
  times or delay-cause fields)
- Rolling monthly cross-validation to mimic production deployment
- Threshold tuning calibrated to delay-screening use case (recall-focused)
- Honest reporting of distribution shift between CV and holdout

## Author

Cynthia Cao | June 2026
