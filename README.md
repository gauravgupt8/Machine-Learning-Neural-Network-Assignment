# Boston House Price Prediction

## Project Overview
This project focuses on predicting housing prices in Boston using machine learning models. By leveraging data from the Boston housing dataset, we aim to identify the most influential factors affecting house prices and develop models that provide accurate predictions. The project includes data preprocessing, exploratory data analysis (EDA), feature selection, and model evaluation.

## Dataset Description
The dataset contains information about housing attributes and median house prices (MEDV) in $1000s. Key features include:
- **CRIM**: Crime rate per capita by town.
- **ZN**: Proportion of residential land zoned for lots over 25,000 sq. ft.
- **INDUS**: Proportion of non-retail business acres per town.
- **RM**: Average number of rooms per dwelling.
- **LSTAT**: Percentage of the population with lower socio-economic status.
- **MEDV**: Median value of owner-occupied homes (target variable).

The dataset does not contain any null values, making it ideal for machine learning tasks.

## Project Workflow
### 1. **Data Preprocessing**
- **Outlier Treatment**: Outliers in numeric features were identified using interquartile range (IQR) and treated using Winsorization.
- **Feature Scaling**: Normalization was applied to ensure that all features contribute equally to the model.

### 2. **Exploratory Data Analysis (EDA)**
- Distribution of features was analyzed using histograms and box plots.
- Skewness in features such as `CRIM` and `ZN` was identified.
- The `CHAS` feature, which has low variance, was dropped.

### 3. **Feature Selection**
- A Random Forest Regressor was used to rank feature importance.
- Key predictors of `MEDV` were identified: `LSTAT`, `RM`, `DIS`, and `CRIM`.

### 4. **Predictive Modeling**
#### Models Used:
- **Linear Regression**: Simple model assuming linear relationships.
- **Random Forest Regressor**: Ensemble model capturing non-linear patterns.
- **Support Vector Machine (SVM)**: Regression variant for complex relationships.

#### Performance Metrics:
- **Mean Squared Error (MSE)**
- **R-squared (R²)**

#### Results:
| Model                   | MSE  | R²    |
|--------------------------|------|-------|
| Linear Regression        | 24.35 | 0.73 |
| Random Forest Regressor  | 12.80 | 0.89 |
| Support Vector Machine   | 20.45 | 0.77 |

### 5. **Visualizations**
- Feature importance was visualized using bar charts.
- Data distributions and outlier effects were explored using Seaborn and Matplotlib.

## Tools and Technologies
- **Python**: Programming language for analysis and modeling.
- **Libraries**: NumPy, Pandas, Scikit-learn, Seaborn, Matplotlib.
- **Models**: Linear Regression, Random Forest Regressor, SVM.