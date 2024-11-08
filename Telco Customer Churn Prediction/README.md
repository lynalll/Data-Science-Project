# Customer Churn Prediction Model

## Overview
This project is a machine learning model designed to predict customer churn for a telecommunications company. Customer churn refers to when a customer stops using a company's services. The model uses customer data to predict the likelihood that a customer will "churn" (leave the company), which can help the business take proactive steps to retain customers.

## Objective
The goal is to create an efficient and accurate churn prediction model that can:

- Identify high-risk customers who are likely to churn.
- Support business decisions by highlighting patterns and trends that lead to churn.
- Help retain customers through targeted marketing or retention strategies based on predicted churn probabilities.

## Dataset
The model was trained on the **WA_Fn-UseC_-Telco-Customer-Churn** dataset. The dataset includes various customer attributes like demographics, account details, service usage, and whether they have churned.

### Key Features in the Dataset:
- **Customer Demographics**: Includes gender, age, and whether they have dependents.
- **Account Information**: Includes contract type, tenure with the company, and billing methods.
- **Service Usage**: Details on services subscribed, like internet, phone, and streaming options.

## Model Details

- **Model Type**: Gradient Boosting Classifier
- **Parameters**:
  - `n_estimators=100`
  - `max_depth=5`
- **Performance**: 
  - **Accuracy**: 87%
  - **Precision and Recall**: Balanced across both churn and non-churn classes.
  - **Handling Class Imbalance**: SMOTE (Synthetic Minority Over-sampling Technique) was used to balance the classes, which helped improve recall and precision for minority (churn) class predictions.

## Results
The model provides the following insights:

- **Churn Prediction Accuracy**: The model achieved 87% accuracy, effectively distinguishing between churn and non-churn cases.
- **Balanced Precision and Recall**: Precision and recall scores for both churners and non-churners are roughly equal, indicating reliable performance across classes.
- **F1-Score**: An F1-score of 0.87 reflects balanced precision and recall, providing a solid trade-off between capturing as many true churn cases as possible while minimizing false positives.

## Use Cases

1. **Customer Retention**: Identify customers likely to churn and create targeted retention campaigns, such as personalized offers or loyalty programs.
2. **Proactive Support**: Use churn predictions to reach out to at-risk customers and address potential issues before they leave.
3. **Resource Allocation**: Focus marketing resources on customers with a high likelihood of churn, maximizing ROI on retention efforts.
4. **Business Insights**: Gain insights into what factors contribute most to churn, enabling data-driven decisions.

## How to Run the Model

### Prerequisites:
- Python 3.x
- Libraries: `pandas`, `scikit-learn`, `imblearn`

### Steps:
1. Clone the repository and load the dataset.
2. Run the preprocessing steps, including SMOTE for class balancing.
3. Split the data, train the model, and evaluate the results.
4. Check the output metrics (accuracy, classification report).

### Future Work:
- **Hyperparameter Tuning**: Further optimization of parameters.
- **Feature Engineering**: Adding additional features that might improve model accuracy.
- **Other Models**: Testing alternative models like XGBoost or LightGBM for comparison.

## Contributing
If you have ideas for improving this project, feel free to create a pull request or open an issue!
