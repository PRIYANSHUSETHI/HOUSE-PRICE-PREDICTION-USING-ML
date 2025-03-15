# House Price Predictions Using Machine Learning

This repository contains a machine learning project focused on predicting house prices using regression techniques. The project includes data preprocessing, feature engineering, model training, evaluation, and deployment using Python and various ML libraries.

## Project Overview

This is a **supervised batch learning problem** with **regression** as the main task. The model is evaluated using **Root Mean Squared Error (RMSE)** as it penalizes large errors more, making it a suitable metric for this problem.

## Features & Dataset

The dataset consists of various housing attributes, including:
- `CHAS` - Charles River dummy variable (1 if tract bounds river; 0 otherwise)
- `RM` - Average number of rooms per dwelling
- `ZN` - Proportion of residential land zoned for large lots
- `LSTAT` - Percentage of lower status of the population
- `TAX` - Property tax rate per $10,000
- `MEDV` - Median value of owner-occupied homes (target variable)

## Project Structure

- **Data Preprocessing**
  - Handling missing values (removal, imputation)
  - Feature engineering (creating new attributes)
  - Exploratory Data Analysis (EDA) with visualizations

- **Data Splitting**
  - Random train-test split (80-20)
  - Stratified sampling based on important features (`CHAS`)

- **Model Training & Evaluation**
  - Models used:
    - Linear Regression
    - Decision Tree Regressor
    - Random Forest Regressor (Final Model)
  - Performance metrics:
    - RMSE
    - Cross-validation for robust evaluation

- **Model Deployment**
  - Final trained model saved using `joblib`
  - Predictions tested on the test dataset

## Dependencies

Ensure you have the following Python libraries installed before running the project:

```sh
pip install pandas numpy scikit-learn matplotlib joblib
```

## Running the Project

1. Clone this repository:

   ```sh
   git clone https://github.com/your-username/house-price-prediction.git
   cd house-price-prediction
   ```

2. Place your dataset (`data.csv`) in the project directory.

3. Run the script:

   ```sh
   python house_price_predictions_using_ml.py
   ```

4. The trained model will be saved as `Sethi.joblib`.

## Results & Insights

- Random Forest Regressor performed the best among the models tested.
- Cross-validation was used to validate model performance.
- Feature engineering (creating `TAXRM = TAX/RM`) improved model accuracy.

## Future Improvements(for my future self and for anyone who continues to grow and learn:))

- Hyperparameter tuning for better performance
- Integration of more features
- Deployment as a web service using Flask or FastAPI
