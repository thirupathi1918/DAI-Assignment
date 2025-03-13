Exploratory Data Analysis on Match Data

This project performs Exploratory Data Analysis (EDA) on the match dataset (matches.csv). The analysis includes data loading, cleaning, handling missing values, data visualization, and statistical insights into match records.

Understanding the Code


1. Reading the Dataset

The dataset is loaded using pd.read_csv('matches.csv').

The structure of the dataset is examined using:

df.info(): Provides an overview of column names, data types, and missing values.

df.head(): Displays the first few rows for an initial look.

df.describe(): Summarizes numerical columns.

df.columns: Lists all column names.

2. Handling Missing Values

The dataset is checked for missing values using df.isnull().sum().

Missing values in key columns are filled with appropriate placeholders (e.g., 'Unknown').

3. Identifying and Handling Duplicates

Duplicate rows are detected using df.duplicated(keep=False).

If duplicates exist, they are printed for further inspection and removed if necessary.

4. Feature Engineering & Data Transformation

Date-related columns are converted to datetime format using pd.to_datetime().

Categorical variables are analyzed for consistency and reformatted if needed.

5. Data Visualization

Boxplots: Display match durations and score distributions.

Histograms: Show the distribution of match scores over time.

Scatter Plots: Visualize relationships between different match statistics.

Count Plots: Represent categorical distributions, such as match outcomes and venues.

Heatmaps: Display correlations between numerical variables.

6. Outlier Detection & Removal

The Interquartile Range (IQR) method is used to detect and remove outliers in numerical columns.

Boxplots before and after outlier removal illustrate the effect.

7. Finding Mode for All Columns

The most frequent values (mode) in each column are computed using df.mode() to identify dominant trends.

8. Match Trends Over Time

Trends in match statistics are visualized over time using:

Line charts for season-wise analysis.

Stacked bar charts to compare different match outcomes.

Heatmaps for time-based match trends.

Conclusion

This analysis provides insights into match data trends, score distributions, and key match statistics, helping to uncover patterns in the dataset. The findings can be used for predictive analysis and decision-making in match-related analytics.
