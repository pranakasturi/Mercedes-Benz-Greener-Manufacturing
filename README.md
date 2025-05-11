# Mercedes-Benz Greener Manufacturing: Optimizing Test Bench Time with Machine Learning

## Description

Mercedes-Benz, a leader in the premium automotive industry, offers a vast array of features and options, allowing customers to create their bespoke vehicles. To guarantee the safety and reliability of each unique configuration before it reaches the customer, Mercedes-Benz employs a rigorous testing system. As one of the world's largest premium car manufacturers, the company prioritizes both safety and efficiency throughout its production lines. However, optimizing the speed of this testing system across numerous potential feature combinations presents a complex and time-intensive challenge without a powerful algorithmic approach.

This repository contains a Machine Learning model developed to predict and ultimately reduce the time vehicles spend on the test bench. By accurately forecasting testing duration based on car configurations, this model contributes to a more efficient manufacturing process and a reduced environmental footprint.

## Model Building Process

The development of this predictive model involved the following key steps:

1.  **Library Import:** Essential Python libraries were imported for data manipulation, visualization, and machine learning tasks. These included:
    * NumPy for numerical operations.
    * Pandas for data manipulation and analysis.
    * Matplotlib for basic plotting.
    * Scikit-learn (sklearn) for various machine learning algorithms and tools.
    * Seaborn for enhanced statistical data visualization.

2.  **Data Loading:** The provided dataset containing car features and the target variable (testing time) was loaded into the Python environment using Pandas.

3.  **Initial Data Analysis:** An initial exploration of the dataset was conducted. This involved:
    * Identifying and dropping the irrelevant 'ID' column, which serves as a unique identifier and does not contribute to the predictive power of the model.
    * Separating the target variable (the time spent on the test bench) from the feature set.

4.  **Label Encoding:** Several categorical features within the dataset were transformed into numerical representations using Label Encoding. This step is crucial for making these features compatible with most machine learning algorithms.

5.  **Variance Analysis:** A variance test was performed on the features to identify columns with zero variance. Features with zero variance provide no discriminatory information and were subsequently dropped from the dataset to streamline the modeling process. This resulted in the removal of 12 such variables.

6.  **Data Cleaning:** Further data cleaning steps were undertaken, including:
    * Checking for and handling any null (missing) values within the dataset.
    * Examining the number of unique values in each feature to identify potential issues or patterns.

7.  **Dimensionality Reduction using PCA:** To address the high dimensionality of the feature space and potentially improve model performance and reduce computational cost, Principal Component Analysis (PCA) was applied. PCA transforms the data into a new set of uncorrelated variables (principal components) that capture most of the variance in the original data, allowing for a reduction in the number of features while retaining crucial information.

8.  **Model Training with XGBoost:** The XGBoost (Extreme Gradient Boosting) algorithm was chosen for its robust performance in regression tasks and its ability to handle complex datasets. The model was trained on the processed training data to learn the relationship between the car features (after dimensionality reduction) and the testing time.

9.  **Model Evaluation (Training Data):** The performance of the trained XGBoost model was evaluated on the training data by computing the Root Mean Square Error (RMSE). RMSE is a common metric for regression tasks, measuring the average magnitude of the errors between predicted and actual values. A lower RMSE indicates better model accuracy.

10. **Visualization of Predictions (Training Data):** A distplot (distribution plot) was generated using Seaborn to visually compare the distribution of the actual target values (testing time) with the distribution of the values predicted by the model on the training data. This visualization helps in understanding how well the model's predictions align with the real values.

11. **Evaluation on Test Data:** Finally, the trained XGBoost model was used to predict testing times on a separate test dataset (provided for the competition). The RMSE was calculated on these predictions to assess the model's generalization ability on unseen data.

12. **Visualization of Predictions (Test Data):** Similar to the training data, a distplot was created to compare the distribution of the predicted testing times with the distribution of the actual (if available or for analysis purposes) testing times in the test dataset. This provides insights into the model's performance and potential biases on unseen data.

This repository serves as a demonstration of a machine learning approach to optimize manufacturing processes, contributing to both efficiency and environmental sustainability within the automotive industry.
