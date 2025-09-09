# Machine_Learning

This repository is a concise, hands-on recap of popular Machine Learning algorithms across three paradigms: Supervised, Unsupervised, and Reinforcement Learning. It focuses on practical intuition, minimal theory, and runnable demos.

## Scope
- Supervised: Linear Regression, Logistic Regression, Support Vector Machine (SVM), Decision Tree, Random Forest, K-Nearest Neighbours (KNN), Naive Bayes
- Unsupervised: K-Means (and extensions later)
- Reinforcement: Basic introduction and simple demo (planned)

## For each algorithm, we aim to cover
- Brief theory: core idea and objective function
- Suitable data/types: regression vs classification, numeric vs categorical, assumptions
- Math essentials: key formulas and constraints (high-level)
- Pros/Cons: when to use and when to avoid
- Fine-tuning: important hyperparameters and how to select them
- Data requirements: preprocessing/encoding/scaling needed
- Demo: an example of a small set of data to practice and verify understanding, performed on Jupyter Notebook (file .ipynb) to easily learn and understand each cell of algorithm

## Evaluation and Optimization
- Metrics: MSE/RMSE/MAE, R², Accuracy, Precision/Recall/F1, ROC-AUC, Confusion Matrix, Silhouette (unsupervised), etc.
- Model selection: train/validation/test split, cross-validation
- Optimization: Gradient Descent/SGD, Momentum, Adam, regularization (L1/L2), early stopping, feature engineering/selection

## Structure
- `Supervised_Learning/`
  - `Linear_Regression.ipynb` — regression with preprocessing, correlation analysis, manual closed-form, SGD, sklearn pipeline, model saving
  - `Logistic_Regression.ipynb` — classification (planned/expanding)
  - `README.md` — brief notes per-algorithm
- `datasets/` — sample datasets (e.g., Housing)
- `Optimizer.ipynb` — optimization techniques overview (work in progress)

## Getting Started
- Open notebooks in `Supervised_Learning/` to explore each algorithm.
- Run cells top-to-bottom; each notebook is self-contained with preprocessing and evaluation.
- Extend demos with your own datasets by following the preprocessing guidance per algorithm.

## Streamlit Apps (Interactive UI)
- Plan to add simple Streamlit apps for each algorithm to demo interactive prediction and visualization.
- Each app will load a trained model (or pipeline), expose inputs via sidebar widgets, and render predictions/plots.
- Expected location: `apps/<algorithm>/app.py`. Example run: `streamlit run apps/linear_regression/app.py`.

## References
- ML From Scratch (NumPy implementations): https://github.com/eriklindernoren/ML-From-Scratch/tree/master
- Stanford CS229 (bản tiếng Việt, tổng hợp ghi chú): https://github.com/afshinea/stanford-cs-229-machine-learning/tree/master/vi
- Machine Learning cơ bản — Vũ Hữu Tiệp (tài liệu/ghi chú tổng quan)

