Drug-Likeness Prediction (pChEMBL Value Estimation)
Overview
This project implements a machine learning model to predict the pChEMBL values of compounds based on their SMILES representation. The dataset consists of bioactivity data for acetylcholinesterase inhibitors. The project involves data preprocessing, molecular descriptor calculation, and model training to estimate drug-likeness.
Features
•	SMILES-based Prediction: Uses molecular descriptors derived from SMILES strings.
•	Machine Learning Model: Random Forest Regressor with train-test splitting.
•	Performance Metrics: 
o	Train R²: ~86%
o	Test R²: ~61%
o	Slight overfitting, but Random Forest performed better than other models.
•	Hyperparameter Tuning: Attempts to improve model performance resulted in degradation.
Workflow
1.	Data Preprocessing
o	Load the dataset (acetylcholinesterase_01_bioactivity_data_processed.csv).
o	Extract molecular features (descriptors) from SMILES representations.
2.	Feature Engineering
o	Convert SMILES into numerical descriptors.
o	Prepare data for machine learning models.
3.	Model Training
o	Train-test split.
o	Train a Random Forest Regressor to predict pChEMBL values.
o	Evaluate model performance.
4.	Results & Interpretation
o	Random Forest Regressor provided the best fit.
o	No significant improvement from hyperparameter tuning.

How to Use
1.	Install dependencies: 
pip install numpy pandas scikit-learn rdkit
2.	Run the notebook and load the dataset.
3.	Input a SMILES string to get a predicted pChEMBL value.
Future Improvements
•	Use advanced models like XGBoost or deep learning.
•	Optimize feature selection to reduce overfitting.
•	Expand dataset for better generalization.
Source of data: DATA PROFESSOR (YouTube/Git)
