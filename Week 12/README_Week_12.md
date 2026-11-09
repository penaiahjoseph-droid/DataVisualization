# Week 12 – Automobile Data Visualization and Market Analysis

## 1. Introduction
This project analyzes automobile technical specifications, fuel efficiency, and selling prices using Python data analysis and visualization libraries. Visualizations help explore relationships between engine performance, vehicle weight, mileage, body style, fuel type, and price.

## 2. Problem Statement
Automobile manufacturers need to understand how vehicle performance, fuel efficiency, size, and pricing relate to each other. This project uses statistical summaries and visualizations to compare automobile categories, explore price patterns, and examine manufacturer-level market positioning.

## 3. Objectives
- Analyze relationships between horsepower, engine size, price, and fuel efficiency.
- Compare automobile prices across body styles.
- Examine pricing patterns by fuel type and engine type.
- Visualize correlations between technical specifications.
- Compare average prices across manufacturers.
- Explore the balance between horsepower, vehicle weight, and combined MPG.
- Prepare a competitive market positioning summary.

## 4. Libraries Used
- **Pandas** – loading, grouping, and summarizing tabular data.
- **NumPy** – numerical operations and data handling.
- **Matplotlib** – creating charts and plots.
- **Seaborn** – statistical visualizations.

## 5. Dataset
The notebook loads automobile data from a CSV file. To continue from Week 11, use the cleaned output from the previous week.

**Recommended input file:** `automobile_cleaned.csv`

Update the `pd.read_csv(...)` path if the CSV is stored in another folder. The dataset should contain columns such as `make`, `fuel-type`, `engine-type`, `body-style`, `horsepower`, `price`, `engine-size`, `curb-weight`, `city-mpg`, and `highway-mpg`. The Week 11 engineered features are `combined_mpg` and `power_to_weight_ratio`.

## 6. Tasks Performed

### Task 1: Load and Inspect the Dataset
Loads the CSV and displays sample records, dimensions, column names, data types, and missing-value counts. It checks whether the engineered features are available.

### Task 2: Horsepower vs. Price
Creates a scatter plot with horsepower on the x-axis, price on the y-axis, and fuel type shown by color. The correlation value describes the linear association between horsepower and price.

### Task 3: Engine Size vs. City MPG
Creates a scatter plot to explore the relationship between engine size and city fuel efficiency, with points colored by fuel type.

### Task 4: Price Distribution Across Body Styles
Uses a box plot to compare price distributions by body style, including medians, spread, and potential outliers.

### Task 5: Fuel Type and Engine Type Pricing
Calculates average prices grouped by fuel type and engine type and presents the comparison in a grouped bar chart.

### Task 6: Technical Specification Correlation Heatmap
Calculates Pearson correlations for available numerical specifications, such as engine size, horsepower, vehicle dimensions, MPG, curb weight, price, and engineered features when present. Correlation indicates association, not causation.

### Task 7: Brand-Level Market Positioning
Groups vehicles by manufacturer and compares average prices, horsepower, and combined MPG. A bar chart compares average prices by manufacturer.

### Task 8: Performance vs. Fuel Efficiency
Creates a bubble scatter plot with horsepower on the x-axis, combined MPG on the y-axis, bubble size representing curb weight, and color representing fuel type. It also displays up to ten vehicles with the highest combined MPG.

### Task 9: Competitive Market Positioning Summary
Prints the vehicle count, average price, average price by body style, horsepower-price correlation, engine-size-city-MPG correlation, and average price by manufacturer. These results can support a written business interpretation.

## 7. Visualizations and Outputs
- Horsepower vs. price scatter plot.
- Engine size vs. city MPG scatter plot.
- Price distribution box plot by body style.
- Grouped bar chart for fuel type and engine type pricing.
- Correlation heatmap for numerical specifications.
- Average-price bar chart by manufacturer.
- Performance vs. fuel-efficiency bubble plot.
- Printed statistical summaries for the market positioning report.

## 8. How to Run
1. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
2. Place `automobile_cleaned.csv` in the working directory, or update the CSV path in the notebook.
3. Open `Week_12.ipynb` in Jupyter Notebook or Google Colab, or run `week_12.py`.
4. Execute the cells from top to bottom.
5. Review the charts and printed summaries.

## 9. Conclusion
This project uses visualization and descriptive statistics to examine automobile pricing, technical specifications, fuel efficiency, and manufacturer-level differences. The charts and summaries support market comparisons and product-positioning discussions. Interpret findings in the context of the dataset, and do not treat correlation as proof of causation.
