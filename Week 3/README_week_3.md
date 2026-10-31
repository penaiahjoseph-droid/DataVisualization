# Week 3 – Apple Stock Data Analysis

## Project Overview
This project analyzes Apple stock market data using Python. It explores stock prices, daily gains and losses, trading volume, and daily returns to understand patterns in the dataset.

## Objectives
- Load and inspect Apple stock data.
- Check missing values and remove duplicate records.
- Convert the `Date` column to datetime format.
- Find the highest and lowest adjusted closing prices.
- Calculate average opening and closing prices.
- Identify the top 10 daily gains and top 10 daily losses.
- Analyze trading volume and detect unusually high-volume trading days.
- Calculate the mean, variance, and standard deviation of daily returns.

## Technologies Used
- Python
- Pandas – data loading and analysis
- NumPy – numerical computing
- Matplotlib – data visualization

## Dataset
The notebook reads `Apple_stock.csv.csv` and expects it at:

```text
/content/drive/MyDrive/Apple_stock.csv.csv
```

Update the path if the file is stored elsewhere.

Columns used by the code:
- `Date` – stock trading date
- `Open` – opening price
- `Close` – closing price
- `Adj Close` – adjusted closing price
- `Volume` – number of shares traded

## Analysis Workflow
1. Load the CSV file into a Pandas DataFrame.
2. Inspect sample rows, dataset dimensions, column information, descriptive statistics, and missing-value counts.
3. Convert `Date` to datetime format using UTC.
4. Remove duplicate rows and check missing values again.
5. Find the maximum and minimum `Adj Close` values.
6. Calculate the average opening and closing prices.
7. Sort by date and calculate the daily price difference:

   `Daily_Delta = Close - Open`

8. Display the 10 records with the largest daily price differences.
9. Calculate daily percentage return:

   `Daily_Return = ((Close - Open) / Open) * 100`

10. Display the 10 records with the lowest daily returns.
11. Calculate average, maximum, and minimum trading volume.
12. Identify anomalous trading days where volume is greater than twice the average volume.
13. Calculate the mean, variance, and standard deviation of daily returns.

## Installation
Install the required libraries:

```bash
pip install pandas numpy matplotlib
```

## How to Run
### Google Colab or Jupyter Notebook
1. Open `Week_3.ipynb`.
2. Upload or mount the folder containing `Apple_stock.csv.csv`.
3. Ensure the CSV path in the code is correct.
4. Run the notebook cells in order.

### Python script
```bash
python week_3.py
```

Make sure the CSV file is available at the path specified in the script.

## Expected Output
The notebook displays:
- Dataset preview, shape, structure, descriptive statistics, and missing-value counts
- Highest and lowest adjusted closing prices
- Average opening and closing prices
- Top 10 daily gains and losses
- Trading-volume statistics
- Anomalous high-volume trading days
- Mean, variance, and standard deviation of daily returns

## Conclusion
This project performs exploratory analysis of Apple stock data. It summarizes price behavior, daily returns, and trading volume, and identifies large price movements and unusually high trading activity.

## Author
Add your name here.
