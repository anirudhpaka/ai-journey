# 🟢 Phase 2. Machine Learning Fundamentals

**Weeks 5–8 · ~32–36 hours · Month 2**

> Full context and week-by-week table in the [main README](../README.md#-phase-2--machine-learning-fundamentals).

## What lives in this folder

```
phase-2-ml/
├── week-5-regression/         # Linear + logistic regression in scikit-learn
├── week-6-trees-forests/      # Titanic Kaggle submission
├── week-7-evaluation/         # Titanic improved with CV + feature engineering
├── week-8-clustering/         # k-means + PCA notebooks
└── milestone-e2e-ml/          # 🎯 End-to-End ML Project
```

## Milestone project. End-to-End ML Project

Pick a domain you actually care about (real estate, stocks, sports, health, anything with a public dataset). Deliver:

1. **Cleaned data** with a data-quality section documenting what you dropped and why
2. **Two+ models compared** side-by-side on the same test set
3. **Honest cross-validated evaluation**: no train-set leakage, correct metric for the task
4. **README that explains every choice**: feature engineering, model, metric, and what the numbers actually mean

**Post the story on LinkedIn.** Recruiters read LinkedIn far more than they read GitHub. The post is the funnel; GitHub is the proof.

## Checkpoint before Phase 3

- [ ] I can explain overfitting and two ways to fight it
- [ ] I can choose precision vs recall for a business case and justify it
- [ ] I can train, tune, and compare two models in scikit-learn without a tutorial
- [ ] I scored in the top half of the Titanic leaderboard

## Common traps

- **Data leakage**: never fit anything (scaler, encoder, imputer) on the full dataset before splitting. Use `Pipeline`.
- **Wrong metric**: accuracy is misleading on imbalanced data. Learn F1, ROC-AUC, and log-loss.
- **Fancy model, no baseline**: always benchmark against a dumb baseline (mean predictor, logistic regression). If your XGBoost is only 1% better, that's the story.
