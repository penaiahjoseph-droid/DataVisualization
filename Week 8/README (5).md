# Student Performance Analysis

## Project Overview
This project analyzes students' academic performance using Python, Pandas, NumPy, Matplotlib, and Seaborn. It explores math, reading, and writing scores alongside demographic and educational background information.

## Objectives
- Load and inspect the StudentsPerformance dataset.
- Explore dataset structure, columns, dimensions, and summary statistics.
- Compare average subject scores across parental education groups.
- Explore relationships among math, reading, and writing scores.
- Compare average scores by lunch type and test preparation course.

## Technologies Used
- **Python** – programming language
- **Pandas** – data loading, cleaning, grouping, and analysis
- **NumPy** – numerical computing
- **Matplotlib** – chart creation
- **Seaborn** – statistical visualizations

## Dataset
The notebook reads a CSV file named `StudentsPerformance.csv`. The columns used include:
- `gender`
- `race/ethnicity`
- `parental level of education`
- `lunch`
- `test preparation course`
- `math score`
- `reading score`
- `writing score`

Place the CSV file in your environment and update the file path in the notebook as needed.

## Analysis Performed
1. **Data inspection**
   - Displays the first and last rows.
   - Checks data types and non-null counts.
   - Examines column names, dataset shape, and descriptive statistics.

2. **Column selection and category exploration**
   - Separates score columns from demographic columns.
   - Checks unique values for gender, parental education, lunch, and test preparation course.

3. **Average scores by parental education**
   - Groups the data by parental education level.
   - Calculates mean math, reading, and writing scores.
   - Displays the averages in a grouped bar chart.

4. **Score relationships**
   - Uses a pair plot to visualize relationships between math, reading, and writing scores.
   - Creates a correlation matrix and heatmap for the three subjects.

5. **Group-wise comparisons**
   - Prints average subject scores by parental education level.
   - Prints average subject scores by lunch type.
   - Prints average subject scores by test preparation course.

## How to Run
1. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
2. Ensure `StudentsPerformance.csv` is available.
3. Update the CSV path in the notebook or Python script. For example:
   ```python
   df = pd.read_csv("StudentsPerformance.csv")
   ```
4. Run `week_8.py` in Python or open `week_8.ipynb` in Jupyter Notebook / Google Colab.

## Output
The program displays dataset previews and information, summary details, category values, a grouped bar chart of average scores by parental education, a pair plot, a correlation heatmap, and printed group-wise averages.

## Notes
- The current script uses a Google Colab file path (`/content/drive/MyDrive/Colab Notebooks/StudentsPerformance.csv`). Change it if you run the project locally.
- The script includes a title and labels for a test-preparation score plot, but the provided code does not calculate or plot grouped averages in that section. Add the relevant plotting code if that chart is required.

## Conclusion
This project provides an introductory exploratory analysis of student performance and visualizes how subject scores relate to parental education, lunch type, and test preparation course.
