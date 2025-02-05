# Car Sales Data Analysis and Prediction

## Overview
This project analyzes a car sales dataset to identify key trends, handle missing data, and build predictive models for car sales using Linear Regression and Random Forest Regression.

## Dataset
The dataset, `Car_sales.csv`, contains various attributes related to car sales, vehicle specifications, and performance metrics.

### Observations
- Some columns are not of much importance.
- Several data points are missing.
- The `Sales_in_thousands` column has an extra count compared to the total manufacturers (indicating possible outliers).
- The `Price_in_thousands` column has two missing values.
- One vehicle's `hp`, `width`, `length`, `wheelbase`, and `engine size` are missing.
- `Fuel efficiency` is missing for three vehicles, and `power performance factor` is missing for two vehicles.
- The `Year_resale_value` column has many null values.

## Data Preprocessing
### Feature Allocation
- **Target Variable**: `Sales_in_thousands`
- **Features**: All other columns except `Manufacturer`, `Model`, `Latest_Launch`, and the target variable.

### Splitting Data
- Numerical features: Selected based on `float64` and `int64` data types.
- Categorical features: Selected based on `object` data type.

### Data Preprocessing Pipelines
1. **Numerical Data**
   - Missing values are imputed with the mean.
2. **Categorical Data**
   - Missing values are imputed with the most frequent value.
   - One-hot encoding is applied to categorical variables.

## Model Training
### Train-Test Split
- The dataset is split into training (80%) and testing (20%) sets.

### Models Used
1. **Linear Regression**
   - Implemented using a pipeline combining preprocessing and regression.
   - Trained and evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² score.

2. **Random Forest Regression**
   - Implemented using a pipeline with preprocessing and a Random Forest model.
   - Trained and evaluated using MAE, MSE, and R² score.

## Model Evaluation
### Linear Regression Results
- **MAE:** `X.XX`
- **MSE:** `X.XX`
- **R² Score:** `X.XX`

### Random Forest Regression Results
- **MAE:** `X.XX`
- **MSE:** `X.XX`
- **R² Score:** `X.XX`

## Analysis
- The **Mean Absolute Error (MAE)** for the Random Forest Regression model is lower, indicating better performance than Linear Regression.
- The **Mean Squared Error (MSE)** is lower for the Linear Regression model compared to Random Forest Regression.
- The **R² score**, which indicates how well the model fits the data, is closer to 1 in the Linear Regression model.

## Conclusion
- Random Forest Regression is more robust and performs better in reducing absolute errors.
- Linear Regression gives a better overall fit but may not generalize well for unseen data.

## Dependencies
Ensure you have the following libraries installed before running the code:
```bash
pip install numpy pandas scikit-learn
```

## Usage
1. Load the dataset.
2. Run the preprocessing steps.
3. Train the models.
4. Evaluate and compare the models.

## Author
This project was developed as part of an exploration into predictive modeling for car sales data.

