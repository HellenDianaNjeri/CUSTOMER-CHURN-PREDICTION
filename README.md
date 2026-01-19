# Customer Churn Prediction

This project predicts which customers are likely to churn (leave) using machine learning models. 
The goal is to help the company take proactive measures to retain high-risk customers and reduce revenue loss.

## Project Overview

- **Objective:** Identify customers at high risk of churn to enable targeted retention strategies.
- **Dataset:** Customer data including demographics, behavior, transactions, and engagement metrics.
- **Target Variable:** `Churn` (1 = churned, 0 = retained)

## Workflow

1. **Data Exploration & Cleaning**
   - Explored data distributions, missing values, and relationships between features.
   - Handled missing data and outliers.

2. **Feature Engineering & Preprocessing**
   - Created new features to capture customer behavior.
   - Applied imputation, encoding, and scaling for machine learning readiness.

3. **Baseline Model**
   - Logistic Regression to establish a performance baseline.
   - Metrics: recall, precision, F1-score, ROC-AUC.

4. **Advanced Models**
   - **Decision Tree:** Captures non-linear relationships. Recall improved to 0.73.
   - **Random Forest:** Ensemble model with highest recall (0.83) for churners.
   - **XGBoost:** Gradient boosting model balancing recall (0.73) and precision (0.52) for optimal F1-score.

5. **Model Evaluation**
   - Metrics reported: confusion matrix, recall, precision, F1-score, ROC-AUC.
   - Model comparison table used to recommend deployment strategy.

6. **Business Recommendations**
   - Use Random Forest if the goal is to maximize recall and identify most at-risk customers.
   - Use XGBoost if a balance between recall and precision is desired.
   - Implement targeted retention campaigns, personalized offers, and proactive support for flagged customers.

## Key Findings

- Advanced tree-based models significantly improved recall compared to Logistic Regression.
- Trade-offs exist: higher recall often leads to lower precision (more false positives).
- Proper model selection depends on the business priority: catching most churners vs minimizing false positives.

## Technologies Used

- Python
- Pandas, NumPy
- Scikit-learn
- XGBoost
- Matplotlib & Seaborn for visualization

## How to Run

1. Clone the repository:  
```bash
git clone <https://github.com/HellenDianaNjeri/CUSTOMER-CHURN-PREDICTION.git>
```
2. Install dependencies:
```
pip install -r requirements.txt
```
3. Run the Jupyter Notebook ```customer_churn.ipynb``` to reproduce preprocessing, modeling, and evaluation.

License

This project is licensed under the MIT License.