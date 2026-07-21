# California Housing Price Analysis

Exploratory data analysis of the classic California Housing dataset, paired with a from-scratch implementation of four gradient descent variants — built to understand *how* linear regression converges, not just to call `.fit()`.

## Project Overview

This project analyzes the 1990 California census housing dataset (20,640 block groups) to understand which factors drive median house value, then uses that understanding to train a simple linear model with a hand-written gradient descent optimizer — comparing batch, stochastic, mini-batch, and momentum update rules on the same data.

## Tech Stack

- **Python** — pandas, NumPy
- **Visualization** — Matplotlib, Seaborn, Plotly (Mapbox), missingno
- **Data source** — `sklearn.datasets.fetch_california_housing` (built into scikit-learn, no external file needed)

## Architecture

```mermaid
flowchart LR
    A[fetch_california_housing] --> B[Data Quality Checks]
    B --> C[IQR Outlier Detection & Clipping]
    C --> D[Correlation Analysis]
    D --> E[Gradient Descent: Batch / Stochastic / Mini-batch / Momentum]
    C --> F[Geographic Visualization]
```

## Features

- Missing-value and duplicate checks before any transformation
- IQR-based outlier detection with before/after boxplots and skew comparison
- Correlation matrix + per-feature scatter plots against the target
- **From-scratch gradient descent** — batch, stochastic, mini-batch, and momentum variants implemented in plain NumPy, compared by convergence curve
- Geographic scatter map (Plotly Mapbox) of price by location and house age

## Testing

No automated test suite — this is an analysis notebook. Correctness is validated by comparing the from-scratch gradient descent's cost-convergence behavior against the expected theoretical ordering (momentum ≤ batch < mini-batch < stochastic in stability), and outputs are inspected directly in the notebook cells.

## Folder Structure

```
california-housing-price-analysis/
├── california_housing_price_analysis.ipynb
├── README.md
└── screenshots/
    ├── histograms.png
    ├── correlation-heatmap.png
    ├── scatter-relationships.png
    └── geographic-price-map.png
```

## How to Run the Project

1. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn plotly missingno
   ```
2. Open `california_housing_price_analysis.ipynb` in Jupyter, or click the Colab badge at the top of the notebook.
3. Run all cells top to bottom — the dataset downloads automatically via scikit-learn, no manual data upload needed.

## Future Improvements

- Fit a full multi-feature regression (or gradient boosting) and report held-out RMSE/R² — this notebook stops at single-feature gradient descent by design
- Add k-fold cross-validation to the gradient descent comparison
- Cluster `Latitude`/`Longitude` into regions as a categorical feature
- Cross-check the hand-rolled optimizer against `sklearn.linear_model.SGDRegressor`

## Screenshots

**Feature distributions:**

![Histograms](screenshots/histograms.png)

**Correlation matrix:**

![Correlation heatmap](screenshots/correlation-heatmap.png)

**Feature vs. target relationships:**

![Scatter relationships](screenshots/scatter-relationships.png)

**Geographic price distribution:**

![Geographic price map](screenshots/geographic-price-map.png)

## Social Links

- **Portfolio:** [abdelrhman-hesham.vercel.app](https://abdelrhman-hesham.vercel.app)
- **LinkedIn:** [linkedin.com/in/abdelrhman-hesham11](https://www.linkedin.com/in/abdelrhman-hesham11/)
- **Email:** abdelrhmanhesham030@gmail.com
