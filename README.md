# House Price Prediction (Regression)

Predicting residential sale prices from property characteristics using machine learning, and comparing regression models to find the most accurate one.

## Problem Statement
Buyers, sellers and investors need a reliable estimate of what a house is worth. This project builds regression models that predict `SalePrice` from features such as lot area, building type, zoning, year built and basement size.

## Dataset
- **Source:** House Price Prediction dataset (from the GeeksforGeeks tutorial on house price prediction)
- **Size:** 2,919 rows, 13 columns
- **Target:** `SalePrice`
- **Features include:** `MSSubClass`, `MSZoning`, `LotArea`, `LotConfig`, `BldgType`, `OverallCond`, `YearBuilt`, `YearRemodAdd`, `Exterior1st`, `BsmtFinSF2`, `TotalBsmtSF`

## Project Workflow
1. **Data loading and inspection:** checked shape, data types and missing values
2. **Data cleaning:** dropped the `Id` column and handled missing values
3. **Exploratory data analysis:** correlation heatmap of numeric features and distributions of categorical features
4. **Encoding:** converted categorical columns to numeric using One-Hot Encoding
5. **Train/test split:** 80% training, 20% testing
6. **Model training:** Linear Regression, Random Forest Regressor, Support Vector Regressor (SVR)
7. **Evaluation:** compared models using Mean Absolute Percentage Error (MAPE)

## Results

| Model | MAPE | Average error |
|-------|------|---------------|
| Support Vector Regressor | 0.1871 | 18.7% |
| Random Forest Regressor | 0.1860 | 18.6% |
| Linear Regression | 0.1874 | 18.7% |

**Best model:** Random Forest Regressor with a MAPE of 0.186, meaning predictions were off by about 18.6% on average.

## Key Insights
- All three models landed within about 0.1 percentage points of each other, so model choice made little difference. The limited set of 12 features is likely what caps accuracy.
- Random Forest scored slightly best, but the gap is too small to call it clearly better than SVR or Linear Regression.
- <add one insight from your correlation heatmap, such as which numeric feature correlates most with SalePrice>

## Key Insights
- ___ (which features are most strongly correlated with price, from your heatmap)
- ___ (which model performed best and a possible reason)
- ___ (anything notable in the categorical features, such as the most common building type or zoning class)

## Visualizations
(https://github.com/angyisinluv/regression-project/blob/main/correlation_heatmap.png?raw=true)

## Technologies Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Jupyter Notebook

## How to Run
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
jupyter notebook
```
Open `regression_project.ipynb` and run all cells. The dataset file `HousePricePrediction.xlsx` must be in the path used by the notebook.

## Future Improvements
- Try ensemble models such as XGBoost or Gradient Boosting
- Tune hyperparameters with GridSearchCV
- Add more features (neighborhood, number of rooms, living area)
- Build a Streamlit app for live price predictions

## Author
**Angyllyn Gurung**
[GitHub](https://github.com/angyisinluv) | [LinkedIn](https://www.linkedin.com/in/angyllyn-gurung)
