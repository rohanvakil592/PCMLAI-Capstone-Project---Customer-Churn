# PCMLAI-Capstone-Project---Customer-Churn

This project helps banks predict which customers are likely to close their accounts ("churn") using their transaction history, demographics, and account details. The model identifies at-risk customers with 87% accuracy, enabling banks to offer targeted retention incentives (e.g., discounts or personalized offers). While it flags churn risks effectively, it misses 51% of true churn cases—highlighting room for improvement. This tool is designed for customer retention teams, not for high-stakes decisions like loan approvals.

DATA
•	Dataset: https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction?resource=download
•	Samples: 10,000 synthetic bank customers.
•	Features: Credit score, age, account balance, geography (France/Germany/Spain), gender, and more.
•	Target: Binary flag (1 if churned, 0 if retained).
•	Limitations: Synthetic data, overrepresents French customers (50%) and males (55%).

MODEL
•	Algorithm: Random Forest Classifier.
•	Why Chosen:
o	Handles imbalanced data (20% churn rate).
o	Interpretable (feature importance scores show key drivers like Age and Balance).
o	Robust to outliers.

HYPERPARAMETER OPTIMISATION
•	Parameters Tuned:
o	n_estimators: 100 trees (trade-off between speed and accuracy).
o	max_depth: 10 (prevents overfitting).
o	class_weight: "balanced" (adjusts for churn class imbalance).
•	Optimisation Method:
o	GridSearchCV tested n_estimators=[50, 100, 200] and max_depth=[5, 10, 15].
o	Chose parameters with highest recall for churn class.

RESULTS
Metric	Retained (0)	Churned (1)	Overall
Precision	0.89	0.77	0.86
Recall	0.96	0.49	0.87
F1-Score	0.92	0.60	0.86
Key Takeaways:
1.	Strengths:
o	96% accurate in identifying retained customers.
o	77% precision for churn predictions (moderate false alarms).
2.	Weaknesses:
o	Misses 51% of true churners (low recall).

Key Takeaways:
1.	Strengths:
o	96% accurate in identifying retained customers.
o	77% precision for churn predictions (moderate false alarms).
2.	Weaknesses:
o	Misses 51% of true churners (low recall).
![image](https://github.com/user-attachments/assets/e24dbe00-205f-4751-be09-2302570fa50f)

