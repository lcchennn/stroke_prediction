# Stroke Prediction Using Machine Learning Approaches

### Check out the code
#### Stroke Prediction Using Machine Learning:
https://www.kaggle.com/lcchennn/stroke-prediction-using-machine-learning
#### HTML Parsing with Beautiful Soup - NHANES Data Codebook with SAS label:
https://www.kaggle.com/lcchennn/html-parsing-nhanes-data-codebook-with-sas-label

## I. Introduction
Stroke is the fifth cause of death in the United States, according to the Heart Disease and Stroke Statistics 2020 report. Those who suffer from stroke, if luckily survived, may also suffer from expensive medical bills and even disability. Foreseeing the underlying risk factors of stroke is highly valuable to stroke screening and prevention. In this project, the National Health and Nutrition Examination Survey (NHANES) data from the National Center for Health Statistics (NCHS) is used to develop machine learning models. The NHANES dataset holds an abundance of variables, ranging from demographics, medical history, physical examinations, biochemistry to dietary and lifestyle questionnaires. Known features contributing to stroke, such as blood pressure, serum cholesterol level, alcohol consumption, weight, etc., and additional features will be selected for correlation evaluation and machine learning model development

## II. Data Loading and Cleaning
1. Exclude rows will null value or NA for the target variable "MCQ160F" (“Has a doctor or other health professional ever told you that you had a stroke?”).
2. Exclude columns with over 50% missing data.
3. Missing data inputation with strategy='most_frequent'.

## III. Feature Selection
1. Train/Test split
2. Train/predict with XGBoost before data preprocessing, result showed false high accuracy where recall for the minority class is very low.
3. Oversampling with imblearn.SMOTE.
4. Using XGBoost for feature selection after oversampling.

### Class imbalance
<br>![image](https://user-images.githubusercontent.com/52438350/111051627-5de82880-8409-11eb-8005-b84459673291.png)

### 24 top features selected
<br>![image](https://user-images.githubusercontent.com/52438350/111051229-6723c600-8406-11eb-810c-d9eaae6d4e52.png)
<br>![image](https://user-images.githubusercontent.com/52438350/111051618-41e48700-8409-11eb-8fd4-d60754fc8c8f.png)

### Feature correlation
<br>![image](https://user-images.githubusercontent.com/52438350/111051240-7c005980-8406-11eb-8438-fad1f162e128.png)

## IV. Model Training
1. Train/Test split
2. Data normalization with sklearn.preprocessing.NormalScaler
3. Logistic Regressio, Random Forest, Adaptive Boosting, Gradient Boosting, SVM, XGBoost model training and prediction.

## V. Model Comparison
Accuracy score comparison.
![image](https://user-images.githubusercontent.com/52438350/111051245-90445680-8406-11eb-898f-775861bb53b5.png)

## VI. Future Work
1. Model optimization/hyperparameter tuning
2. Ensamble
3. ROC/AUC comparison

## References
1. NHANES Datasets from 2013-2014
https://www.kaggle.com/cdc/national-health-and-nutrition-examination-survey
2. A data-driven approach to predicting diabetes and cardiovascular disease with machine learning
https://pubmed.ncbi.nlm.nih.gov/31694707/
3. Codebook
https://wwwn.cdc.gov/nchs/nhanes/Search/DataPage.aspx?Component=Demographics&CycleBeginYear=2013

