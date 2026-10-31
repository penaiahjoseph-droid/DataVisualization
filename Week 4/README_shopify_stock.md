# Shopify Stock Data Analysis

## Project Overview
This project analyzes Shopify stock market data using Python. It examines stock prices, daily price changes, daily returns, trading volume, and return statistics. It also creates charts to visualize closing-price trends, trading-volume trends, and the distribution of daily returns.

## Objectives
- Load and inspect Shopify stock data.
- Convert the date column to datetime format.
- Check for missing values and remove incomplete rows.
- Remove duplicate records and sort data by date.
- Calculate daily price differences and percentage returns.
- Analyze trading-volume statistics and identify unusually high-volume days.
- Calculate mean, variance, and standard deviation of daily returns.
- Visualize stock price, trading volume, and daily return distribution.

## Technologies Used
- **Python** – programming language
- **Pandas** – data loading, cleaning, and analysis
- **NumPy** – numerical computing
- **Matplotlib** – data visualization
- **Seaborn** – histogram visualization

## Dataset
The notebook loads the file `shopify_stock.csv`:

```python
df = pd.read_csv("shopify_stock.csv")
```

The CSV file should be in the same working directory as the notebook, or the path should be updated to its location.

Columns used in the notebook:
- `date` – stock trading date
- `open` – opening price
- `close` – closing price
- `volume` – trading volume

## Analysis Workflow
1. Load the CSV dataset into a Pandas DataFrame.
2. Inspect the first rows, dataset shape, structure, and descriptive statistics.
3. Convert `date` to datetime format using UTC.
4. Check missing values and remove rows containing missing values.
5. Remove duplicate records.
6. Sort the data by date.
7. Calculate daily price difference:

   `Daily_Delta = close - open`

8. Calculate daily percentage return:

   `Daily_Return = ((close - open) / open) * 100`

9. Calculate average, maximum, and minimum trading volume.
10. Identify anomalous trading days where volume is greater than twice the average volume.
11. Calculate mean return, return variance, and return standard deviation.
12. Plot the closing-price trend, trading-volume trend, and daily-return distribution.

## Installation
Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

## How to Run
1. Place `shopify_stock.csv` in the notebook's working directory.
2. Open `shopify_stock.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
3. Run the cells in order.

The notebook uses `sns.histplot()` for the return-distribution chart, so make sure Seaborn is installed and imported. If you encounter a `NameError` for `sns`, add this import near the top of the notebook:

```python
import seaborn as sns
```

## Expected Output
- Dataset preview and descriptive statistics
- Missing-value and duplicate handling
- Daily price differences and percentage returns
- Trading-volume summary
- List of unusually high-volume trading days
- Mean, variance, and standard deviation of daily returns
- Closing-price trend chart
- Trading-volume trend chart (`chart.png` is saved by the notebook)
- Daily-return distribution histogram

## Conclusion
This project provides an exploratory analysis of Shopify stock data. It summarizes daily price movements and trading activity and uses statistical measures and charts to help understand patterns in the stock dataset.

## Author
Add your name here.
