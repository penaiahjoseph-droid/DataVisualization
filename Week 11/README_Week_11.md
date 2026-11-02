# Week 11 – Automobile Dataset Data Cleaning and Feature Engineering

## 1. Introduction
The Automobile Dataset contains technical specifications, engine characteristics, fuel consumption details, and pricing information for different automobile models. This project uses Python data analysis libraries to inspect, clean, transform, and summarize the dataset.

## 2. Problem Statement
Automobile datasets may contain missing values, inconsistent data types, and non-standard missing-value markers such as `?`. These issues can affect calculations and comparisons. The goal is to clean the dataset, convert technical columns into suitable numerical types, create useful features, and produce grouped statistical summaries.

## 3. Objectives
- Understand the structure and characteristics of the Automobile Dataset.
- Identify and replace non-standard missing-value markers.
- Impute missing numerical values using make-wise medians, with overall medians as a fallback.
- Convert technical specifications to numerical data types.
- Create power-to-weight ratio and combined MPG features.
- Compare automobile specifications across body styles and engine locations.
- Export the cleaned dataset as `automobile_cleaned.csv`.

## 4. Libraries Used
- **Pandas** – loading, cleaning, transforming, grouping, and exporting tabular data.
- **NumPy** – handling missing values and numerical operations.
- **Matplotlib** – plotting and visualization support.
- **Seaborn** – statistical visualization support.

## 5. Dataset
The program loads a CSV file containing automobile attributes such as make, body style, engine location, horsepower, peak RPM, bore, stroke, price, engine size, curb weight, city MPG, and highway MPG.

**Input file:** `Automobile.csv` (change the filename/path in the code if your file has a different name).

## 6. Tasks Performed

### Task 1: Import Libraries and Load the Dataset
Imports the required libraries and displays the first and last five rows, dataset dimensions, and column names.

### Task 2: Understand Dataset Structure
Displays data types, non-null counts, descriptive statistics, and lists of categorical and numerical columns.

### Task 3: Detect and Replace Missing Values
Replaces `?` markers with `NaN`, then reports missing-value counts and percentages for each column.

### Task 4: Handle Missing Values
Converts selected technical columns to numeric values. Missing values in `horsepower`, `peak-rpm`, `bore`, `stroke`, and `price` are filled using the median within each automobile make. Any remaining missing values in those columns are filled using the overall column median.

### Task 5: Convert Numerical Data Types
Converts `horsepower` to a nullable integer type (`Int64`) and converts `peak-rpm`, `price`, `bore`, and `stroke` to floating-point values.

### Task 6: Power-to-Weight Ratio
Creates `power_to_weight_ratio` using:

`(horsepower / curb-weight) * 1000`

This represents horsepower per 1,000 units of curb weight as recorded in the dataset.

### Task 7: Combined Fuel Efficiency
Creates `combined_mpg` using:

`(city-mpg + highway-mpg) / 2`

This is a simple arithmetic average, not an official EPA combined fuel-economy calculation.

### Task 8: Statistical Summary by Body Style
Groups records by `body-style` and calculates average horsepower, engine size, curb weight, price, and combined MPG.

### Task 9: Statistical Summary by Engine Location
Groups records by `engine-location` and calculates average horsepower, engine size, curb weight, and price.

### Task 10: Export the Dataset
Exports the transformed dataset to `automobile_cleaned.csv` without including the DataFrame index.

## 7. Output
The project produces:
- Dataset preview and structure information.
- Missing-value counts and percentages.
- Updated numerical data types.
- The `power_to_weight_ratio` feature.
- The `combined_mpg` feature.
- Statistical summaries by body style and engine location.
- **`automobile_cleaned.csv`** – the cleaned and transformed dataset.

## 8. How to Run
1. Install the required libraries if they are not already installed:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
2. Place the automobile CSV dataset in your working folder.
3. Update the `pd.read_csv(...)` path in `week_11.py` to match the location and filename of your dataset.
4. Run the Python script or execute the cells in `Week_11.ipynb`.
5. Find `automobile_cleaned.csv` in the current working directory.

## 9. Conclusion
This project demonstrates a basic data-cleaning and feature-engineering workflow using Pandas and NumPy. It identifies missing values, prepares selected columns for numerical analysis, creates additional automobile performance and fuel-efficiency features, compares groups of vehicles, and exports the resulting dataset for further analysis.
