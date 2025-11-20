
# Performed EDA and created a Machine Learning Model with anonymized data provided by "Salifort Motors" (Advanced Google Data Analytics Capstone Project)

# Project Overview
Salifort Motors company needed help understanding their high employee attrition. Their HR department provided AGE Analytics anonymized employee data to conduct basic and extensive exploratory data analysis for immediate feedback. 
Additionally, an XGboost Classication model was created to predict employee attrition. Our final model achieved an ROC-AUC of 0.976 which significantly helps Salifort Motors identify employees that are at high risk of leaving the company.

# Data Understanding 

50% of U.S. employees leave or change jobs annually, contributing to persistent, high workforce churn. Each month, more than 4 million employees voluntarily quit their positions, representing about 2% of the national workforce at any given time.
Turnover is predominantly driven by voluntary departures, which now account for approximately 70% of all employee separations.
Businesses typically incur costs ranging from one-half to twice an employee’s annual salary to recruit, hire, and train replacements.
Understanding, predicting, and reducing employee attrition has become a critical priority for HR departments and business leaders seeking to retain talent and control operational costs.

# Modeling and Evaluation 

To address the significant class imbalance (~83% stayers vs. ~17% leavers), a scale_pos_weight parameter reflecting the ratio of the majority to minority class was applied during model training, enabling the model to better
focus on the minority class without bias.

Evaluation metrics focused on both threshold-dependent and threshold-independent measures. The model achieved an overall accuracy of 98% with strong precision (0.94) and recall (0.88) for the attrition class, 
indicating effective identification of employees likely to leave. The ROC AUC score of approximately 0.976 demonstrates excellent discriminative ability across classification thresholds. 
The confusion matrix showed minimal false positives and false negatives, underscoring the model's reliability.

These results affirm XGBoost's superiority over logistic regression for this task due to its capacity to model complex, non-linear relationships and interactions between features. 
The evaluation strategy prioritized ROC AUC as a comprehensive, threshold-independent metric critical for imbalanced classification problems, ensuring robust performance assessment.

# Conclusion
Salifort Motors should focus on employee retention for those with lower satisfaction scores, overworked individuals and those with low salaries and have not had a promotion.
Have respective department deploy model into the daily workflow to flag at-risk employees for personalized outreach or to help establish systems or programs to address issue. 
Take a pro-active approach to leveraging real-time insights year-round 

