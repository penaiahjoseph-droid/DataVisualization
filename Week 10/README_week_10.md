# Week 10 – Real Estate Investment Analysis

## Project Overview
This project analyzes house/property data to understand how property prices relate to living area, property grade, waterfront status, and geographic location. It uses data analysis, visualization, location clustering, and simple linear regression.

## Objectives
- Explore and clean the house-price dataset.
- Study the relationship between living area and property price.
- Compare property prices across property grades.
- Compare prices for waterfront and non-waterfront properties.
- Visualize property prices geographically.
- Identify high-value location clusters.
- Build a simple linear regression model to examine the relationship between living area and price.

## Technologies Used
- Python
- Pandas – data loading, cleaning, and analysis
- Matplotlib – plotting and chart output
- Seaborn – statistical visualizations
- Scikit-learn – linear regression

## Dataset
The project reads `kc_house_data.csv`, a house-sales dataset. The script expects the file at `/kaggle/kc_house_data.csv`.

Important columns used:
- `price` – property price
- `sqft_living` – interior living area in square feet
- `grade` – property grade
- `waterfront` – waterfront indicator
- `lat` – latitude
- `long` – longitude

Make sure the CSV path matches your environment before running the script.

## Workflow
1. Load the CSV dataset with Pandas.
2. Inspect the data using `head()`, `tail()`, `info()`, `columns`, and `shape`.
3. Convert selected columns to numeric values.
4. Remove rows missing required values and rows with non-positive prices or living areas.
5. Generate visualizations for price versus living area, grade, waterfront status, and geographic location.
6. Group locations by rounded latitude and longitude and calculate property counts, average prices, median prices, and average living areas.
7. Keep location clusters with at least five properties, sort by average price, and export the cluster results to CSV.
8. Fit a linear regression model using living area to estimate its relationship with property price.
9. Print a real-estate investment summary.

## Visualizations and Output Files
The script creates the following image files:
- `living_area_vs_price.png` – living area versus price with a regression line
- `price_by_grade.png` – price distribution by property grade
- `price_by_waterfront.png` – price comparison by waterfront status
- `geographic_price_heatmap.png` – geographic property-price scatter plot
- `high_value_location_clusters.csv` – location-cluster summary sorted by average price

The terminal output includes the top 10 high-value location clusters and summary statistics such as the number of properties analyzed, average price, median price, average living area, regression coefficient, and R-squared score.

## Installation
Install the required libraries:

```bash
pip install pandas matplotlib seaborn scikit-learn
```

## How to Run
1. Download or place `kc_house_data.csv` in your working directory.
2. Update the path in `week_10.py` if needed:

```python
df = pd.read_csv("/kaggle/kc_house_data.csv")
```

3. Run the Python file:

```bash
python week_10.py
```

Alternatively, open `week_10.ipynb` in Jupyter Notebook or Google Colab and run the cells. Ensure the dataset path is valid in that environment.

## Model Note
The linear regression model uses only `sqft_living` as its input feature and `price` as the target. It is a simple relationship analysis, not a complete property valuation or investment recommendation. The coefficient and R-squared value are calculated from the cleaned dataset.

## Conclusion
This project provides an exploratory view of real-estate prices by living area, property grade, waterfront status, and geographic location. It also produces location-cluster summaries and a basic regression analysis that can help identify patterns in the dataset.

## Author
Add your name here.
