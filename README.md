# Nepal-Disaster-Analysis-using-Machine-Learning-Models

The script is a comprehensive implementation of loss detection and analysis using a dataset of disaster incidents in Nepal. Here's an overview of the key steps in the code:

1.Data Import and Preprocessing

Libraries: Uses libraries like pandas, numpy, matplotlib, seaborn, and statsmodels for data handling, visualization, and statistical analysis.

Dataset Import: The dataset is read from a CSV file containing details of various disasters.

Preprocessing:
Drops unnecessary columns (e.g., S.No., Remarks).
Removes rows with missing values in important columns (Estimated Loss, District).
Converts certain numerical columns to their absolute values (e.g., Injured, Affected Family).

2. Feature Engineering

Categorical Grouping:
Assigns districts to provinces (like Koshi, Madhesh) based on mappings.

Temporal Features:
Extracts year and season (e.g., Spring, Winter) from the incident date.

New Features:
Combines damages to compute houses_fully_destroyed and houses_partially_destroyed.

Disaster Categories:
Consolidates disaster names into key categories (e.g., Earthquake, Flood, Fire, Landslide).

3. Exploratory Data Analysis (EDA)

Summarization: Basic stats like describe() and value counts for categorical columns.

Visualizations:
Pie charts and count plots for disaster distribution across provinces and seasons.
Time-series analysis of disaster frequency and cumulative loss over years.
Correlation heatmaps for numerical features.

4. Predictive Modeling

Feature Selection:
Uses Recursive Feature Elimination (RFE) with LinearRegression to select key predictors for Estimated Loss.

Model Building:
Implements multiple iterations of Ordinary Least Squares (OLS) regression using statsmodels to refine the model by dropping insignificant features.
Final predictors include Affected Family and Summer season.

Evaluation:
Tests the model on a separate dataset.
Computes the R² score to measure the predictive power.
Scatterplot to compare actual (y_test) vs. predicted (y_pred) values.

5.Key Insights Derived

Loss Analysis:
Cumulative loss and death trends over the years are calculated and visualized.

Disaster Patterns:
Insights into how disasters vary by season and province.

6.Potential Applications:

This analysis can be used for:
Risk assessment and disaster management in Nepal.
Identifying trends and patterns for policymaking.
Enhancing resource allocation for disaster-affected regions.







