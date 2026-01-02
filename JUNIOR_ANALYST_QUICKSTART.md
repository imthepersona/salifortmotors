Salifort Motors Employee Attrition Project 🎯
Predicts employee churn using HR data. XGBoost model trained on 15K employees.

🚀 Quick Start (5 minutes)
Open VSCode → salifort motors attrition project/

Open notebook → notebooks/salifort_analysis.ipynb

Kernel → Salifort Motors (auto-selects)

Run all cells → Ctrl+F9

✅ Notebook runs end-to-end. Model loads automatically.

📁 Folder Structure
text
├── data/raw/              # Raw HR data (salifort_hrdata_raw.csv)
├── notebooks/             # Analysis (your Jupyter notebooks)
├── models/                # Trained XGBoost model (*.pkl)
├── reports/figures/       # Charts, Tableau exports, Executive Summary & PACE Strategy Document
└── src/                   # Reusable Python code
🔮 Predict Attrition for New Employees
New CSV? Run this complete code in any notebook:

python
import pandas as pd
import joblib

# Load trained model (save it first: joblib.dump(model, "../models/salifort_xgb_model.pkl"))
model = joblib.load("../models/salifort_xgb_model.pkl")

# Load new employees
new_df = pd.read_csv("../data/raw/new_employees.csv")

# EXACT SAME preprocessing as training:
categorical_cols = ['department', 'salary', 'hours_bin', 'tenure_bin']
new_df_encoded = pd.get_dummies(new_df, columns=categorical_cols, drop_first=True)

# Drop same columns as training:
X_new = new_df_encoded.drop(['left_company', 'total_projects', 'monthly_avg_hours'], 
                           axis=1, errors='ignore')

# Match training columns exactly:
X_new = X_new.reindex(columns=X_train.columns, fill_value=0)  # X_train.columns from notebook

# Predict churn risk (0-1):
new_df['churn_risk'] = model.predict_proba(X_new)[:,1]
new_df.to_csv("../reports/new_predictions.csv")
print("✅ Predictions saved! High churn_risk = at risk of leaving.")
Higher churn_risk = more likely to quit! Ready for HR dashboard.

🛠️ Troubleshooting
Problem	Fix
ModuleNotFoundError: pandas	Kernel → Salifort Motors
FileNotFoundError: salifort_xgb_model.pkl	Run notebook to train/save model first
KeyError: column	Check X_new.reindex(columns=X_train.columns) matches notebook
Kernel stuck	Kernel → Restart Kernel
📊 What the Model Does
Input: Employee features (age, salary, department, tenure, etc.)

Output: Churn probability (0-1)

Performance: ROC-AUC [FILL IN YOUR SCORE]

Trained: XGBoost with class imbalance handling (scale_pos_weight)

👥 For Junior Analysts
Read notebooks/salifort_analysis.ipynb - full pipeline

Save model: joblib.dump(model, "../models/salifort_xgb_model.pkl")

Predict new data: Copy prediction code above

Ask: Post Slack question with notebook screenshot

⚙️ Environment
text
(.venv) pip install -r requirements.txt  # If we add one later
Kernel: "Salifort Motors" (Python 3.11 + xgboost)
Model ready for HR dashboard! Questions? @willescalanteAGE

​