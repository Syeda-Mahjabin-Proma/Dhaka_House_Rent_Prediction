# Dhaka House Rent Prediction Model

## Overview

This project predicts **house rents in Dhaka** based on features like location, area, number of bedrooms, and bathrooms.
It implements **Random Forest Regressor**, **XGBoost Regressor**, and **Linear Regression** to estimate rental prices. Among these models, **Random Forest** provided the best performance.

---

## Dataset Description

The dataset `houserentdhaka.csv` contains **28,800 rows** and the following columns:

| Column         | Type    | Description                          |
| -------------- | ------- | ------------------------------------ |
| **Unnamed: 0** | int64   | Index (removed during processing)    |
| **Location**   | object  | Area/Neighborhood                    |
| **Area**       | int64   | Area in square feet                  |
| **Bed**        | int64   | Number of bedrooms                   |
| **Bath**       | int64   | Number of bathrooms                  |
| **Price**      | float64 | Rent in Bangladeshi Taka (in Thousand) |

### Data Cleaning Steps

* Removed unnecessary columns (`Unnamed: 0`)
* Cleaned `Area` by removing 'sqft' and commas → converted to `int`
* Cleaned `Price` by handling "Thousand" and "Lakh" → converted to `float`
* Encoded categorical feature `Location` using **Target Encoding**

---

## Steps & Methods

1. **Data Preprocessing**

   * Missing value inspection
   * Categorical encoding
   * Conversion of strings to numeric for `Area` and `Price`

2. **Exploratory Data Analysis (EDA)**

   * Summary statistics
   * Feature inspection
   * Outlier detection

3. **Model Building**

   * **Random Forest Regressor**
   * **XGBoost Regressor**
   * **Linear Regression**
   * Evaluation metrics: **RMSE**, **MAE**, **R² Score**

4. **Model Evaluation**

| Model             | RMSE | R² Score |
| ----------------- | ------- | -------- |
| Random Forest     | 8796.60 | 0.79 |
| XGBoost           | 9433.56 | 0.76 |
| Linear Regression | 13153.48 |0.54|

> **Random Forest** provided the most accurate predictions among all models.

5. **User Input Prediction**

   * Users can input **Location, Area, Bedrooms, Bathrooms**
   * Model predicts the **estimated house rent**

---

## Technologies Used

* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Plotly Express
* Scikit-learn
* Category Encoders
* XGBoost

---

## How to Run

1. Clone the repository:

```bash
git clone https://github.com/Syeda-Mahjabin-Proma/Dhaka_House_Rent_Prediction.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
pip install category_encoders
```

3. Run the Python script:

```bash
python main.py
```

4. Follow the prompts to input **Location, Area, Bed, Bath** for rent prediction.

---

## Future Improvements

* Add more features like **floor number, furnishing status, or proximity to amenities**
* Hyperparameter tuning for **Random Forest** and **XGBoost**
* Develop a **web application** for real-time predictions
* Expand dataset to include more locations in Dhaka

---
## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
