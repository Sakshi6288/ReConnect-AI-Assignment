# ReConnect-AI-Assignment
The task is to analyze the provided dataset containing historical load, temperature, and rain factor data, and deliver detailed findings, methodology, and a final load demand forecast. 

# Data Description :
Hourly historical load, weather and holiday data an of the utility are provided (Load_History.csv). The historical data file contains the data from the 01-01-2022 00:00 till 24-12-2023 23:00. Beyond this point it contains only weather and holdiay data.

POWER_MW – Hourly Load
Temp_FC – Forecasted Temperature – available for future in advance
Rain_FC – Forecasted Precipitation – available for future in advance
Is_holiday – Holiday Tagging [ 1 – Holiday, 0 – No Holiday]

This notebook performs exploratory data analysis and preprocessing on a power load forecasting dataset and machine learning models such as K Means, PLS and RandomForest have been utilized for the forecasting of final load demand. 
Key steps include:
## Data Exploration
* Loads historical power consumption data (Load_History.csv).
* Visualizes relationships between variables using scatter plots (e.g., temperature, rainfall, holiday vs. power load).
* Detects outliers using box plots and pairwise visualizations (seaborn.pairplot).

## Missing Data Handling
* Inspects and reports missing values (count and percentage).
* Filters data up to a specific date (2023-12-24 23:00:00).
* Demonstrates two strategies for missing data:
  * Dropping rows with missing values.
  * Filling missing values using column-wise mean.

## Data Visualization
* Generates comparative plots to understand data distributions and outlier patterns before and after handling missing values.

## Model Training
1. K-Means Clustering (Unsupervised Learning)
Used to group the data based on features: POWER_MW, Temp_FC, and Rain_FC.
Helps identify hidden patterns or clusters in power load behavior.

2. Random Forest Regressor (Supervised Learning)
Employed to predict power load (POWER_MW) based on input features.
Applied on both:
Full dataset.
Season-specific data (e.g., winter/Summer etc).

3. PLS Regression
PLS Regression is a supervised machine learning technique used when predictors (features) are highly collinear or when the number of predictors exceeds the number of observations.

## Performance Evaluation
RMSE (Root Mean Squared Error)
R² Score (Coefficient of Determination)
Actual vs Predicted plots were generated for visual evaluation.

