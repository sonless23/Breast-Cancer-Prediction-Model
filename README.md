# Breast Cancer Malignancy Prediction Using Machine Learning
This project uses machine learning techniques to predict whether a breast tumor is malignant or benign based on diagnostic features. It highlights how supervised learning can assist in clinical decision-making by providing fast, data-driven predictions based on patient metrics.
________________________________________
# Introduction
Breast cancer is one of the most common cancers affecting women globally. Timely and accurate diagnosis is critical to improving treatment outcomes. This project leverages machine learning models to classify tumors as malignant or benign using structured input data from digitized breast mass features.
The primary objective is to build and evaluate classification models for integration into decision support systems.
________________________________________
# Dataset
The dataset used is the publicly available Breast Cancer Wisconsin Diagnostic Dataset, available through sklearn.datasets. It contains 30 numeric features computed from digitized images of fine needle aspirate (FNA) of breast masses. The target variable is binary:

•	0 = Benign

•	1 = Malignant
________________________________________
# Methodology
## Data Preprocessing
•	I loaded and structured the dataset into a data frame.

•	Standardized the features using StandardScaler().

•	Split into train/test sets.

•	No missing values were present.
## Exploratory Data Analysis (EDA)
•	I used seaborn to visualize class distribution, the data was moderately imbalanced.

•	I compared mean feature distributions between benign and malignant classes using boxplots and histograms.
## Model Selection and Testing
I tested multiple models using a param grid:

•	Logistic Regression

•	Support Vector Classifier (SVC)

•	Decision Tree

•	Random Forest

Cross-validation was applied and hyperparameters were tuned using GridSearchCV().
## Model Evaluation
•	I evaluated the final model using classification report metrics: precision, recall, f1-score.

•	Best model was selected using recall and not accuracay for the malignant class — since false negatives in cancer diagnosis carry the highest clinical risk.
________________________________________
# Results
The best-performing model achieved:

•	High recall for malignant class

•	Balanced precision and f1-score

•	Robustness on unseen test data

Logistic Regression performed the best based on recall.
________________________________________
# How to Use
1.	Clone the repository or download the notebook.
	
2.	Open the notebook (breast cancer malignancy model.ipynb) in Jupyter or Google Colab.
	
3.	Ensure necessary libraries are installed: scikit-learn, pandas, seaborn, matplotlib.
	
4.	Run all cells in order.
	
5.	You can tune the hyperparameters yourself or test other models.
________________________________________
# Background Considerations
In medical diagnosis, recall (sensitivity) is typically more critical than overall accuracy. A model that misses malignant cases (false negatives) poses a much greater risk than one that incorrectly flags benign ones (false positives). Hence, this project places special emphasis on maximizing recall for malignant cases.
________________________________________
# Disclaimer
This project is for educational and research purposes only. It is not intended for clinical use or diagnosis. Always consult licensed medical professionals for diagnosis and treatment.
________________________________________
# Contact
Reach out to me at chibuikemofobuike@gmail.com for feedback, collaboration, or questions.
________________________________________


