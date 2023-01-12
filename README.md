# Wine_Quality_Classification

The goal of this task is to train a model that can accurately predict the quality of wine based on a set of features.

### Data 

Source - ![Kaggle](https://www.kaggle.com/datasets/yasserh/wine-quality-dataset)

The dataset is clean hence no extra cleaning is needed to work with it. 

The Number of unique categories in our target variable wine is 6. Wine records having quality of 3,4 and 8 account for less than 5% of dataset. Most of wine samples have quality of 5 or 6 (over 80% of all records) indicating an imbalanced dataset. The data needs to be balanced before using for model building. Using an imbalanced dataset will cause our models to perform poorly because the minority class will be ignored and be biased towards the majority class.

Also, some features in the dataset were highly skewed and needed to be normalized using the np.log function.

### Modelling

Before building the models, the data is first balanced using SMOTE to oversample the minority class. Next is to use cross validation to evaluate the selected models to choose the best model for this classification project.

| Model | Cross Validation Score |
|---|---|
| Logistic Regression | 58% |
| KNN | 78% |
| Decision Tree | 76% |
| Gaussian NB | 52% |
| Random Forest | 85% |