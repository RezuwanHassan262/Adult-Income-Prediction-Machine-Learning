# Adult Income Prediction Machine Learning

This project investigates factors influencing income using the Adult Income Dataset. It involves data preprocessing, visualization, and machine learning. Key steps include data cleaning, feature transformation and engineering. Predictive models are developed to classify income levels, providing insights into key determinants.

## Dataset

This was the dataset: Census Income

[UCI Repository](https://archive.ics.uci.edu/dataset/20/census+income) || [Kaggle Version](https://www.kaggle.com/datasets/wenruliu/adult-income-dataset/data)

The Adult Income Dataset is derived from census data and includes a range of demographic and socio-economic attributes relevant to individual income levels.

| Column Name      | Description                                                                                         |
|------------------|-----------------------------------------------------------------------------------------------------|
| age              | Age of the individual                                                                               |
| workclass        | Working class of the individual                                                                     |
| fnlwgt           | Final weight, which is the number of units in the target population that the individual represents  |
| education        | Level of education of the individual                                                                |
| education-num    | Number of years of education of the individual                                                      |
| marital-status   | Marital status of the individual                                                                    |
| occupation       | Occupation of the individual                                                                        |
| relationship     | Relationship status of the individual                                                               |
| race             | Race of the individual                                                                              |
| sex              | Sex of the individual                                                                               |
| capital-gain     | Capital gain of the individual                                                                      |
| capital-loss     | Capital loss of the individual                                                                      |
| hours-per-week   | Number of hours worked per week by the individual                                                   |
| native-country   | Native country of the individual                                                                    |
| income           | Income class of the individual (<=50K or >50K)                                                      |


## Analysis and Workflow

**Reading and Loading Data:** Reading and loading the data properly. 

**Data Preprocessing:** Executing basic analysis of the dataset and processing accordingly. 

**Feature Engineering** Developing new features or modifying existing ones to represent the patterns within the data better.  

**Splitting the dataset:** Splitting the dataset into Train-Test splits to train the ML algorithms.  

**Data Encoding:** Converting categorical or textual data into numerical format to help the algorithms process the input.

**ML Algorithm Implementations:** Implemented different ML classification algorithms on the dataset.

**Seeing the important features:** The factors that were most important in determining the model's predictions.

**Relationship between features:** Trying to understand some features influence the model's output while averaging out the effects of other features using partial dependence plots.


## Predicting Survival using ML algorithms

I tried to predict the survival chances of passengers using different ML algorithms, Those are mentioned below with accuracy and relevant metrics.

|             Algorithm             |   Mean Absolute Error   |
| --------------------------------- |:-----------------------:|
| Decision Tree Classifier (Small)  |          15.5           | 
| Decision Tree Classifier (Large)  |          14.5           | 
|    Random Forest Classifier       |          13.6           | 
|   Gradient Boosting Classifier    |          12.6           |
