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


## Findings and Observations from the Data

![Important Features (Random Forest)](https://raw.githubusercontent.com/RezuwanHassan262/Adult-Income-Prediction-Machine-Learning/main/figures/1.png)

![Partial Dependence Plot](https://raw.githubusercontent.com/RezuwanHassan262/Adult-Income-Prediction-Machine-Learning/main/figures/2.png)

From the partial dependence plot above, we can infer,

1. Relationship: This plot indicates how different relationship statuses influence income predictions.
      * Value 0 ("Husband") has the highest partial dependence, indicating that being a "Husband" is strongly associated with a higher income probability.
      * Values 1–4 ("Not-in-family," "Own-child," and "Unmarried,"): These are relationship statuses like "Not-in-family," "Own-child," or "Unmarried," which are associated with much lower income probabilities.
      * Value 5 ("Wife") shows a slight increase in partial dependence compared to intermediate statuses but remains lower than "Husband."

        Key Insight: Traditional roles like "Husband" have higher predicted income levels.

2. Education: This plot shows the impact of years of education on income.
      * Education < 6 years: The partial dependence is flat and low, indicating little impact on income prediction.
      * Education > 10 years: As education increases beyond 10 years, the partial dependence sharply rises, peaking at around 15–16 years. Suggesting that advanced education strongly correlates with higher income predictions.

        Key Insight: Education level is a strong predictor of income, and the effect becomes significant at higher levels of education.



## Predicting Survival using ML algorithms

I tried to predict the survival chances of passengers using different ML algorithms, Those are mentioned below with accuracy and relevant metrics.


![Decision Tree Classifier (Small)](https://raw.githubusercontent.com/RezuwanHassan262/Adult-Income-Prediction-Machine-Learning/main/figures/3.png)

![Decision Tree Classifier (Large)](https://raw.githubusercontent.com/RezuwanHassan262/Adult-Income-Prediction-Machine-Learning/main/figures/4.PNG)

The above 2 figures (Small and Large) are the decision tree classifier visualizations. The performances of the classifiers are given below, Mean Absolute Error (MAE) was utilized to evaluate the model performances.


|          ML Algorithm             |   Mean Absolute Error   |
| --------------------------------- |:-----------------------:|
| Decision Tree Classifier (Small)  |          15.5           | 
| Decision Tree Classifier (Large)  |          14.5           | 
|    Random Forest Classifier       |          13.6           | 
|   Gradient Boosting Classifier    |          12.6           |
