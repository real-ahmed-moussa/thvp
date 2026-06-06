# Model Results — Taipei House Value Prediction

All metrics are 10-fold cross-validated MSE (5 re-shuffles). Results are as originally obtained; `set.seed(42)` is used throughout.

## Primary Results

| Model | Optimal Hyperparameters | CV MSE |
|---|---|---|
| GAM (Backfitting) | df = (3, 8, 6, 3, 6, 7) per predictor | **58.80** |
| MARS | degree = 1, nk = 10 | 61.07 |
| Ridge Regression | scaling = "scale", λ = 10 | 80.06 |

GAMs achieved the lowest MSE — **26% lower than Ridge** and 3.7% lower than MARS.

## Ridge Regression — All Scaling Methods

| Scaling | Optimal λ | CV MSE |
|---|---|---|
| Scale (standardised) | 10 | **80.06** |
| None (raw) | 0.005 | 80.08 |
| CorrForm | 0.05 | 80.09 |

All three scaling variants produce similar MSE, confirming that Ridge's performance ceiling is set by the linearity assumption rather than the choice of regularisation scale.

## GAM — Optimal Degrees of Freedom per Predictor

| Predictor | Optimal df |
|---|---|
| Transaction date (`tr_date`) | 3 |
| House age (`house_age`) | 8 |
| Distance to MRT (`dist_mrt`) | 6 |
| Convenience stores (`n_stores`) | 3 |
| Latitude (`lat`) | 6 |
| Longitude (`long`) | 7 |

The high df for `house_age` (8) reflects its parabolic U-shaped relationship with price. The moderate df for `dist_mrt` (6) captures the rapid inverse-decay curve.
