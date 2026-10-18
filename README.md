# House Price Prediction

A machine learning project that predicts residential house sale prices using the Ames Housing dataset. The project covers data preparation, exploratory data analysis, feature engineering, model comparison, hyperparameter tuning, evaluation, and feature importance analysis.

## Project Overview

**Objective:** Predict house sale prices (`SalePrice`) using property characteristics.

**Dataset:** Ames Housing Dataset  Kaggle House Prices: Advanced Regression Techniques.

**Problem type:** Supervised learning - Regression.

**Final model:** Gradient Boosting Regressor.

**Tools and technologies:**
- Python
- pandas and NumPy
- scikit-learn
- Matplotlib and Seaborn
- JupyterLab
- Git and GitHub

## Dataset

The dataset contains 1,460 training observations and 81 columns, including the target variable `SalePrice`.

The features describe different aspects of residential properties, including:
- Overall quality and living area
- Basement and garage characteristics
- Lot size and neighborhood
- Construction and remodeling years
- Property type and other housing characteristics

**Target variable:** `SalePrice`, the house's sale price in US dollars.

**Dataset source:** [Kaggle — House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

Download the dataset from Kaggle and place the required CSV file or files in the project's data directory, following the structure used by the notebooks.

## Project Workflow

The project follows a typical machine learning workflow:

1. **Data loading** — Load the dataset into pandas DataFrames.
2. **Data inspection** — Examine the shape, data types, summary statistics, and target distribution.
3. **Exploratory data analysis** — Investigate relationships between property characteristics and sale prices.
4. **Data cleaning** — Handle missing values and prepare numerical and categorical columns.
5. **Feature engineering** — Create additional features, including `TotalSF` and `HouseAge`.
6. **Data splitting** — Separate training and testing data.
7. **Preprocessing** — Prepare features for the selected algorithms.
8. **Model training** — Train and compare multiple regression algorithms.
9. **Model evaluation** — Compare performance using cross-validation and test-set metrics.
10. **Hyperparameter tuning** — Search for better Gradient Boosting Regressor settings.
11. **Feature importance** — Investigate which features contribute most to predictive performance.
12. **Model selection** — Select the model with the lowest tuned cross-validation RMSE.

## Models Compared

The following regression algorithms were evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Elastic Net
- Random Forest Regressor
- Gradient Boosting Regressor
- K-Nearest Neighbors Regressor
- Support Vector Regression (SVR)

The final model was selected based on its tuned cross-validation RMSE.

## Model Performance

The Gradient Boosting Regressor was selected as the final model.

### Initial Model

| Metric | Result |
|---|---:|
| Cross-validation RMSE | 30,249.85 |
| Cross-validation RMSE standard deviation | 5,663.20 |
| Test RMSE | 27,483.82 |
| Test MAE | 16,552.90 |
| Test R² | 0.9015 |

### Tuned Model

The selected hyperparameters were:

| Hyperparameter | Value |
|---|---:|
| `learning_rate` | 0.1 |
| `max_depth` | 4 |
| `n_estimators` | 200 |

| Metric | Result |
|---|---:|
| Cross-validation RMSE | 28,665.81 |
| Test RMSE | 28,466.78 |
| Test MAE | 16,194.92 |
| Test R² | 0.8944 |

### Interpreting the Results

- **RMSE:** Measures prediction error, penalizing larger errors more heavily. Lower is better.
- **MAE:** Measures the average absolute difference between predicted and actual sale prices. Lower is better.
- **R²:** Measures the proportion of target variance explained by the model relative to a mean-prediction baseline. Higher is generally better.

The tuned model improved cross-validation RMSE and test MAE compared with the initial model. However, its test RMSE increased and its test R² decreased. Hyperparameter tuning therefore improved some metrics but did not improve every test-set metric.

All error values are expressed in US dollars because the target variable is `SalePrice`.

## Feature Importance

Permutation importance was used to investigate which features most affected the model's predictive performance.

The ten most important features were:

| Rank | Feature | Mean importance |
|---:|---|---:|
| 1 | `OverallQual` | 25,787.88 |
| 2 | `GrLivArea` | 15,377.57 |
| 3 | `TotalBsmtSF` | 6,005.05 |
| 4 | `GarageCars` | 5,517.31 |
| 5 | `LotArea` | 1,849.01 |
| 6 | `BsmtQual` | 1,624.05 |
| 7 | `BsmtFinSF1` | 1,491.72 |
| 8 | `YearBuilt` | 1,135.51 |
| 9 | `YearRemodAdd` | 1,059.08 |
| 10 | `Neighborhood` | 971.49 |

The results indicate that overall quality, above-ground living area, basement area, and garage capacity were particularly influential in the model's predictions.

**Important:** Permutation importance measures predictive usefulness, not causation. It does not prove that changing a feature will cause a particular change in house price.

## Project Structure

The following is a suggested structure. Adjust the paths to match the files in your repository.

```text
house_price_prediction/
├── data/
│   └── README.md
├── notebooks/
│   └── house_price_prediction.ipynb
├── models/
│   └── README.md
├── reports/
│   └── figures/
├── src/
├── requirements.txt
├── .gitignore
└── README.md
```

- `data/` — Dataset files or instructions for obtaining them.
- `notebooks/` — Jupyter notebooks containing analysis and experiments.
- `models/` — Saved model artifacts, if included.
- `reports/figures/` — Charts and other generated visual outputs.
- `src/` — Reusable Python modules, if the project uses them.
- `requirements.txt` — Python package dependencies.
- `.gitignore` — Files and directories that Git should not track.
- `README.md` — Project documentation.

Only include directories and filenames that actually exist in the repository. Large datasets and generated model files may be better kept outside Git or managed using an appropriate data-versioning approach.

## Getting Started

### 1. Install Prerequisites

Install:
- Git
- Python 3.12 or another compatible Python version
- JupyterLab, installed later through the project's dependencies

Verify that Python and Git are available:

```bash
python --version
git --version
```

### 2. Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/YOUR_USERNAME/house_price_prediction.git
cd house_price_prediction
```

Replace the example GitHub URL with the actual URL of your repository.

Cloning an existing repository already configures the remote named `origin`. You do not need to run `git init` or `git remote add origin` after cloning.

### 3. Create a Virtual Environment

Create a project-specific virtual environment:

```bash
python -m venv .venv
```

A virtual environment isolates this project's Python packages from other projects and the system-wide Python installation.

### 4. Activate the Virtual Environment

**Windows PowerShell:**

```powershell
.\.venv\Scripts\Activate.ps1
```

**Windows Command Prompt (CMD):**

```bat
.venv\Scripts\activate.bat
```

After activation, your terminal will usually display `(.venv)` at the beginning of the command prompt.

If PowerShell blocks activation because of its execution policy, you can use Command Prompt or consult the official Python documentation for the appropriate activation guidance.

### 5. Verify the Environment

With the virtual environment activated, run:

```bash
python --version
where.exe python
python -m pip --version
```

On Windows, `where.exe python` should list the virtual environment's Python executable first.

The `python -m pip --version` command should also indicate that pip belongs to the virtual environment.

### 6. Install Dependencies

Upgrade pip within the active virtual environment:

```bash
python -m pip install --upgrade pip
```

Install the project's dependencies:

```bash
python -m pip install -r requirements.txt
```

**Important:** Always activate `.venv` before installing packages, and use `python -m pip` instead of a standalone `pip` command. This helps ensure that packages are installed into the intended Python environment.

If the repository does not yet contain `requirements.txt`, install the necessary packages:

```bash
python -m pip install pandas numpy scikit-learn matplotlib seaborn joblib jupyterlab
```

Then generate the dependency file:

```bash
python -m pip freeze > requirements.txt
```

Review the generated file before committing it. Ideally, it should reflect the packages required by the project rather than unrelated packages installed in the environment.

### 7. Launch JupyterLab

With the virtual environment activated, run:

```bash
jupyter lab
```

Open the notebook associated with the project and execute the cells in their intended order.

If JupyterLab is not found, verify that the environment is active and install it using:

```bash
python -m pip install jupyterlab
```

### 8. Obtain the Dataset

Download the dataset from the [Kaggle competition page](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques).

Follow the notebook's expected paths when placing the files. If the dataset is not included in the repository, ensure that the relevant directory and download instructions are documented.

## Reproducibility

For consistent results:

- Use the documented Python environment and dependencies.
- Set random seeds where supported.
- Keep training and test data separate.
- Fit preprocessing steps using training data only.
- Use cross-validation for model comparison and hyperparameter tuning.
- Evaluate the final selected model on held-out test data.
- Record the model parameters and evaluation metrics.

Results can vary if package versions, random seeds, data splits, or preprocessing procedures differ.

## Limitations and Future Improvements

Potential improvements include:

- Testing additional feature-engineering approaches.
- Comparing alternative gradient-boosting implementations.
- Examining residuals and prediction errors across different price ranges.
- Using more systematic hyperparameter search.
- Evaluating model stability across different data splits.
- Saving the complete preprocessing and prediction pipeline.
- Building a simple interface or API for house-price predictions.

The model's performance on the original test split does not guarantee equivalent performance on future housing data.

## References

- [Kaggle — House Prices: Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)
- [Python Documentation](https://docs.python.org/3/)
- [Python `venv` Documentation](https://docs.python.org/3/library/venv.html)
- [pip Documentation](https://pip.pypa.io/en/stable/)
- [scikit-learn Documentation](https://scikit-learn.org/stable/)

## Author

**Samuel Ablordeppey**

GitHub: `https://github.com/samuelablorh`
