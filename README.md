# Turkey Electricity Price Day-Ahead Market Forecasting: 

This project presents a model developed for forecasting electricity prices in Turkey. Forecasting daily electricity prices in Turkey holds strategic importance for energy suppliers, energy consumers, and market participants. This model can assist companies operating in the energy sector and researchers in improving their price forecasts, planning operations, and managing resources.

## Dataset and Preprocessing (EDA)

### Dataset

The dataset used in this project represents the day-ahead electricity market from the IExchange Istanbul (EXIST) over a 5-year period. The dataset includes the following variables:

- **Date**: Date
- **Hour**: Hour
- **HOLY**: Holiday (Yes/No)
- **MCP**: Market Clearing Price (Dependent Variable)
- **Other independent variables**: **MCP_24**, **MCP_168**, **MCP_672**, **PISO**, **PIBO**, **SSOV**, **SBOV**, **MO**, **MB**, **TV**, **DER**, **TG**, **NG**, **HYD**, **LIG**, **RYHD**, **ICOAL**, **WIND**, **SOL**, **FUEL**, **GEO**, **ASPH**, **BCOAL**, **BIO**, **IMEX**, **WAS**, **GASP**, **ANK**, **IST**

### EDA Steps

The `EDA_Project.ipynb` file includes the following steps:

1. **Duplicate Values**: Checking and removing duplicate values.
2. **Null Values in Data**: Identifying missing values in the data.
3. **Data Types that are Objects**: Editing data types that are objects.
4. **Editing Data Types**: Adjusting data types.
5. **Descriptive Statistics**: Calculating descriptive statistics.
6. **Correlation**: Examining correlations between variables.
7. **Handling with Missing Values**: Dealing with missing values.
8. **Univariate & Multivariate Analysis**: Performing univariate and multivariate analyses.
9. **MCP_USD (Target Feature)**: Analyzing the target feature (MCP).

## Model Training and Evaluation

### Data Preprocessing

The `Vanilla-Crossvalidation-GridSearch.ipynb` file includes the following preprocessing steps:

1. Data Preprocessing: Initial data preprocessing steps.
2. Train / Test Split**: Splitting the data into training (80%) and testing (20%) sets.
3. Scaling: Scaling the data.

### Models Used

1. Random Forest Regressor 
   - Vanilla RF
   - Cross Validation RF
   - RF GridSearchCV
   - Error Metrics

2. Support Vector Regressor (SVR)
   - Vanilla SVR
   - Cross Validation SVR
   - SVR GridSearchCV
   - Error Metrics

3. Decision Tree Regressor
   - Vanilla DT
   - Cross Validation DT
   - DT GridSearchCV
   - Error Metrics

4. Sequential Model
   - Vanilla Sequential Model
   - Error Metrics

5. XGBoost Model
   - Vanilla XGB
   - Cross Validation XGB
   - XGB Model GridSearchCV
   - Error Metrics

6. CatBoost Regressor
   - Vanilla CatBoost
   - Cross Validation CatBoost
   - CatBoost GridSearchCV
   - Error Metrics

7. LightGBM Regressor
   - Vanilla LightGBM
   - Cross Validation LightGBM
   - LightGBM GridSearchCV
   - Error Metrics

### Evaluation Metrics:

**Standard evaluation metrics for electricity price forecasting include multiple scalar metrics such as R-squared, MAE, MAPE, RMSE, and MSE.**

## Tuned Model and SHAP Analysis

### Tuned Modeling

The `Tuned_Hyperparameter.ipynb` file includes the following steps:

1. **Tuned Modeling**: Hyperparameter optimization for models.
2. **SHAP Value Analysis**: Analyzing SHAP values for each model.
3. **Model Performance Comparison**: Identifying the best-performing model. The LightGBM model showed the best performance.

## Usage Instructions

The project code and dataset are available in the GitHub repository. Follow the steps below to run the project:

### Clone the Repository

git clone https://github.com/TheEmgame/EPF-Turkish-Day-Ahead-Market.git
cd EPF-Turkish-Day-Ahead-Market

### Download and Prepare the Dataset
Download the dataset and place it in the data folder. Ensure the dataset is in the correct format for EDA and model training steps.
### Run EDA Steps
Use the EDA_Project.ipynb file to perform the preprocessing and exploratory data analysis steps on the dataset.

### Run Train and Evaluate Models
Use the Vanilla-Crossvalidation-GridSearch.ipynb file to train various models and compute evaluation metrics.

### Tuned Models and SHAP Analysis
Use the Tuned_Hyperparameter.ipynb file to perform hyperparameter optimization for the models and analyze the SHAP values to understand feature importance.

## Results and Discussion

The models developed in this project were successfully used to forecast market clearing prices in the Turkey day-ahead electricity market. According to the evaluation metrics, the LightGBM model provided the best performance. The strategic applications of this model and how the results can be utilized in the energy market have been discussed.

## Forecast Models:

It includes seven different forecast models that can be automatically used in any day-ahead market without the need for expert knowledge.
