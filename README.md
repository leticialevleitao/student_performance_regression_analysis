# Student Performance Prediction using Regression Models
*Project developed as part of the Atlântico Avanti Data Science Bootcamp regarding student habits performance*

This project investigates how students’ habits and contextual factors influence academic performance.  
Using the [**student_habits_performance**](https://github.com/atlantico-academy/datasets/raw/main/student_habits_performance.csv) dataset, we compare multiple regression models to predict exam scores and identify the most effective and efficient approach.

## Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Jupyter Notebook

## Goals

- Predict students’ exam scores (`exam_score`)
- Compare regression models using multiple evaluation metrics
- Identify which student habits most strongly impact academic performance
- Balance predictive performance and computational efficiency


## Dataset

**student_habits_performance**

The dataset contains behavioral, demographic, and contextual variables, including:

- **Study habits:** `study_hours_per_day`
- **Attendance:** `attendance_percentage`
- **Lifestyle:** `diet_quality`, `exercise_frequency`
- **Mental health:** `mental_health_rating`
- **Contextual factors:** `internet_quality`, `parental_education_level`
- **Demographics:** `age`, `gender`, `part_time_job`, `extracurricular_participation`

**Target variable:**  
- `exam_score`

## Exploratory Data Analysis (EDA)

Key preprocessing and exploration steps:

- Variable typing:
  - Continuous: `study_hours_per_day`, `attendance_percentage`, `exam_score`
  - Discrete: `age`, `exercise_frequency`, `mental_health_rating`
  - Ordinal: `diet_quality`, `parental_education_level`, `internet_quality`
  - Nominal: `gender`, `part_time_job`, `extracurricular_participation`

- Missing value treatment:
  - Mean (continuous)
  - Median (discrete)
  - Mode (categorical)

- Feature scaling:
  - `MinMaxScaler` for all numerical variables

- Encoding:
  - `OrdinalEncoder` for ordinal features
  - `OneHotEncoder` for nominal features

## Modeling Strategy

### Preprocessing Pipeline
- Implemented with `ColumnTransformer`
- Unified handling of imputation, scaling, and encoding

### Hyperparameter Optimization
- `RandomizedSearchCV`
- 5-fold cross-validation
- Model-specific search spaces

### Final Validation
- Monte Carlo Cross-Validation (`ShuffleSplit`)
- 30 repetitions to ensure robustness and stability

## Models Evaluated

- **Linear Regression (LRG)**
- **K-Nearest Neighbors Regressor (KNN)**
- **Decision Tree Regressor (DTR)**
- **Support Vector Regressor (SVR)**

### Evaluation Metrics
- MAE — Mean Absolute Error
- MSE — Mean Squared Error
- R² — Coefficient of Determination
- MAPE — Mean Absolute Percentage Error
- Training Time

