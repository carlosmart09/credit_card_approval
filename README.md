# Credit Card Approval

## Overview

This project aims to build a credit card approval system using machine learning techniques. The goal is to predict whether an applicant will be approved for a credit card based on various features.


## Features and Components

### Feature Engineering

In our credit card approval system, we performed essential feature engineering steps to prepare the data for model training. Here are the details:

1. **Label Encoding for Categorical Features**:
   
We encountered categorical features in our dataset. To make them compatible with machine learning algorithms, we applied label encoding. This process assigns a unique numeric value to each category within a feature.

2. **Standard Scaling**:

Standard scaling (also known as z-score normalization) was applied to our dataset.
Specifically, we focused on column 12, which had high values. Standard scaling ensures that all features have a mean of 0 and a standard deviation of 1. This helps prevent any feature from dominating the model due to its scale.
By performing these feature engineering steps, we ensured that our data was appropriately prepared for model training.

### Model Selection: K-Nearest Neighbors (KNN)
#### Overview
In our credit card approval system, we assessed several machine learning models to determine the most suitable one. Among these models—**K-Nearest Neighbors (KNN)**, **Logistic Regression**, and **Decision Tree**—we found that KNN yielded the highest accuracy.

#### K-Nearest Neighbors (KNN)
* **Description**:
  * KNN is a non-parametric and instance-based classification algorithm.
  * It makes predictions based on the majority class of its k nearest neighbors in the feature space.
  * The choice of k (number of neighbors) significantly impacts the model’s performance.
* **Hyperparameter Tuning**:
  * To optimize our KNN model, we performed hyperparameter tuning.
  * Specifically, we experimented with different values of k.
  * After evaluating the model’s performance on validation data, we determined that k = 11 provided the best results.

### Evaluation Metrics

We rigorously assessed model performance using the following evaluation metric:

* **Accuracy**:
  * Accuracy measures the proportion of correctly predicted instances out of the total instances in the dataset.
  * It provides an overall view of the model’s correctness.
    
In our analysis, we considered precision, recall, and F1-score; however, decisions were ultimately based solely on accuracy.

## Data

* **Data Source**:
Our credit card approval dataset was obtained from the **UCI Machine Learning Repository**. 

* **Column Information**:
  * The dataset contains several columns, each representing different features related to credit card applications.
  * However, for privacy reasons, the column names have been encrypted, preventing us from providing explicit details about their meanings.
* **Data Preprocessing Steps**:
1. **Label Encoding for Categorical Features**:
  * Since some features were categorical, we applied label encoding to convert them into numerical representations.
  * Label encoding assigns unique numeric values to each category within a feature.
2. **Handling Null Values**:
  * We identified null values in the dataset.
  * Given that null values accounted for less than 5% of the total dataframe, we decided to drop those rows.
3. **Standard Scaling**:
  * One continuous feature exhibited atypical values significantly above the interquartile range.
  * To ensure consistent scaling across features, we applied standard scaling (z-score normalization) to the entire dataset.



## Results and Visualizations

After evaluating different machine learning models on our credit card approval dataset, we observed the following results:
* **K-Nearest Neighbors (KNN)**:
  * Initially, KNN achieved an accuracy of *86%**.
  * However, by fine-tuning the hyperparameter (number of neighbors), we improved the accuracy to **87%**.
    
!confusion_matrix.png

## Contributing
Feel free to contribute by opening issues or submitting pull requests. Let's make this project better together!

## License

This dataset is licensed under a Creative Commons Attribution 4.0 International (CC BY 4.0) license.

