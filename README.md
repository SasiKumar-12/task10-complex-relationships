# Task 10 — Complex Relationships

AI/ML Developer · Phase 1 Industry Immersion

## Objective
Model complex, non-linear relationships in data using more expressive algorithms (gradient boosting), validated against a linear baseline.

## Dataset
California Housing dataset (built into scikit-learn) — predicting median house value from features like median income, house age, average rooms, and location.

## Approach
1. Reproducible setup with a fixed random seed
2. Train / validation / test split (70 / 15 / 15)
3. Exploratory data analysis to identify non-linear patterns
4. Linear Regression baseline
5. XGBoost model, tuned via grid search (max_depth, learning_rate, n_estimators, subsample)
6. Partial dependence plots to sanity-check feature effects
7. Final evaluation on a held-out test set

## Results

| Model | R2 | RMSE |
|---|---|---|
| Linear Regression (baseline) | 0.585 | 0.735 |
| XGBoost (tuned, validation) | 0.825 | 0.478 |
| XGBoost (tuned, test) | 0.848 | 0.449 |

## Conclusion
XGBoost significantly outperforms the linear baseline (R2: 0.585 → 0.848), confirming that the data contains meaningful non-linear relationships. Partial dependence plots show sensible feature effects (e.g. price increasing with median income), and the gap between train and validation performance indicates the model is not overfitting. The added model complexity is justified by the validated performance lift.

## How to run