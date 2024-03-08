# Taxi Demand Prediction in New York City

## Source:

‫‪https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page‬‬‬‬


## About:

This project aims to forecast taxi demand in New York City by leveraging machine learning (ML) and non-ML methods. Through comprehensive data preparation, modeling, evaluation, and specific focus on JFK airport - one of the city's busiest locations for taxi trips, this project highlights the effectiveness of various predictive algorithms.

## Result Summary:

The comparison of different predictive methods indicates that the Random Forest model outperforms others by achieving the lowest residual errors. Detailed findings are organized into four Jupyter notebooks, each focusing on distinct phases of the project - Data Preparation, Modeling, Machine Learning Evaluation, and a targeted Evaluation for JFK Airport.

Result table for JFK airport (the busiest location):

![image](https://github.com/Shahla9/New-York-taxi-demand-prediction/assets/114596964/7d11c64b-f445-4701-bb07-2069e6b6195e)



Result table for the busiest locations:

![image](https://github.com/Shahla9/New-York-taxi-demand-prediction/assets/114596964/7fa8db71-cc54-4c1f-aa9a-79db4e325772)


## Steps:

### Data Preparation:

In the initial phase, the "Data Preparation" notebook outlines the steps taken to fetch, clean, and prepare taxi record data sourced from the New York City government's website. Key steps included:

#### Data Fetching and Cleaning:
Removing date outliers and cleaning the dataset to ensure accuracy.
#### Data Profiling:
Analyzing the dataset to understand its characteristics.
#### Daily Trip Counts and Filtering:
Counting daily trips for each location, followed by narrowing down to the 50 most popular areas.
#### Feature Extraction:
Creating lag features ranging from 1 to 10 days to capture temporal dependencies in daily trips.
#### Null Handling:
Addressing missing values to maintain dataset integrity.

### Model:

The "Model" notebook focuses on machine learning models. Here, the dataset—comprising the busiest locations' daily trip sums and extracted features for the first four months of 2023—is prepared for modeling. The features included are:

FEATURES = [
    '1_day_lag', '2_day_lag', '3_day_lag', 
    '4_day_lag', '5_day_lag', '6_day_lag',	
    '7_day_lag', '8_day_lag', '9_day_lag', '10_day_lag'
]

The label for prediction is set as:

LABEL = ['Daily_trips']

For the model's train-test split, data from the first three months are used for training, while the fourth month's data is reserved for testing.

#### Machine Learning:

This phase employs Decision Tree and Random Forest algorithms to predict taxi demands. The selection of these models is based on their ability to handle non-linear data and provide insights into the importance of different features affecting taxi demand.


### Evaluation:

The "Evaluation" notebook delves into the performance assessment of the predictive models using Root Mean Square Error (RMSE) and Mean Absolute Percentage Error (MAPE) metrics. A table summarizing the residuals of various methods is presented, demonstrating the superior accuracy of the Random Forest model.


### Evaluation for JFK Airport:

In the final notebook, "EVALUATION_AIRPORT," a focused analysis on JFK Airport reveals lower residual errors compared to the broader study encompassing the 50 popular areas. This targeted evaluation underscores the model's effectiveness in predicting taxi demand at a highly trafficked location.

#### The project utilizes a range of libraries to facilitate data manipulation, analysis, and modeling:

##### Geopandas: For geographic data processing.
##### Numpy: For numerical computations.
##### Pandas: For data manipulation and analysis.
##### Math: For mathematical functions.
##### Tabulate: For formatting tables in the output.

This project serves as a comprehensive guide to predicting taxi demand in New York City, showcasing the application of machine learning techniques to real-world transportation data.
