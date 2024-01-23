# Credit_card_fraud_detection-Kaggle_competition-
The dataset for this competition (both train and test) was generated from a deep learning model trained on the Credit Card Fraud Detection. Feature distributions are close to, but not exactly the same, as the original.

- All features are numerical
- V1 - V28 are PCA obtained components, only 'time' and 'amount' have not been transformed with PCA
- 'time' indicates seconds elapsed between transaction and first transaction
- 'amount' is the transaction amount
- 'class'  - 1 is fraud

Submissions are evaluated on area under the ROC curve between the predicted probability and the observed target.

Project summary:
1. Train and test data analyzed. EDA done for train data. Train set is imbalanced data.
2. All features have outliers, except 'Time' feature.
3. Correlation between features are low and acceptable.
4. All features have been scaled using StandardScaler()
5. Quick models have been developed using Randomforest and Logistic Regression without processing data. Hence, model predcitions had low ROC-AUC scores
6. Then train data have been treated via removing outliers using z-score removal method. Before z-score removal class 1 features have been removed from dataset, due to low quantity and not lose them.
8. Then as data had imbalance, SMOTE techniqe has been used to balance classes
9. Logistic Regression, Random Forest , LightGBM and Voting Classifier based on previous three classifiers have been used and their ROC-AUC scores compared. Best result LightGBM provided and final model have been developed on it.
