# Credit Card Fraud Detection

**Repository**

⸻

📋 **Overview**

Even though fraudulent transactions represent well under 1 % of all charges, they can cost banks and customers millions each year. In this project, we use the publicly available Kaggle dataset (284 ,807 European card transactions, 492 frauds; 0.172 % positive class) to:
	1.	Preprocess & explore the data
	2.	Train & compare four classifiers (Logistic Regression, Random Forest, XGBoost, SVM) on the imbalanced data
	3.	Handle imbalance using:
	•	SMOTE + Tomek Links (resampling pipeline)
	•	Class weighting in Random Forest
	4.	Evaluate all models via precision, recall, F1-score, confusion matrices, ROC-AUC & PR curves

t-SNE visualizations reveal how oversampling spreads minority points—and why class weights sometimes give a better production-ready trade-off.

⸻

🚀 **Quickstart**
	1.	Clone the repo

git clone https://github.com/shaaidaar/creditcard-fraud-detection.git
cd creditcard-fraud-detection


	2.	Install dependencies

pip install -r requirements.txt


	3.	Download the data
    download from Kaggle: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud
    
	4.	Run the notebook

jupyter notebook Fraud_Detection.ipynb

	•	Follow the sections:
	1.	Data loading & EDA
	2.	Preprocessing & scaling
	3.	Baseline model training
	4.	Imbalance handling (SMOTE+Tomek, class weights)
	5.	t-SNE plots
	6.	Final evaluation & comparison

⸻

**🔍 Results Summary
**
Model	                        ROC-AUC	Recall	Precision	F1-score
Random Forest (baseline)	    0.924	  0.77	    0.96	  0.85
Random Forest (class_weight)	0.9376	0.70	    0.97	  0.82
Random Forest (SMOTE + Tomek)	0.9732	0.84	    0.54  	0.66

**Takeaway:
**For this highly skewed fraud dataset, class-weighted Random Forest strikes the best production-ready balance—boosting recall with minimal loss in precision, without risk of overfitting that complex resampling can introduce.

⸻

📚 **References**
	•	Scikit-learn.org. (2018). Compare the effect of different scalers on data with outliers.
	•	Brownlee, J. (2020). Tour of Evaluation Metrics for Imbalanced Classification.
	•	Hajibabaee, P., Pourkamali-Anaraki, F. & Hariri-Ardebili, M.A. (2021). An Empirical Evaluation of the t-SNE Algorithm for Data Visualization in Structural Engineering.
	•	Raden, Towards Data Science (2021). Imbalanced Classification in Python: SMOTE-Tomek Links.

