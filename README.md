# **Predicting Boston Housing Prices**
This is my implementation of the Predicting Boston Housing Prices Project<br/>
From Udacity Machine Learning & AI Foundations Nanodegree<br/>
**Machine Learning Project**

![jpg](imgs/img1.jpg)

In this project, you will apply basic machine learning concepts on data collected for housing prices in the Boston, Massachusetts area to predict the selling price of a new home. You will first explore the data to obtain important features and descriptive statistics about the dataset. Next, you will properly split the data into testing and training subsets, and determine a suitable performance metric for this problem. You will then analyze performance graphs for a learning algorithm with varying parameters and training set sizes. This will enable you to pick the optimal model that best generalizes for unseen data. Finally, you will test this optimal model on a new sample and compare the predicted selling price to your statistics.

Things i learnt by completing this project:
* How to explore data and observe features.
* How to train and test models.
* How to identify potential problems, such as errors due to bias or variance.
* How to apply techniques to improve the model, such as cross-validation and grid search.
* How to use the python library for ML, scikit-learn.

# Table of Contents
- [**Predicting Boston Housing Prices**](#predicting-boston-housing-prices)
- [Table of Contents](#table-of-contents)
- [Business Problem](#business-problem)
- [Project Assumptions](#project-assumptions)
- [Data Dictionary](#data-dictionary)
- [Solution Planning](#solution-planning)
  - [Final Product](#final-product)
  - [Tech Stack](#tech-stack)
  - [Process and Methods](#process-and-methods)
- [Business Insights](#business-insights)
- [Conclusion](#conclusion)
- [References](#references)
- [Next Steps](#next-steps)

# Business Problem
The Boston housing market is highly competitive, and you want to be the best real estate agent in the area. To compete with your peers, you decide to leverage a few basic machine learning concepts to assist you and a client with finding the best selling price for their home. Luckily, you’ve come across the Boston Housing dataset which contains aggregated data on various features for houses in Greater Boston communities, including the median value of homes for each of those areas. Your task is to build an optimal model based on a statistical analysis with the tools available. This model will then be used to estimate the best selling price for your clients' homes.

# Project Assumptions
* Some template code was provided.
* The dataset is a little outdated, so it don't represent real-world values for the estimations.
* Some pre-processing was made to the original dataset before it was made available for the project.

# Data Dictionary
The dataset for this project originates from the UCI Machine Learning Repository. The Boston housing data was collected in 1978 and each of the 506 entries represent aggregated data about 14 features for homes from various suburbs in Boston, Massachusetts. For the purposes of this project, the following preprocessing steps have been made to the dataset:
* 16 data points have an 'MEDV' value of 50.0. These data points likely contain missing or censored values and have been removed.
* 1 data point has an 'RM' value of 8.78. This data point can be considered an outlier and has been removed.
* The features 'RM', 'LSTAT', 'PTRATIO', and 'MEDV' are essential. The remaining non-relevant features have been excluded.
* The feature 'MEDV' has been multiplicatively scaled to account for 35 years of market inflation.

Variable | Description
--- | ---
RM  | the average number of rooms among homes in the neighborhood.
LSTAT   | the percentage of homeowners in the neighborhood considered "lower class" (working poor).
PTRATIO | the ratio of students to teachers in primary and secondary schools in the neighborhood.
MEDV    | target variable

# Solution Planning
## Final Product
At the end of this project i will have built a notebook with both analysis of the implemented model and predictions about the price of a house, based on its features. 

## Tech Stack
* Python
* Numpy and Pandas
* Matplotlib
* Scikit-Learn

## Process and Methods
* [Step 0](#step0): Knowing the Data
  * METHOD:
    - Read the dataset documentation.
* [Step 1](#step0): Import Dataset
  * METHOD:
    - Import relevant libraries into the notebook 
    - Read the dataset file 'housing.csv' into a pandas DataFrame
    - Print the size of the dataset
* [Step 2](#step0): Data Exploration
  * METHOD:
    -  Create dataset dictionary
    -  Separate the dataset into features and the target variable
    -  Calculate and display some summary statistics
* [Step 3](#step0): Feature Observation
  * METHOD:
    - Investigate the correlations between each variable with each other
* [Step 4](#step0): Developing a Model
  * METHOD:
    - Define a Performance Metric
    - Shuffle and Split Data
    - Training and Testing
* [Step 5](#step0): Analyzing Model Performance
  * METHOD:
    -  Plot the Learning Curves of the model with different values for the hypeparameters
    -  Investigate the Bias-Variance Tradeoff
* [Step 6](#step0): Evaluating Model Performance
  * METHOD:
    -  Execute Grid Search
    -  Cross-Validation Step
    -  Making Predictions
* [Step 7](#step0): Conclusion
  * METHOD:
    -  Test the resulting model with real-world data, comparing its predicted price with its real value.
    -  Calculate its R2 Score and other metrics

# Business Insights
* **How relevant today is data that was collected from 1978? How important is inflation?**:
  * Slightly relevant, because the infrastructure of the neighborhoods changed, the inflation has changed too, other features that influenciates the final value of the property arose etc. Very important, because it changes the real value of goods and services over a period.
* **Is it fair to judge the price of an individual home based on the characteristics of the entire neighborhood?**:
  * Yes. It is one of the most important factors because it directly influences the quality of life of home owners.
* **Are the features present in the data sufficient to describe a home? Do you think factors like quality of apppliances in the home, square feet of the plot area, presence of pool or not etc should factor in?**:
  * No, because it is missing features that could affect the selling price in today's housing market such as size of a backyard or if there is a garage, number of bathrooms, etc. Totally, yes.

# Conclusion
* **Regarding the model**:
  * An optimal model is not necessarily a robust model. Sometimes, a model is either too complex or too simple to sufficiently generalize to new data. Sometimes, a model could use a learning algorithm that is not appropriate for the structure of the data given. Other times, the data itself could be too noisy or contain too few samples to allow a model to adequately capture the target variable — i.e., the model is underfitted.
* **Regarding the Business Insights**:
  * This type of project is key to companies like a real-state agency, finding a way to predict the values of the homes based on their features increases speed, automate tasks, reduce costs with audit, etc. Such a solution, using ML and Data Science can bring a lot of value to those companies.

# References
- Dataset: Located in the repo as 'housing.csv'
# Next Steps
- Create a more robust network using popular ML frameworks
- Try to generate more insights about this business problems (make more analysis)
- Plot some graphs