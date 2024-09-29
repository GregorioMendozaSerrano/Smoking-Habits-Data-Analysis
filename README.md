# **Data Analysis Exercise:** Smoking Habit Classification 
## Author: Gregorio Mendoza Serrano

### Context
You are working as a data analyst at "HealthData Lab," a leader in epidemiological research and public health data analysis. Your team has collected health data from individuals in an observational study to identify patterns related to smoking habits.

### The Challenge
Use this dataset to classify individuals as smokers or non-smokers. This classification will aid in the development of public health campaigns and in understanding the impacts of smoking on overall health.

### Objective
Based on the provided dataset, your task is to classify each record as a smoker or non-smoker. The categorization should be based on exploratory data analysis and the observed features.

---

## 2. Instructions

### Initial Data Exploration
- **Exercise 1**: State the size of the dataset. Identify which variables are numeric and which are categorical. Who is the lightest individual? Who is the tallest? Draw a histogram of males and females based on whether they smoke or not.
  
- **Exercise 2**: For the continuous variable "age," apply binarization using a threshold at the mean age, including this variable in the DataFrame as "age_bin." Count the two resulting categories in the binarized variable. For the continuous variable "Cholesterol," apply quantile grouping using percentiles and include this variable in the DataFrame as "Cholesterol_per."
  
- **Exercise 3**: For the continuous variable "fasting blood sugar," apply min-max scaling. Draw a histogram of the original variable and another histogram of the scaled variable: what conclusions can you draw by comparing both histograms?
  
- **Exercise 4**: Isolate the discrete variable "blood_group" in a DataFrame consisting of only that variable. Generate three different DataFrames:
  - One with variables generated using one-hot encoding.
  - Another with variables generated using dummy coding.
  - A final one with variables generated using effect coding.

### Data Preprocessing
- **Exercise 5**: In this section, continue preparing our dataset for analysis based on the previously completed tasks:
  - **Data Splitting**: Segment the data using the `scikit-learn` library with the reproducible seed "1234," utilizing 80% for the training set and 20% for the testing set. Indicate the size of both sets.

### Exploratory Data Analysis
- **Exercise 6**: Deeply explore the data to gain insights that guide the model construction:
  - **Variable Distribution**: For the variable "age," apply quantile grouping using deciles. For each group, manually calculate the associated WoE. Calculate the IV of the discretized variable with respect to the target. Do you think this is an important variable regarding its relationship with the target variable (smoking)?
  - **Relationships between Variables**: Perform the same exercise for the variable "Height." Based on the results obtained, which variable do you think has a stronger predictive power?

### Feature Selection
- **Exercise 7**: Evaluate and select the most informative features for the model:
  - **Determination of Relevant Features**: Using the `.corr()` attribute of the DataFrame in pandas format, list the three variables that correlate the most with the target variable. What logical interpretation can you give to the obtained correlation regarding these variables?

### Model Construction
- **Exercise 8**: Choose and apply the appropriate classification model.
  - **Training**: Train the selected model using the training set with either the kNN or SVM algorithm. Justify your answer.

### Model Evaluation
- **Exercise 9**: Evaluating the model's performance is crucial to understanding its effectiveness. This includes:
  - **Metric Comparison**: Observe and analyze performance metrics discussed in class, such as accuracy, precision, recall, F1-score, AUC-ROC, and confusion matrix. What conclusions can be drawn from each of these metrics?
  - **Cross-Validation**: Use cross-validation to optimize hyperparameters and confirm the stability of the model. What is the best parameter configuration?

### Interpretation of Results and Conclusions
- **Exercise 10**: Analyze the influence of each feature and propose improvements for the model.
  - Based on the analysis of the model, which feature do you think is the most important? Justify your answer.
  - How do you think you could improve the model in future iterations?
