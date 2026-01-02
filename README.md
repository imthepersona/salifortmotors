# Salifort Motors Employee Attrition 🎯

**XGBoost model predicts employee churn.** **ROC-AUC: 0.98** (production-ready excellence).

## 🎯 Results
| Metric | Score |
|--------|-------|
| **Accuracy** | **98%** |
| **ROC-AUC** | **0.98** |
| **Churn Recall** | **93%** |
| **Stay Precision** | **99%** |

![Confusion Matrix](reports/figures/confusion_matrix.png)
![Top Churn Drivers](reports/figures/tableau_churn_visual.png)
![ROC Curve](reports/figures/roc_auc.png)

## 🚀 Quick Start
1. `pip install -r requirements.txt`
2. `jupyter lab notebooks/salifort_analysis.ipynb`
3. Run all → Model ready!

**Predict new hires:** `JUNIOR_ANALYST_QUICKSTART.md`

## 📁 Structure
├── data/raw/ # HR datasets
├── notebooks/ # Analysis pipeline
├── models/ # XGBoost .pkl
├── reports/ # 📊 Executive PDF + Tableau visuals!
└── requirements.txt

text

## Business Impact
- Identifies **93% of leavers** before they quit
- **Target top 20% risk** → Maximize retention ROI

**Fork → Run → Deploy to HR!** [web:233]