# Healthcare Dataset Analysis

## Project Overview
This project analyzes a healthcare dataset containing 55,500 patient records. It uses Python data-analysis libraries to inspect patient information, check data quality, calculate hospital stay durations, and compare total billing amounts across medical conditions and insurance providers.

## Objectives
- Load and explore the healthcare dataset.
- Inspect the dataset structure, dimensions, and descriptive statistics.
- Check for missing values and remove incomplete rows.
- Convert admission and discharge dates into datetime format.
- Calculate each patient's hospital stay duration in days.
- Summarize billing amounts by medical condition and insurance provider.
- Visualize billing totals using a stacked bar chart.

## Technologies Used
- **Python** – programming language
- **Pandas** – data cleaning, grouping, and analysis
- **NumPy** – numerical operations
- **Matplotlib** – chart creation
- **Seaborn** – visualization library imported in the notebook

## Dataset
The notebook loads the file `healthcare_dataset (1).csv` from Google Drive:

```python
df = pd.read_csv("/content/drive/MyDrive/Colab Notebooks/healthcare_dataset (1).csv")
```

Update the file path if the dataset is stored in another location.

The dataset contains columns such as:
- `Name`
- `Age`
- `Gender`
- `Blood Type`
- `Medical Condition`
- `Date of Admission`
- `Doctor`
- `Hospital`
- `Insurance Provider`
- `Billing Amount`
- `Room Number`
- `Admission Type`
- `Discharge Date`
- `Medication`
- `Test Results`

The displayed dataset has 55,500 rows and 15 original columns. The notebook adds a `Hospital_Stays` column, giving 16 columns after processing.

## Analysis Workflow
1. Load the healthcare CSV file into a Pandas DataFrame.
2. Inspect the data using `head()`, `shape`, and `describe()`.
3. Check missing values with `isnull().sum()` and remove rows containing missing values using `dropna()`.
4. Convert `Date of Admission` and `Discharge Date` to UTC datetime values.
5. Calculate hospital stay duration:

   `Hospital_Stays = Discharge Date - Date of Admission`

   The duration is converted into a number of days.
6. Group the data by `Medical Condition` and `Insurance Provider`.
7. Calculate the total `Billing Amount` for each group.
8. Plot the results as a stacked bar chart to compare billing totals across medical conditions and insurance providers.

## Visualization
The notebook creates a stacked bar chart titled **“Billing Amount by Medical Condition and Insurance Provider.”**
- X-axis: Medical Condition
- Y-axis: Billing Amount
- Bar segments: Insurance Provider
- Legend: Aetna, Blue Cross, Cigna, Medicare, and UnitedHealthcare

## Installation
Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

## How to Run
1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload the CSV file or mount Google Drive.
3. Confirm that the CSV path in `pd.read_csv()` is correct.
4. Run the notebook cells in order.

## Notes
- The notebook checks for missing values and removes incomplete rows. The displayed output shows no missing values in the original columns.
- The descriptive statistics show some negative values in `Billing Amount`; the current notebook does not remove or correct them.
- The notebook calculates hospital stay duration but does not yet visualize or summarize those durations.
- The billing chart shows total billing amounts, not average bills or patient counts.

## Conclusion
This project demonstrates basic healthcare data exploration, date processing, hospital-stay calculation, grouped billing analysis, and data visualization. The stacked bar chart helps compare billing totals across medical conditions and insurance providers.

## Author
Add your name here.
