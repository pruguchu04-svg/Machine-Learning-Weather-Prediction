# Weather Temperature Prediction using Linear Regression

A simple linear regression project that predicts the **Maximum Temperature (MaxTemp)** of a day using the **Minimum Temperature (MinTemp)** as a predictor.

## 📌 Overview

Regression analysis is a predictive modelling technique used to investigate the relationship between a dependent variable and one or more independent variables. Linear regression is commonly applied in fields such as:

- Market research and customer survey analysis
- Studying automobile engine performance
- Pricing strategy for goods
- Astronomy and other scientific measurements

This project applies **simple linear regression** to weather data, exploring whether the minimum temperature of a day can predict its maximum temperature.

##  Dataset

The dataset (`weather_dataset.csv`) contains **366 daily weather records** with **22 features**.

For this analysis, only two columns are used:
- **Independent variable (X):** `MinTemp`
- **Dependent variable (y):** `MaxTemp`

##  Tools & Libraries

- `pandas` – data loading and manipulation
- `numpy` – numerical operations
- `matplotlib` & `seaborn` – data visualization
- `scikit-learn` – train/test splitting, model building, and evaluation metrics

##  Workflow

1. **Exploratory Data Analysis (EDA)**
   - Inspected dataset shape, summary statistics, and sample rows
   - Visualized the relationship between `MinTemp` and `MaxTemp` with a scatter plot
   - Plotted the distribution of `MaxTemp` to check its spread and skewness

2. **Data Preparation**
   - Reshaped `MinTemp` and `MaxTemp` into 2D arrays (`reshape(-1, 1)`) as required by scikit-learn
   - Split the data into training (80%) and testing (20%) sets using `train_test_split`

3. **Model Training**
   - Trained a `LinearRegression` model on the training data
   - Retrieved the learned **intercept** and **coefficient**

4. **Prediction**
   - Generated predictions on the test set
   - Compared actual vs. predicted values in a table and bar chart
   - Plotted the regression line against the test data

5. **Evaluation**
   - Assessed performance using Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE)

## 📊 Results

| Metric | Value |
| Intercept | 14.56 |
| Coefficient | 0.82 |
| Mean Absolute Error (MAE) | 3.51 |
| Mean Squared Error (MSE) | 17.01 |
| Root Mean Squared Error (RMSE) | 4.12 |


##  Conclusion

The model reveals a **positive relationship** between minimum and maximum temperature — warmer nights tend to be followed by warmer days. With an average prediction error of around **4°C (RMSE)**, the model captures the general trend reasonably well but is only **moderately accurate**, since `MaxTemp` is influenced by many other factors (humidity, wind, cloud cover, pressure, season, etc.) not included in this single-feature model.


