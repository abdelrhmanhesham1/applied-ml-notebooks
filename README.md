# Applied ML Notebooks

A collection of applied machine learning mini-projects — regression, classification, and interactive dashboards — plus a separate folder of fundamentals coursework. Each project is self-contained: its own notebook, README, and real result screenshots.

## Projects

| Project | Task | Result |
|---|---|---|
| [California Housing Price Analysis](projects/california-housing-price-analysis/) | EDA + from-scratch gradient descent (batch/stochastic/mini-batch/momentum) | `MedInc` strongest predictor, r = 0.69 |
| [Diamond Price Prediction](projects/diamond-price-prediction/) | Random Forest + XGBoost regression, tuned | XGBoost RMSE ≈ $437, R² = 0.991 |
| [Egypt Gold Price Forecasting](projects/egypt-gold-price-forecasting/) | Linear regression on macroeconomic indicators | Test R² = 0.980, RMSE ≈ 105 EGP |
| [Housing Price Prediction](projects/housing-price-prediction/) | Custom normal-equation regression vs. scikit-learn vs. polynomial+Ridge | Polynomial model R² = 0.9974 |
| [COVID-19 Data Pipeline & Dashboard](projects/covid19-data-pipeline-dashboard/) | Data cleaning pipeline + interactive Dash dashboard | Country/date-filtered live dashboard |
| [Laptop Recommendation Dashboard](projects/laptop-recommendation-dashboard/) | Random Forest classifier + interactive Dash UI | 98% test accuracy (synthetic data) |

Fundamentals practice notebooks (Python basics, regression/classification walkthroughs) live separately in [`coursework/`](coursework/) — see that folder's README for why they're organized apart from the projects above.

## Tech Stack

Python · pandas · NumPy · scikit-learn · XGBoost · Matplotlib · Seaborn · Plotly · Dash

## Repository Structure

```
applied-ml-notebooks/
├── README.md                                  <- you are here
├── CERTIFICATES.md
├── projects/
│   ├── california-housing-price-analysis/
│   ├── diamond-price-prediction/
│   ├── egypt-gold-price-forecasting/
│   ├── housing-price-prediction/
│   ├── covid19-data-pipeline-dashboard/
│   └── laptop-recommendation-dashboard/
└── coursework/
    ├── README.md
    ├── 01_python_fundamentals.ipynb
    ├── 02_linear_regression_methods.ipynb
    ├── 03_classification_and_titanic.ipynb
    └── 04_practice_exercises.ipynb
```

## How to Run

Every project notebook carries an "Open in Colab" badge for zero-setup viewing, or run locally:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost dash jupyter-dash plotly missingno
jupyter notebook
```

Each project's own README documents its exact dependencies and any dataset download steps.

## Social Links

- **Portfolio:** [abdelrhman-hesham.vercel.app](https://abdelrhman-hesham.vercel.app)
- **GitHub:** [github.com/abdelrhmanhesham1](https://github.com/abdelrhmanhesham1)
- **LinkedIn:** [linkedin.com/in/abdelrhman-hesham11](https://www.linkedin.com/in/abdelrhman-hesham11/)
- **Email:** abdelrhmanhesham030@gmail.com
