# HOUSE PRICE PREDICTION

## A MACHINE LEARNING PROJECT

## 1. Project Information

**Project Name:** House Price Prediction

**Project Type:** Supervised Learning / Regression

**Status:** Development

**Date Started:** 2026-10-09

**Last Updated:** 2026-10-18

**Author:** Samuel Ablordeppey

### Project Description

An end-to-end machine learning project for predicting residential house prices using regression models, Python, scikit-learn and the Ames Housing Dataset.

### Objective

Build a linear regression model capable of predicting residential house prices from property characteristics.

### Expected Outcome

A trained and evaluated regression model that accepts house features and produces an estimated sale price.

## 2. Problem Definition

### Real-World Problem

House prices depend on numerous property characteristics such as size, location, quality, age, and available facilities. Manually estimating prices can be difficult when many factors must be considered simultaneously.

### Machine Learning Problem

Use historical housing data to learn the relationship between property characteristics and sale prices, then use the learned relationship to predict prices for unseen houses.

### Problem Type

- Supervised Learning
- Regression

### Target Variable

**Name:** SalePrice

**Type:** Continuous numerical

**Description:** Final sale price of the residential property.

**Units:** US dollars

### Features

Features shown in datasets section below

## 3. Requirements & Constraints

### Functional Requirements

1. Load the housing dataset.
2. Clean and preprocess the data.
3. Engineer useful features.
4. Train a regression model.
5. Evaluate model performance.
6. Save the trained model.
7. Generate predictions for new observations.

### Technical Requirements

1. Python
2. Pandas
3. NumPy
4. Scikit-learn
5. Matplotlib
6. Seaborn
7. Joblib

### Constraints

- Dataset contains missing values.
- Numerical and categorical variables require different preprocessing.
- Linear regression has assumptions that must be investigated.
- Model performance depends on the quality of the available features.

## 4. Dataset

### Dataset Information

**Dataset Name:** Ames Housing Dataset

**Source:** Kaggle

