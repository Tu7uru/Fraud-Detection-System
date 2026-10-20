# Fraud Detection System

Course project for HY-484, Computer Science Department, University of Crete (January 2022).

Compares supervised and unsupervised machine-learning models for detecting fraudulent transactions, and measures how much **graph features** improve them: transactions are modeled as a graph (accounts as nodes, transactions as edges) with NetworkX, and each node's PageRank, closeness centrality and eigenvector centrality are added as features.

## Methods compared

- **Supervised:** Logistic Regression, Random Forest, AdaBoost — evaluated with confusion matrices, ROC curves and AUC.
- **Unsupervised:** Isolation Forest and K-Means, each with and without PCA.

## Headline results (full analysis in the report)

- Random Forest was the most accurate supervised model; AdaBoost came close at roughly a third of the training time.
- Adding the graph features raised AdaBoost's true positives by 200+.
- Unsupervised methods were weaker: Isolation Forest performed best, while K-Means failed to separate fraud.

## Datasets (not included in the repo)

- [PaySim — Synthetic Financial Datasets For Fraud Detection](https://www.kaggle.com/datasets/ealaxi/paysim1)
- [ULB Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) (284,807 transactions, 492 frauds)

Download them from Kaggle and place them under the paths used in the notebooks.

## Repository layout

- `src/Fraud-Detection-System.ipynb` — the full analysis notebook
- `src/Template-Fraud-Detection.ipynb` — a reusable skeleton of the same pipeline
- `doc/Fraud_Detection_Report.pdf` — the written report (all figures and numbers)
- `doc/Fraud_Detection_Presentation.pdf` — the presentation

## Stack

Python, pandas, NumPy, NetworkX, scikit-learn, matplotlib, seaborn, plotly, Jupyter.

## Authors

Haralambos Varsamis, Apostolos Mavrogiannakis
