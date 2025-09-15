# Real-Estate-Price-Prediction
This project predicts the price of properties (apartments, flats, houses) based on their features such as size, location, furnishing status, and number of bedrooms (BHK). It uses regression models to estimate property prices and visualize key factors affecting pricing.

# Dataset

The dataset contains property listings with the following important columns:
| Column           | Description                                                 |
| ---------------- | ----------------------------------------------------------- |
| **price**        | Price of the property (target variable).                    |
| **size**         | Size of the property in square feet.                        |
| **propertyType** | Type of property, often contains number of BHK.             |
| **location**     | City/Locality of the property.                              |
| **furnishing**   | Furnishing status (Furnished, Semi-Furnished, Unfurnished). |

Dataset:- https://www.kaggle.com/datasets/muhammedthouyibtk/house-price-india-dataset?select=Makaan_Properties_Buy_Dataset.csv

Additional engineered features:

BHK: Extracted from propertyType column.

Price_per_sqft: price / size.


Steps Performed

* Data Preprocessing

Load dataset using pandas.

Handle missing values (drop or impute).

Extract BHK from propertyType.

Calculate Price_per_sqft.

Encode categorical variables with OneHotEncoder.

Scale numerical features with StandardScaler.

* Exploratory Data Analysis (EDA)

Plot distribution of prices.

Correlation heatmap for numeric features.

Price by location.

Furnishing status vs price.

* Model Training

Applied multiple regression models:

Linear Regression (baseline)

Random Forest Regressor

XGBoost Regressor

LightGBM Regressor

* Evaluation Metrics
Used:

RMSE (Root Mean Squared Error)

MAE (Mean Absolute Error)

R² Score (Coefficient of Determination)

* Visualization
Actual vs Predicted Price (scatter plot).

Feature Importance (tree-based models).

# Results
| Model                   | RMSE     | MAE      | R²   |
| ----------------------- | -------- | -------- | ---- |
| Linear Regression       | 48944.50 | 23527.27 | 0.40 |
| Random Forest Regressor | 37142.90 | 11401.77 | 0.65 |
| XGBoost Regressor       | 34700.60 | 12367.72 | 0.70 |
| LightGBM Regressor      | 38323.62 | 13367.63 | 0.63 |


# Future Improvements

Add more engineered features (amenities, nearby facilities).

Use hyperparameter tuning (GridSearchCV / Optuna).

Deploy as a web app with Streamlit or Flask.
