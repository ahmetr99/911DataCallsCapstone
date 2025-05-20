# Emergency Risk Prediction Using 911 Call Data

This project analyzes emergency 911 call records to identify and predict high-risk areas based on spatial and temporal features. It combines exploratory data analysis with supervised machine learning to support emergency planning and resource allocation decisions.

## Dataset

The dataset consists of real 911 call records and includes the following fields:

- `lat`, `lng`: Geographic coordinates of the call
- `timeStamp`: Timestamp of the incident
- `title`: Emergency type (e.g., EMS, Fire, Traffic)
- `desc`: Description of the call
- `zip`, `twp`: Zip code and township

## Objectives

- Identify temporal and geographic patterns in emergency call data
- Visualize call volumes by hour, day, and month
- Map call locations and hotspot regions
- Define and label high-risk areas based on historical call frequency
- Train a machine learning model to classify a location and time as high or low risk

## Methodology

1. Data preprocessing and feature engineering:
   - Extract hour, day of week, and month from timestamps
   - Group by latitude and longitude to count call volume
   - Define "high-risk" areas as locations with call counts above the 75th percentile

2. Exploratory Data Analysis:
   - Time-series plots and count visualizations
   - Distribution analysis by category and location
   - Heatmap and marker cluster maps using geographic coordinates

3. Model building:
   - Random Forest classifier with balanced class weights
   - Input features: latitude, longitude, hour, day of week, month
   - Target variable: Risk level (binary)

## Results

- Model accuracy: approximately 84%
- Recall for high-risk areas: approximately 97%
- Feature importance indicates time and location are strong predictors
- Confusion matrix and metric visualizations confirm model reliability

## Future Work

- Integrate additional features such as population density or weather data
- Apply time series forecasting techniques for future incident prediction
- Experiment with other classification algorithms (e.g., XGBoost, logistic regression)
- Build a dashboard for real-time visualization and prediction

## How to Run

1. Load the dataset (`911.csv`)
2. Open the Jupyter notebook or Google Colab
3. Execute cells in sequence to reproduce the analysis and model training

## Author

Ahmet Rahmanoglu 
Data Science & Analytics  
https://www.linkedin.com/in/ahmet-rahmanoglu-675248207/
