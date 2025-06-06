# -Chicago-Car-Crash-Injury-Prediction
This project applies classification modeling to predict whether a car crash in Chicago results in an injury/fatality or no injury, based on crash attributes such as weather, lighting, crash time, and road conditions.

Project Objectives
Predict Injury Outcomes: Build a machine learning model to classify whether a crash results in injury/fatality or not.

Identify Risk Factors: Understand the most influential features contributing to crash severity.

Support Safety Policy: Provide actionable insights to help traffic safety officials in Chicago prioritize interventions.

Target Stakeholder
Chicago Department of Transportation (CDOT): Insights and predictions from this model can help CDOT target high-risk scenarios and optimize resource allocation for traffic safety.

 Dataset
Source: City of Chicago Open Data Portal

Original Size: Over 1.5M rows

Final Dataset: Cleaned and filtered to relevant numeric and categorical predictors

Target Variable: INJURY_OR_FATAL

1: Injury or Fatality

0: No Injury

Features Used
Crash hour, day, and month

Posted speed limit

Weather and lighting conditions

First crash type

Traffic control device presence

Road surface condition

Number of vehicles involved

Data Preparation
One-hot encoding of categorical features

Stratified train-test split

Handled class imbalance using evaluation metrics (recall, precision, F1)

Models Built
1. Baseline Model – Logistic Regression
Simple and interpretable

Identified baseline metrics for comparison

2. Decision Tree
Tuned with max_depth, min_samples_split, and min_samples_leaf using RandomizedSearchCV

Model Performance Summary
Model	Precision (Injury)	Recall (Injury)	F1 Score (Injury)	Accuracy
Logistic Regression	0.77	0.24	0.36	88%
Decision Tree	0.80	0.22	0.34	88%
Tuned Decision Tree	↑ (Pending insertion)	↑	↑	↑

While the models show high overall accuracy, recall for the injury class is relatively low due to class imbalance.

Key Insights
Night-time crashes and wet road surfaces increase injury likelihood.

Speed limits and crash types are strong predictors.

Interventions can be targeted around weather, lighting, and traffic control conditions.

Repository Contents
Phase3_Chicago_Crash_Prediction.ipynb: Main notebook with EDA, modeling, and evaluation.

Chicago_Crash_Model_Presentation.pptx: Summary PowerPoint slides.

README.md: Project overview (this file).

Future Work
Improve class imbalance handling using SMOTE or class weighting.

Try ensemble models like XGBoost.

Build an interactive dashboard for stakeholder insights.

Acknowledgements
City of Chicago for the crash dataset.

Flatiron School Phase 3 curriculum for model guidance and structure.

