# Superstore Sales & Profit Analysis (Task 1 — BDA)

Exploratory Data Analysis (EDA) on the **Sample Superstore** dataset, examining sales, profit, discounts, delivery time, and correlations between key business metrics.

## Overview

This project loads retail order data and explores:
- Sales performance across product categories
- Profit distribution and variation across categories
- The relationship between discounting and profitability
- Delivery time (days between order and shipment)
- Correlations between numeric features (Sales, Profit, Discount, Quantity, Delivery Days)

## Dataset

- **File:** `samplesuperstore.csv`
- **Expected location:** `/content/samplesuperstore.csv` (Google Colab path — update if running locally)
- **Key columns used:**
  - `Order Date`, `Ship Date` — used to compute `Delivery Days`
  - `Category` — product category
  - `Sales`, `Profit`, `Discount`, `Quantity` — numeric business metrics

## Requirements

```
pandas
numpy
matplotlib
seaborn
```

Install with:

```bash
pip install pandas numpy matplotlib seaborn
```

## Project Structure

```
.
├── Task_1_BDA.ipynb   # Jupyter/Colab notebook with full analysis
├── task_1_bda.py       # Script version of the same analysis
└── README.md
```

## How to Run

1. Place `samplesuperstore.csv` in the same directory (or update the `pd.read_csv(...)` path in the code).
2. Run the notebook cell-by-cell in Jupyter/Colab, **or** run the script directly:

```bash
python task_1_bda.py
```

## Analysis Steps

1. **Load & inspect data** — `df.head()`, `df.info()`, `df.describe()`
2. **Clean & engineer features**
   - Convert `Order Date` and `Ship Date` to `datetime`
   - Compute `Delivery Days = Ship Date - Order Date`
   - Check for missing values (`df.isnull().sum()`)
3. **Sales by category** — grouped totals + bar chart
4. **Sales distribution** — histogram of `Sales`
5. **Profit by category** — bar plot and box plots (overall and by category)
6. **Discount vs. profit** — scatter plot showing how discounts affect profitability
7. **Correlation analysis** — correlation matrix and heatmap across numeric columns

## Key Outputs

- Bar chart: Total Sales by Category
- Histogram: Sales Distribution
- Bar/box plots: Profit by Category
- Scatter plot: Discount vs. Profit
- Heatmap: Correlation between numeric variables

## Notes

- No missing values were found in the dataset during the null check.
- Higher discounts generally correlate with reduced (or negative) profit — visible in the discount-vs-profit scatter plot.