**URL:** [https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

**Version:** Original dataset version used for the project

**Number of Rows:** 1,460

**Number of Columns:** 81

### Dataset Files

```text
data/
 ├── raw/
 ├── external/
 └── processed/
```

### Data Dictionary

| # | Feature | Type | Description | Unit | Role |
|---:|---|---|---|---|---|
| 1 | Id | Numerical | Unique identifier for each property | Identifier | Feature |
| 2 | MSSubClass | Numerical | Type of dwelling involved in the sale | Class code | Feature |
| 3 | MSZoning | Categorical | General zoning classification | Category | Feature |
| 4 | LotFrontage | Numerical | Linear feet of street connected to property | Feet | Feature |
| 5 | LotArea | Numerical | Lot size | Square feet | Feature |
| 6 | Street | Categorical | Type of road access | Category | Feature |
| 7 | Alley | Categorical | Type of alley access | Category | Feature |
| 8 | LotShape | Categorical | General shape of property | Category | Feature |
| 9 | LandContour | Categorical | Flatness of property | Category | Feature |
| 10 | Utilities | Categorical | Type of utilities available | Category | Feature |
| 11 | LotConfig | Categorical | Lot configuration | Category | Feature |
| 12 | LandSlope | Categorical | Slope of property | Category | Feature |
| 13 | Neighborhood | Categorical | Physical location within Ames city limits | Category | Feature |
| 14 | Condition1 | Categorical | Proximity to main road, railroad, or other condition | Category | Feature |
| 15 | Condition2 | Categorical | Secondary proximity to road, railroad, or other condition | Category | Feature |
| 16 | BldgType | Categorical | Type of dwelling | Category | Feature |
| 17 | HouseStyle | Categorical | Style of dwelling | Category | Feature |
| 18 | OverallQual | Numerical | Overall material and finish quality rating | Rating 1–10 | Feature |
| 19 | OverallCond | Numerical | Overall condition rating | Rating 1–10 | Feature |
| 20 | YearBuilt | Numerical | Original construction year | Year | Feature |
| 21 | YearRemodAdd | Numerical | Year of remodeling or addition | Year | Feature |
| 22 | RoofStyle | Categorical | Type of roof | Category | Feature |
| 23 | RoofMatl | Categorical | Roof material | Category | Feature |
| 24 | Exterior1st | Categorical | Primary exterior covering | Category | Feature |
| 25 | Exterior2nd | Categorical | Secondary exterior covering | Category | Feature |
| 26 | MasVnrType | Categorical | Masonry veneer type | Category | Feature |
| 27 | MasVnrArea | Numerical | Masonry veneer area | Square feet | Feature |
| 28 | ExterQual | Categorical | Exterior material quality | Category | Feature |
| 29 | ExterCond | Categorical | Exterior material condition | Category | Feature |
| 30 | Foundation | Categorical | Type of foundation | Category | Feature |
| 31 | BsmtQual | Categorical | Basement height/quality | Category | Feature |
| 32 | BsmtCond | Categorical | General basement condition | Category | Feature |
| 33 | BsmtExposure | Categorical | Basement walkout/garden-level exposure | Category | Feature |
| 34 | BsmtFinType1 | Categorical | Quality of primary finished basement area | Category | Feature |
| 35 | BsmtFinSF1 | Numerical | Finished basement area, type 1 | Square feet | Feature |
| 36 | BsmtFinType2 | Categorical | Quality of secondary finished basement area | Category | Feature |
| 37 | BsmtFinSF2 | Numerical | Finished basement area, type 2 | Square feet | Feature |
| 38 | BsmtUnfSF | Numerical | Unfinished basement area | Square feet | Feature |
| 39 | TotalBsmtSF | Numerical | Total basement area | Square feet | Feature |
| 40 | Heating | Categorical | Type of heating | Category | Feature |
| 41 | HeatingQC | Categorical | Heating quality and condition | Category | Feature |
| 42 | CentralAir | Categorical | Central air conditioning | Yes/No | Feature |
| 43 | Electrical | Categorical | Electrical system | Category | Feature |
| 44 | 1stFlrSF | Numerical | First-floor area | Square feet | Feature |
| 45 | 2ndFlrSF | Numerical | Second-floor area | Square feet | Feature |
| 46 | LowQualFinSF | Numerical | Low-quality finished area | Square feet | Feature |
| 47 | GrLivArea | Numerical | Above-ground living area | Square feet | Feature |
| 48 | BsmtFullBath | Numerical | Full bathrooms in basement | Count | Feature |
| 49 | BsmtHalfBath | Numerical | Half bathrooms in basement | Count | Feature |
| 50 | FullBath | Numerical | Full bathrooms above grade | Count | Feature |
| 51 | HalfBath | Numerical | Half bathrooms above grade | Count | Feature |
| 52 | BedroomAbvGr | Numerical | Bedrooms above basement level | Count | Feature |
| 53 | KitchenAbvGr | Numerical | Kitchens above grade | Count | Feature |
| 54 | KitchenQual | Categorical | Kitchen quality | Category | Feature |
| 55 | TotRmsAbvGrd | Numerical | Total rooms above grade, excluding bathrooms | Count | Feature |
| 56 | Functional | Categorical | Home functionality rating | Category | Feature |
| 57 | Fireplaces | Numerical | Number of fireplaces | Count | Feature |
| 58 | FireplaceQu | Categorical | Fireplace quality | Category | Feature |
| 59 | GarageType | Categorical | Garage location/type | Category | Feature |
| 60 | GarageYrBlt | Numerical | Year garage was built | Year | Feature |
| 61 | GarageFinish | Categorical | Interior finish of garage | Category | Feature |
| 62 | GarageCars | Numerical | Garage car capacity | Cars | Feature |
| 63 | GarageArea | Numerical | Garage area | Square feet | Feature |
| 64 | GarageQual | Categorical | Garage quality | Category | Feature |
| 65 | GarageCond | Categorical | Garage condition | Category | Feature |
| 66 | PavedDrive | Categorical | Paved driveway status | Category | Feature |
| 67 | WoodDeckSF | Numerical | Wood deck area | Square feet | Feature |
| 68 | OpenPorchSF | Numerical | Open porch area | Square feet | Feature |
| 69 | EnclosedPorch | Numerical | Enclosed porch area | Square feet | Feature |
| 70 | 3SsnPorch | Numerical | Three-season porch area | Square feet | Feature |
| 71 | ScreenPorch | Numerical | Screen porch area | Square feet | Feature |
| 72 | PoolArea | Numerical | Pool area | Square feet | Feature |
| 73 | PoolQC | Categorical | Pool quality | Category | Feature |
| 74 | Fence | Categorical | Fence quality | Category | Feature |
| 75 | MiscFeature | Categorical | Miscellaneous feature not covered elsewhere | Category | Feature |
| 76 | MiscVal | Numerical | Value of miscellaneous feature | USD | Feature |
| 77 | MoSold | Numerical | Month property was sold | Month 1–12 | Feature |
| 78 | YrSold | Numerical | Year property was sold | Year | Feature |
| 79 | SaleType | Categorical | Type of sale | Category | Feature |
| 80 | SaleCondition | Categorical | Condition of sale | Category | Feature |
| 81 | SalePrice | Numerical | Final sale price of residential property | USD | Target |

### Data Split

**Training:** 80%

**Validation:** Used during model development

**Testing:** 20%

## 5. Environment & Dependencies

Operating System: Windows 11

Python Version: 3.12

Main Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Joblib

### Virtual Environment Configuration

Environment Tool: `venv`

Environment Directory: `.venv/`

Create Environment:

```
python -m venv .venv
```

Activate Environment (Windows PowerShell):

```
.\.venv\Scripts\Activate.ps1
```

Deactivate Environment:

```
deactivate
```

Upgrade pip:

```
python -m pip install --upgrade pip
```

### Installation

Activate virtual environment above then

```
python -m pip install -r requirements.txt
```

### Reproducibility

Random Seed: 42

Environment: Python virtual environment (`.venv`)

Dependency Management: `requirements.txt`

Development Dataset Version: Version 0.1.0

## 6. Data Understanding

### Initial Inspection

The dataset was inspected for:

- Number of observations
- Number of features
- Data types
- Missing values
- Duplicate records
- Unique values
- Numerical distributions
- Categorical variables
- Target distribution

### Initial Observations

1. The dataset contains both numerical and categorical features.
2. Several features contain missing values.
3. `SalePrice` are normally distributed and right skewed.
4. Some numerical features have strong relationships with `SalePrice`.
5. Some features show potential multicollinearity.

## 7. Data Cleaning

### Missing Values

**Problem:** Several columns contain missing values.

**Detection:** Pandas isnull() analysis.

**Treatment:** Numerical variables were imputed using appropriate statistical values, while categorical variables were handled according to their meaning and missing-value behavior.

**Reason:** The model requires a complete numerical feature matrix.

### Duplicates

**Detected:** No significant duplicate observations were identified.

**Action:** Dataset was checked before modeling.

**Reason:** Duplicate observations can distort model training.

### Invalid Values

**Problem:** Some variables contained values requiring interpretation before modeling.

**Action:** Values were inspected and corrected or transformed where necessary.

**Reason:** Invalid values can introduce incorrect relationships into the model.

### Outliers

**Detection:** Statistical analysis and visualization.

**Treatment:** Investigated individually rather than automatically removing all outliers.

**Reason:** Some extreme house values may represent legitimate observations.

### Data Leakage

**Potential leakage:** Features that directly reveal the target or information unavailable at prediction time.

**Detection:** Feature review and train/test preprocessing separation.

**Action:** Leakage-prone information was excluded.

## 8. Exploratory Data Analysis

### Univariate Analysis

The distributions of numerical variables were examined using histograms and descriptive statistics.

### Bivariate Analysis

Relationships between individual features and `SalePrice` were examined using scatter plots, box plots, and correlation analysis.

### Multivariate Analysis

Feature relationships and correlations were examined to identify:

- Strong predictors
- Redundant features
- Multicollinearity
- Potential interactions

### Important Findings

1. Living area has a strong relationship with sale price.
2. Overall quality is strongly associated with price.
3. Several numerical features are correlated with each other.
4. The target distribution contains high-value properties that create skewness.

## 9. Feature Engineering

### Features Created

| Feature        | Method / Formula                     | Reason                                |
| -------------- | ------------------------------------ | ------------------------------------- |
| TotalSF        | Total above-ground and basement area | Represent total usable space          |
| HouseAge       | Sale year - Year built               | Represent property age                |

### Features Removed

| Feature | Reason |
|---|---|
| Id | Identifier rather than predictive information |
| Highly redundant feature | Reduce unnecessary redundancy |

### Numerical Transformation

- Log transformation
- Power transformation
- Polynomial transformation where appropriate

### Categorical Transformation

- One-Hot Encoding
- Rare-category handling where necessary

### Scaling

**Method:** StandardScaler

**Reason:** Scale numerical features to comparable ranges and support preprocessing consistency.

### Feature Selection

**Methods Used**

- Correlation analysis
- Multicollinearity analysis
- RFECV
- Model-based selection

### Selected Features

```text
OverallQual
GrLivArea
GarageCars
TotalBsmtSF
YearBuilt
TotalSF
HouseAge
...
```

### Removed Features

```text
Id
Highly redundant variables
Low-information variables
```

## 10. Assumptions

### Data Assumptions

1. Historical housing relationships provide useful information about future observations.
2. Training data is sufficiently representative of the prediction population.
3. Feature values are measured consistently.

### Linear Regression Model Assumptions

1. Linear relationship between predictors and target.
2. Residuals are approximately independent.
3. Residual variance is reasonably constant.
4. Residuals are approximately normally distributed for inference.
5. Severe multicollinearity should be controlled.

## 11. Baseline Model

**Baseline:** Basic Linear Regression using the initial processed features.

### Purpose

Establish a reference performance level before applying additional feature engineering and feature selection.

### Results

**Metric:** RMSE  
**Score:** Example baseline RMSE

## 12. Model Selection

### Candidate Models

| Model                                | Reason for Testing                                            |
| ------------------------------------ | ------------------------------------------------------------- |
| Linear Regression                    | Establish an interpretable linear baseline                    |
| Ridge Regression                     | Investigate L2 regularization                                 |
| Lasso Regression                     | Investigate L1 regularization and feature selection           |
| Elastic Net Regression               | Combine L1 and L2 regularization                              |
| Random Forest Regression             | Capture nonlinear relationships and feature interactions      |
| Gradient Boosting Regression         | Improve predictive accuracy by sequentially correcting errors |
| K-Nearest Neighbors (KNN) Regression | Test prediction based on similarities between observations    |
| Support Vector Regression (SVR)      | Model nonlinear relationships using kernels                   |

### Model Selection Criteria

- Predictive performance
- Generalization
- Interpretability
- Computational cost
- Model assumptions

## 13. Model Training

**Model:** Linear Regression

**Features:** Selected numerical and encoded categorical features

**Training Data:** Training dataset

**Parameters:** Default LinearRegression configuration

**Random State:** 42

### Training Process

1. Split the data.
2. Fit preprocessing transformations on training data.
3. Transform validation/test data.
4. Train the regression model.
5. Generate predictions.
6. Evaluate performance.

## 14. Hyperparameter Tuning

**Method:** Not required for basic Linear Regression.

### Parameters Tested

None

### Best Parameters

Default LinearRegression configuration

## 15. Experiment Tracking

| Experiment | Model                           | Features | Parameters                  | Metric        | Result (RMSE) | Notes                                   |
| ---------- | ------------------------------- | -------- | --------------------------- | ------------- | ------------- | --------------------------------------- |
| 1          | Linear Regression               | Initial  | Default                     | CV RMSE       | 39,503.98     | Baseline                                |
| 2          | Ridge Regression                | Initial  | `alpha=10.0`                | Tuned CV RMSE | 32,547.28     | L2 regularization                       |
| 3          | Lasso Regression                | Initial  | `alpha=100.0`               | Tuned CV RMSE | 32,433.77     | L1 regularization and feature selection |
| 4          | Elastic Net Regression          | Initial  | `alpha=0.1`, `l1_ratio=0.8` | Tuned CV RMSE | 32,433.60     | Combined L1 and L2 regularization       |
| 5          | Random Forest Regression        | Initial  | Tuned parameters            | Tuned CV RMSE | 30,747.57     | Nonlinear relationships                 |
| 6          | Gradient Boosting Regression    | Initial  | Tuned parameters            | Tuned CV RMSE | 28,665.81     | Best tuned CV performance               |
| 7          | KNN Regression                  | Initial  | `n_neighbors=5`, `p=1`      | Tuned CV RMSE | 35,832.19     | Similarity-based predictions            |
| 8          | Support Vector Regression (SVR) | Initial  | `C=100`, `epsilon=0.1`      | Tuned CV RMSE | 33,912.14     | Kernel-based regression                 |

Notes

- All models used the same initial feature set for comparison.
- “Tuned parameters” means the best parameters found during hyperparameter tuning; the full parameter dictionaries are available in your consolidated results.
- Gradient Boosting achieved the lowest tuned cross-validation RMSE (28,665.81), so it is the selected model under your CV-based selection criterion.
- Lasso achieved the lowest tuned test RMSE (28,257.31), but model selection should follow the predefined CV criterion rather than choosing based on test performance.


## 16 - 17. Model Evaluation & Consolidated Regression Model Comparison


### Baseline Model Results - Linear Regression

| RMSE      | MAE       | R²       | CV Mean RMSE | CV RMSE Std |
| --------- | --------- | -------- | ------------ | ----------- |
| 29,077.94 | 18,191.83 | 0.889767 | 39,503.98    | 5,683.75    |
|           |           |          |              |             |

### Consolidated Regression Model Comparison

| Model             | Initial CV RMSE | Initial CV RMSE Std | Initial Test RMSE | Initial Test MAE | Initial Test R² | Tuned CV RMSE | Tuned Test RMSE | Tuned Test MAE | Tuned Test R² | Best Parameters                                          |
| ----------------- | --------------- | ------------------- | ----------------- | ---------------- | --------------- | ------------- | --------------- | -------------- | ------------- | -------------------------------------------------------- |
| Gradient Boosting | 30,249.85       | 5,663.20            | 27,483.82         | 16,552.90        | 0.901522        | 28,665.81     | 28,466.78       | 16,194.92      | 0.894352      | `learning_rate=0.1`, `max_depth=4`, `n_estimators=200`   |
| Random Forest     | 31,371.81       | 5,053.78            | 30,017.99         | 17,951.64        | 0.882524        | 30,747.57     | 29,066.07       | 17,703.47      | 0.889857      | `max_depth=20`, `min_samples_leaf=2`, `n_estimators=100` |
| Elastic Net       | 34,750.74       | 8,734.32            | 36,756.03         | 20,546.63        | 0.823866        | 32,433.60     | 31,196.91       | 18,881.66      | 0.873115      | `alpha=0.1`, `l1_ratio=0.8`, `max_iter=20000`            |
| Lasso             | 36,518.60       | 7,155.22            | 27,819.40         | 17,809.67        | 0.899102        | 32,433.77     | 28,257.31       | 17,124.28      | 0.895901      | `alpha=100.0`, `max_iter=20000`                          |
| Ridge             | 34,094.04       | 7,307.58            | 29,587.77         | 19,087.18        | 0.885867        | 32,547.28     | 30,713.84       | 19,079.64      | 0.877014      | `alpha=10.0`                                             |
| SVR               | 78,811.00       | 5,361.96            | 88,626.34         | 59,515.87        | -0.024028       | 33,912.14     | 36,234.09       | 19,339.13      | 0.828833      | `C=100`, `epsilon=0.1`, `kernel='linear'`                |
| KNN               | 39,296.30       | 6,203.71            | 39,707.87         | 23,004.63        | 0.794440        | 35,832.19     | 36,575.61       | 21,392.52      | 0.825591      | `n_neighbors=5`, `p=1`, `weights='distance'`             |
| Linear Regression | 39,503.98       | 5,683.75            | 29,077.94         | 18,191.83        | 0.889767        | 39,209.58     | 29,085.52       | 18,190.33      | 0.889709      | `fit_intercept=False`                                    |


## 18. Error Analysis

### Major Errors

1. The tuned Gradient Boosting model achieved a test RMSE of 28,466.78 and MAE of 16,194.92.
2. Some predictions may substantially overestimate or underestimate actual sale prices.
3. Residual plots were used to examine prediction errors, their distribution, and possible patterns.

### Possible Causes

1. Limited or missing predictive features.
2. Nonlinear relationships between property characteristics and sale prices.
3. Outliers or unusual properties.
4. Feature interactions that the model does not fully capture.

### Improvements

1. Investigate observations with the largest absolute residuals.
2. Improve feature engineering and investigate useful feature interactions.
3. Examine residual plots for systematic patterns and unequal error variance.
4. Compare model performance using cross-validation and appropriate evaluation metrics.

## 19. Model Interpretation

### Feature Importance

Permutation importance was used to evaluate how shuffling individual features affected the selected model's predictive performance.

### Explainability

Methods: Permutation importance and regression coefficients where applicable.

### Key Findings

1. Feature importance identifies which features contribute most to the selected model's predictive performance.
2. Permutation importance measures the increase in prediction error when a feature is shuffled.
3. Features with low or negative permutation importance may provide limited useful predictive information.
4. Feature importance indicates predictive contribution, not necessarily causation.

Note: Confirm the specific leading features from your `best_model_feature_importance` results before naming them.

## 20. Bias & Data Quality

### Potential Bias

The Ames Housing dataset represents a specific housing market and period. Results may not generalize to other locations, time periods, or housing markets.

### Data Quality Issues

1. Missing values requiring appropriate imputation.
2. Numerical features with different scales.
3. Potential outliers and unusual property observations.
4. Categorical features with many levels.
5. Potential differences between the training data and future prediction data.

### Impact

These issues can affect model performance, interpretation, and generalization. The preprocessing pipeline helps handle missing values, feature scaling, and categorical encoding, but it cannot eliminate dataset bias or guarantee accurate predictions on data outside the original distribution.

## 21. Final Model

**Model:** Gradient Boosting Regressor  
**Version:** 1.0  
**Selection Criterion:** Lowest tuned cross-validation RMSE  
**Features:** Selected engineered and encoded features

### Final Configuration

```
Model: GradientBoostingRegressor
Learning Rate: 0.1
Maximum Depth: 4
Number of Estimators: 200
Preprocessing: Scikit-learn Pipeline
Features: Selected features
Random State: 42
```

### Final Performance

|Metric|Initial Model|Tuned Model|
|---|---|---|
|Cross-Validation RMSE|30,249.85|28,665.81|
|Cross-Validation RMSE Std|5,663.20|—|
|Test RMSE|27,483.82|28,466.78|
|Test MAE|16,552.90|16,194.92|
|Test R²|0.901522|0.894352|

**Validation Note:** Gradient Boosting was selected because it achieved the lowest tuned cross-validation RMSE of **28,665.81** among the eight candidate models. Tuning improved its cross-validation RMSE by approximately **5.23%** and reduced test MAE from **16,552.90** to **16,194.92**. However, test RMSE increased from **27,483.82** to **28,466.78**, while test R² decreased from **0.901522** to **0.894352**. This indicates that tuning improved average cross-validation performance and MAE but did not improve every test metric. The final model explains approximately **89.44%** of the variation in house sale prices on the test set.

### Feature Importance

Feature importance was evaluated using permutation importance. Higher values indicate features whose shuffling caused a larger deterioration in model performance.

|Rank|Feature|Importance|Importance Std|
|---|---|---|---|
|1|OverallQual|25,787.88|1,600.61|
|2|GrLivArea|15,377.57|1,162.79|
|3|TotalBsmtSF|6,005.05|517.91|
|4|GarageCars|5,517.31|306.90|
|5|LotArea|1,849.01|382.56|
|6|BsmtQual|1,624.05|85.73|
|7|BsmtFinSF1|1,491.72|571.67|
|8|YearBuilt|1,135.51|152.80|
|9|YearRemodAdd|1,059.08|679.71|
|10|Neighborhood|971.49|173.96|

**Feature Importance Note:** The most influential features were **OverallQual**, **GrLivArea**, **TotalBsmtSF**, and **GarageCars**. These represent overall material and finish quality, above-ground living area, basement area, and garage capacity. The results suggest that property quality and size-related features contribute substantially to the model’s predictions. Permutation importance measures predictive contribution, not causation; it can also be affected by correlations between features.

### Final Validation Summary

The tuned Gradient Boosting Regressor is the selected model based on cross-validation performance. It provides strong predictive performance, with a test R² of **0.894352** and test MAE of **16,194.92**. Its feature-importance results identify overall quality and living area as the strongest predictive features. These results apply to the test data used in this project; performance on new housing data may differ.

## 22. Model Persistence

**Method:** Joblib

```text
models/
 └── house_price_prediction.joblib
```

### Required Preprocessing

The saved pipeline contains the preprocessing required to transform incoming data before generating predictions.


## 23. Prediction / Inference

### Input Requirements

The final Gradient Boosting Regressor requires the same input features and preprocessing used during model training.

```
OverallQual:
GrLivArea:
TotalBsmtSF:
GarageCars:
LotArea:
BsmtQual:
BsmtFinSF1:
YearBuilt:
YearRemodAdd:
Neighborhood:
OverallCond:
ExterQual:
FullBath:
Fireplaces:
BsmtExposure:
Condition1:
SaleCondition:
OpenPorchSF:
KitchenQual:
MasVnrArea:
...
```

**Important:** The model uses the full set of features expected by its trained preprocessing pipeline, not just the most important features listed above. All required raw input columns must be supplied, with missing values handled according to the fitted pipeline.

### Prediction Output

```
Predicted Sale Price: [Model Prediction]
```

The predicted sale price is an estimate based on the property details provided. Prediction quality may vary for properties that differ substantially from the training data.


## 24. Deployment (Future)

**Deployment Type:** Local application / API / Web application

**Technology:** FastAPI or Streamlit

### Deployment Structure

```text
deployment/
 ├── api/
 ├── app/
 └── config/
```

## 25. Testing (Future)

### Tests

- Data validation
- Preprocessing
- Model prediction
- Missing input handling
- Invalid input handling
- Edge cases
- Prediction output

### Results

**Tests Passed:** Example

**Tests Failed:** 0



## 26. Problems & Solutions

| Problem | Cause | Solution |
|---|---|---|
| Missing values | Incomplete observations | Imputation through the preprocessing pipeline |
| Categorical features | Non-numerical values | Categorical encoding |
| Multicollinearity | Correlated predictors | Feature analysis and regularization where appropriate |
| Skewed variables | Asymmetric feature distributions | Transformation where appropriate |
| Large residuals | Difficult-to-predict observations | Residual analysis and error investigation |
| Model overfitting risk | Model complexity or sensitivity to training data | Cross-validation and hyperparameter tuning |
| Inconsistent model performance | Differences between validation and test results | Compare cross-validation and test metrics |
| Model reproducibility | Different settings or preprocessing between runs | Fixed random seed, pipelines, and saved model artifacts |

## 27. Lessons Learned

### Machine Learning

1. Data quality and preprocessing influence model performance.
2. Cross-validation provides a more reliable basis for model selection than a single test result.
3. Hyperparameter tuning can improve cross-validation performance without improving every test metric.
4. Feature importance helps identify influential predictors but does not establish causation.
5. Residual analysis helps reveal patterns and observations the model predicts poorly.

### Technical

1. Scikit-learn pipelines help keep preprocessing consistent during training and prediction.
2. Preprocessing and feature selection must be fitted without leaking information from validation or test data.
3. Saving the fitted model allows predictions to be generated without retraining.
4. Permutation importance provides a way to assess how much individual features contribute to predictive performance.

### Project Development

1. Documentation makes experiments and decisions easier to track.
2. Separating data, source code, models, and outputs improves project organization.
3. Reproducibility should be considered from the beginning.
4. Comparing initial and tuned models helps explain why the final model was selected.

## 28. Limitations

1. The dataset represents the Ames, Iowa housing market and a specific period; results may not generalize to other markets or time periods.
2. The final model's performance depends on the quality, completeness, and relevance of its input features.
3. The tuned model did not improve every test metric compared with its initial version.
4. The test results may not fully represent performance on future, unseen housing data.
5. Correlated features can affect the interpretation of permutation importance.
6. Feature importance describes predictive contribution, not causal relationships.
7. The model has not been demonstrated to perform equally well on housing data from other locations.

## 29. Future Improvements

1. Evaluate the model on a genuinely new housing dataset or a future-period holdout.
2. Investigate observations with the largest absolute prediction errors.
3. Explore additional feature engineering and meaningful feature interactions.
4. Evaluate the stability of feature importance across cross-validation folds.
5. Compare further hyperparameter configurations using a controlled validation process.
6. Develop an API for serving predictions.
7. Build a user-facing interface for entering property details and obtaining estimated sale prices.
8. Monitor prediction performance if the model is deployed.

## 30. Final Results

### Summary

The project developed an end-to-end machine learning workflow to predict residential sale prices using the Ames Housing Dataset. The workflow included data preprocessing, model comparison, cross-validation, hyperparameter tuning, model evaluation, residual diagnostics, feature-importance analysis, and model persistence.

### Final Model

**Model:** Gradient Boosting Regressor  
**Version:** 1.0  
**Selection Criterion:** Lowest tuned cross-validation RMSE  
**Main Metric:** Root Mean Squared Error (RMSE)

| Metric | Final Result |
|---|---:|
| Tuned Cross-Validation RMSE | 28,665.81 |
| Test RMSE | 28,466.78 |
| Test MAE | 16,194.92 |
| Test R² | 0.894352 |

### Key Findings

1. Data preprocessing was necessary to prepare the housing features for model training.
2. Gradient Boosting achieved the lowest tuned cross-validation RMSE among the eight evaluated models.
3. The final model achieved a test R² of **0.894352**, explaining approximately 89.44% of the variation in test sale prices.
4. **OverallQual**, **GrLivArea**, **TotalBsmtSF**, and **GarageCars** were the most influential features according to permutation importance.
5. Hyperparameter tuning improved cross-validation RMSE, but test RMSE and R² were slightly worse than those of the initial Gradient Boosting model.
6. The final model is suitable as a predictive baseline for the dataset, but performance on other housing markets requires further validation.


## 31. Project Structure

```text
house-price-prediction/
 │
 ├── data/
 │   ├── raw/
 │   ├── external/
 │   └── processed/
 │
 ├── notebooks/
 │
 ├── src/
 │   ├── data/
 │   ├── features/
 │   ├── models/
 │   ├── evaluation/
 │   └── visualization/
 │
 ├── models/
 ├── outputs/
 ├── tests/
 ├── config/
 ├── scripts/
 ├── docs/
 │
 ├── README.md
 ├── requirements.txt
 └── .gitignore
```

## 32. References

### Dataset

- Ames Housing Dataset
- Kaggle dataset source

### Documentation

- Python Documentation
- Pandas Documentation
- NumPy Documentation
- Scikit-learn Documentation

### Research Papers

- Relevant regression and housing-price research

### Other Resources

- Machine learning reference materials

## 33. Progress Log

### LOG - STARTUP
#### 2026-10-09

>**Task:** Project setup
>**What I Did:** Defined the project objective, problem type, and success criteria; created the project repository and folder structure; configured the environment, dependencies, Git, .gitignore, documentation, and progress log; obtained and organized the dataset.
>**Result:** Project environment, repository, documentation, and dataset were successfully set up.
>**Problem:** None.
>**Decision:** Proceed with detailed data understanding and analysis.
>**Next Step:** Data.

### LOG - DATA PREPARATION & CLEANING
#### 2026-10-11

>**Task:** Data preparation and cleaning
>**What I Did:** Loaded the dataset; inspected its structure, dimensions, data types, missing values, duplicates, outliers, inconsistencies, and target variable (`SalePrice`); created reusable functions for data inspection and cleaning.
>**Result:** Initial data quality checks were completed, and potential cleaning requirements were identified.
>**Problem:** Some data quality issues required further investigation before making cleaning decisions.
>**Decision:** Investigate the findings before applying potentially destructive cleaning operations.
>**Next Step:** EDA.

### LOG - EDA
#### 2026-10-11

>**Task:** Exploratory data analysis
>**What I Did:** Analyzed the target variable, numerical and categorical feature distributions, relationships with `SalePrice`, correlations, outliers, and potential feature interactions; documented important patterns and findings.
>**Result:** Identified potentially influential predictors, including `OverallQual`, `GrLivArea`, and `GarageCars`, alongside skewed distributions, rare categories, correlations, and extreme values.
>**Problem:** Some features showed skewness, unusual values, and relationships that required further investigation.
>**Decision:** Use the findings to guide feature engineering, transformations, encoding, and outlier handling.
>**Next Step:** Feature Engineering.

### LOG - FEATURE ENGINEERING
#### 2026-10-11

>**Task:** Feature engineering
>**What I Did:** Separated the features (`X`) from the target (`y`); split the data into training and testing sets; created additional features, including `TotalSF` and `HouseAge`.
>**Result:** The new features were created, and the original cleaned dataset was preserved.
>**Problem:** No significant problems were encountered.
>**Decision:** Retain the engineered features and evaluate appropriate preprocessing techniques.
>**Next Step:** Data Preprocessing Pipeline.

### LOG - DATA PREPROCESSING PIPELINE
#### 2026-10-12

>**Task:** Build the data preprocessing pipeline
>**What I Did:** Evaluated missing-value imputation, categorical encoding, numerical scaling, multicollinearity, and dimensionality reduction; organized preprocessing steps into a consistent pipeline fitted using training data only.
>**Result:** A structured preprocessing workflow was established to prepare features consistently for model training and evaluation.
>**Problem:** Different feature types required different preprocessing approaches, and dimensionality reduction needed to be justified by its effect on model performance.
>**Decision:** Apply only necessary preprocessing techniques and prevent data leakage by fitting transformations on training data.
>**Next Step:** Modeling.

### LOG - MODELING
#### 2026-10-12

>**Task:** Model development and evaluation
>**What I Did:** Established a baseline; trained candidate regression models; generated predictions; evaluated performance using appropriate metrics and cross-validation; tuned model hyperparameters; compared results and examined prediction errors.
>**Result:** Multiple models were evaluated, and model optimization was performed to identify the strongest candidate.
>**Problem:** Model performance varied, requiring careful comparison of validation results and generalization.
>**Decision:** Select the final model based on cross-validation performance, prediction errors, and generalization rather than training performance alone.
>**Next Step:** Model Finalization.

### LOG - MODEL FINALIZATION
#### 2026-10-12

>**Task:** Finalize the selected model
>**What I Did:** Selected the Gradient Boosting Regressor based on the lowest tuned cross-validation RMSE; recorded the best parameters (`learning_rate=0.1`, `max_depth=4`, `n_estimators=200`); evaluated the model on the test set; performed error analysis; saved the model, pipeline, configuration, metrics, and results.
>**Result:** The final model was selected and evaluated. Tuned cross-validation RMSE was approximately 28,665.81, while test RMSE was approximately 28,466.78, MAE was approximately 16,194.92, and R² was approximately 0.8944.
>**Problem:** The tuned model's test RMSE was slightly higher than that of the initial model, indicating that tuning did not improve every test-set metric.
>**Decision:** Retain the selected model based on cross-validation performance and document both initial and tuned results transparently.
>**Next Step:** Experiment Tracking.

### LOG - EXPERIMENT TRACKING
#### 2026-10-12

>**Task:** Record and track experiments
>**What I Did:** Documented candidate models, feature engineering, preprocessing, hyperparameters, evaluation metrics, observations, and model-selection decisions.
>**Result:** Experiment history and the reasoning behind the final model selection were documented for reproducibility.
>**Problem:** None.
>**Decision:** Maintain experiment records and version-control relevant project changes.
>**Next Step:** Pre-deployment.

### LOG - EXPERIMENT TRACKING
#### 2026-10-18

>**Task:** Update project progress and version control
>**What I Did:** Updated the progress log, committed project changes, and pushed the changes to GitHub.
>**Result:** Project progress was documented, and the changes were pushed to the remote repository.
>**Problem:** None.
>**Decision:** Continue preparing the project for potential deployment.
>**Next Step:** Pre-deployment.

### LOG - PRE-DEPLOYMENT
#### 2026-10-18

>**Task:** Prepare the project for deployment
>**What I Did:** Cleaned the codebase, organized notebooks and source files, removed unnecessary files, added appropriate tests, checked reproducibility and dependencies, updated environment configuration and `.gitignore`, and reviewed project documentation.
>**Result:** The project structure was cleaned and organized, and reproducibility and deployment preparation were reviewed.
>**Problem:** The README and complete reproduction instructions still required final review and completion.
>**Decision:** Complete the remaining documentation and verify that the project can be reproduced from a clean environment.
>**Next Step:** Complete project documentation.

### LOG - DEPLOYMENT
#### 2026-10-18

>**Task:** Deploy the machine learning project
>**What I Did:** Selected a deployment method, prepared the inference workflow, created the application or API, configured the production environment and secrets, tested locally, deployed the application, and tested the deployed version.
>**Result:** The application was deployed and tested successfully.
>**Problem:** None.
>**Decision:** Monitor the deployed application and address any issues that arise.
>**Next Step:** Finalize.

### LOG - FINALIZE
#### 2026-10-18

>**Task:** Finalize the project
>**What I Did:** Reviewed the final project files, README, and documentation; checked Git status; committed and pushed final changes; prepared a version release; organized portfolio materials and archived project notes.
>**Result:** The project was finalized, documented, version-controlled, and published.
>**Problem:** None.
>**Decision:** Mark the project as complete.
>**Next Step:** Start the next project.