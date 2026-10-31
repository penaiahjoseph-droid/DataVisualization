# Week 9 – House Sales Data Cleaning and Outlier Detection

## Project Overview
This project uses Python to explore and clean house sales data. It checks the dataset structure, handles duplicate and invalid values, creates additional features, and identifies unusual house sale prices using the Interquartile Range (IQR) method.

## Objectives
- Explore the house sales dataset.
- Check dataset dimensions, columns, summary statistics, and missing values.
- Remove duplicate records.
- Clean bedroom and bathroom values.
- Convert date and year columns to appropriate data types.
- Calculate house age and years since renovation.
- Calculate price per square foot for living area and lot area.
- Detect house-price outliers and visualize them with a box plot.
- Save the cleaned dataset as a CSV file.

## Technologies Used
- **Python** – programming language
- **Pandas** – data loading, inspection, and cleaning
- **NumPy** – numerical operations and conditional calculations
- **Matplotlib** – plotting support
- **Seaborn** – box plot visualization
- **Jupyter Notebook / Google Colab** – running the analysis

## Dataset
The script reads a CSV file named `kc_house_data.csv`.

The analysis uses fields including:
- `price`
- `date`
- `bedrooms`
- `bathrooms`
- `sqft_living`
- `sqft_lot`
- `yr_built`
- `yr_renovated`

The exact columns available depend on the input CSV file.

## Project Workflow

### 1. Load and Explore the Data
The dataset is loaded with Pandas. The notebook checks:
- First and last rows
- Data types and non-null counts
- Descriptive statistics
- Number of rows and columns
- Column names
- Missing-value counts

### 2. Clean the Data
- Remove duplicate rows.
- Convert `bedrooms` and `bathrooms` to numeric values.
- Treat values less than or equal to zero in those columns as missing.
- Fill missing bedroom and bathroom values with their respective medians.
- Convert `date` to datetime format.
- Convert `yr_built` and `yr_renovated` to numeric values.

### 3. Feature Engineering
The script creates these columns:
- `sale_year`: year extracted from the sale date.
- `house_age`: sale year minus the year the house was built.
- `years_since_renovation`: sale year minus renovation year, when a valid renovation year greater than zero exists.
- `price_per_sqft_living`: sale price divided by living area when living area is positive.
- `price_per_sqft_lot`: sale price divided by lot area when lot area is positive.

Negative house ages and negative years since renovation are changed to missing values.

### 4. Detect Price Outliers
The project uses the Interquartile Range (IQR) method:
- `Q1`: 25th percentile of house prices.
- `Q3`: 75th percentile of house prices.
- `IQR`: `Q3 - Q1`.
- Lower bound: `Q1 - 1.5 × IQR`.
- Upper bound: `Q3 + 1.5 × IQR`.

Rows with prices outside these bounds are marked as outliers in the `valuation_outlier` column. The script prints the bounds and the number of outliers, displays selected columns for those rows, and plots house prices using a Seaborn box plot.

**Note:** Outliers are flagged, not removed, by this script.

### 5. Export the Cleaned Data
The final dataset is saved as `cleaned_house_sales.csv`, including the added feature and outlier-flag columns.

## How to Run

1. Install Python if needed.
2. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. Place `kc_house_data.csv` in the location expected by the script, or update the CSV path in `week_9.py`.
4. Run the script:

   ```bash
   python week_9.py
   ```

   Alternatively, open `Week_9.ipynb` in Jupyter Notebook or Google Colab and run the cells.

## Output
- Dataset exploration and summary information in the console/notebook.
- Price outlier bounds and outlier count.
- A box plot titled **House Price Outlier Detection**.
- Selected records identified as price outliers.
- `cleaned_house_sales.csv` containing the processed data.

## Project Structure

```text
.
├── week_9.py
├── Week_9.ipynb
├── kc_house_data.csv
└── cleaned_house_sales.csv   # generated after running the project
```

## Conclusion
This project demonstrates basic data exploration, data cleaning, feature engineering, and outlier detection using Python libraries. The resulting CSV file can be used for further house-sales analysis.

## Limitations
- The input file must contain the columns referenced by the script.
- The script expects the CSV file at `/kc_house_data.csv` unless its path is changed.
- Missing values in columns other than bedrooms and bathrooms are not generally filled by this script.
- Price outliers are marked rather than deleted.
