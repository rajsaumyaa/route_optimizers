# Route-optimizers – Traffic Demand Prediction

A machine learning project to forecast traffic demand across urban delivery zones using historical order and traffic data.

## Problem Statement

Predict demand at the zone level to help optimize delivery routing and resource allocation across a logistics network.

## Approach

- **Feature Engineering**: Applied geohash-based target encoding to convert raw latitude/longitude coordinates into grid-level demand signals, capturing spatial patterns that raw coordinates would miss.
- **Temporal Features**: Extracted hour-of-day, day-of-week, and lag-based features to capture time-dependent demand patterns.
- **Modeling**: Trained an ensemble of LightGBM, XGBoost, and CatBoost models, each tuned via grid search and validated using k-fold cross-validation.
- **Blending**: Combined predictions from all three models using weighted averaging for the final output.

## Results

- Achieved a leaderboard score of **91.38** on the held-out test set.

## Tech Stack

Python, Pandas, NumPy, Scikit-learn, LightGBM, XGBoost, CatBoost

## Project Structure

```
## Project Structure

├── route_optimizers.ipynb        # End-to-end notebook: preprocessing, feature engineering, model training, and blending
├── approach_route_optimizers.txt # Detailed write-up of approach, methodology, and design decisions
├── ppt_route_optimizers.pptx     # Presentation summarizing problem, approach, and results
└── README.md
```
