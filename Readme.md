# California Housing Prices Prediction

![California Housing](https://storage.googleapis.com/kaggle-datasets-images/45561/87595/6bd22bc2633e9b8bb7b80b2f09d28ed5/data-original.jpg)

## About the Dataset
This project is based on the "California Housing Prices" dataset sourced from Kaggle, available [here](https://www.kaggle.com/datasets/camnugent/california-housing-prices). The dataset contains information from the 1990 California census, providing details about houses in different California districts, along with some summary statistics based on the census data.

The dataset consists of the following columns:

- longitude: Longitude of the district
- latitude: Latitude of the district
- housing_median_age: Median age of houses in the district
- total_rooms: Total number of rooms in the district
- total_bedrooms: Total number of bedrooms in the district
- population: Total population in the district
- households: Total number of households in the district
- median_income: Median income of households in the district
- median_house_value: Median value of houses in the district (target variable)
- ocean_proximity: Proximity of the district to the ocean (categorical)

## Data Description
The dataset contains a total of 20,640 entries. The `total_bedrooms` column has some missing values (20433 non-null entries). The `ocean_proximity` column has five unique categories: "INLAND," "ISLAND," "NEAR BAY," "NEAR OCEAN," and "<1H OCEAN." The data types include 9 float64 columns and 1 object (categorical) column.

Here are some summary statistics of the numerical columns:

```python
housing.describe()
```

- **longitude:** Mean: -119.576, Standard Deviation: 2.002, Min: -124.350, Max: -114.310
- **latitude:** Mean: 35.640, Standard Deviation: 2.138, Min: 32.540, Max: 41.950
- **housing_median_age:** Mean: 28.652, Standard Deviation: 12.576, Min: 1.000, Max: 52.000
- **total_rooms:** Mean: 2622.348, Standard Deviation: 2138.559, Min: 6.000, Max: 39320.000
- **total_bedrooms:** Mean: 534.885, Standard Deviation: 412.716, Min: 2.000, Max: 6210.000
- **population:** Mean: 1419.525, Standard Deviation: 1115.715, Min: 3.000, Max: 35682.000
- **households:** Mean: 496.975, Standard Deviation: 375.738, Min: 2.000, Max: 5358.000
- **median_income:** Mean: 3.876, Standard Deviation: 1.905, Min: 0.4999, Max: 15.0001

## Data Preprocessing
Before using the data for machine learning, some preprocessing steps are required, such as handling missing values in the `total_bedrooms` column and encoding the categorical variable `ocean_proximity` into numerical format (e.g., using one-hot encoding).

## Model Building
In this project, we used the `RandomForestRegressor` from scikit-learn to build a machine learning model for predicting the "median_house_value" based on the other features. The trained model achieved an R-squared value of approximately 0.8082 on the test data, indicating a reasonable fit to the data.

## How to Use the Project
To use this project, you can follow these steps:

1. Download the "housing.csv" file from the Kaggle dataset link provided above.
2. Run the Jupyter Notebook or Python script that contains the project code.
3. Ensure that the required libraries (e.g., pandas, numpy, scikit-learn) are installed in your Python environment.
4. The project will preprocess the data, build a random forest regression model, and provide the R-squared value for evaluation.
5. Feel free to modify the code or experiment with different models and hyperparameters to further improve the performance.

Happy exploring and building your machine learning project! If you have any questions or need assistance, please feel free to reach out. Enjoy your learning journey!