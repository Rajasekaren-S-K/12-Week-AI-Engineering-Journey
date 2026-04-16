🩺 Week 4 — Machine Learning: Classification
Hope AI Master Program · Applied AI, Gen AI & Data Science

Can a machine learning model detect Chronic Kidney Disease from a routine blood test? This week's assignment answers exactly that — by building, training, and benchmarking 5 classification models on real clinical laboratory data.

## 🎯 Problem Statement

Chronic Kidney Disease (CKD) silently affects millions worldwide, often going undetected until irreversible damage has occurred. The goal of this assignment is to build a binary classification model that accurately predicts whether a patient has CKD — using 24 clinical and diagnostic features — enabling earlier, data-driven screening that could save lives.

## 📂 Assignment

| Item | Detail |
|---|---|
| 📓 Notebook | Classification_Assignment.ipynb |
| 📊 Dataset | CKD.csv |
| 🎯 Target Variable | `classification` (1 = CKD present / 0 = Not CKD) |
| 🔢 Features Used | age, bp, sg, al, su, rbc, pc, pcc, ba, bgr, bu, sc, sod, pot, hrmo, pcv, wc, rc, htn, dm, cad, appet, pe, ane |
| ✂️ Train / Test Split | 67% / 33% |
| 📐 Evaluation Metrics | Accuracy, Precision, Recall, F1-Score, Confusion Matrix |

## 🔬 ML Pipeline

```
Raw Data (399 samples · 25 columns)
│
├── 1. Exploratory Data Analysis (EDA)
│   └── Shape, dtypes, null check, duplicate check, unique value distribution
│
├── 2. Feature Engineering
│   ├── Binary encoding: normal/abnormal → 1/0  (rbc, pc, pcc, ba, htn, dm, cad, pe, ane)
│   ├── Label encoding: appet (poor=0, yes=1) · classification (no=0, yes=1)
│   └── One-Hot Encoding: sg (5 levels → sg_b, sg_c, sg_d, sg_e) — drop_first=True
│
├── 3. Feature Scaling
│   └── StandardScaler — fit on train only, transform on test
│
├── 4. Train / Test Split
│   └── 67% train · 33% test · random_state=0
│
└── 5. Model Training & Evaluation
    └── 5 models trained → Confusion Matrix + Classification Report → Best model selected
```

## 🤖 Models Benchmarked

| # | Model | Category | Key Strength | Accuracy |
|---|---|---|---|---|
| 1 | Logistic Regression | Linear | Fast, interpretable, strong baseline | **99%** |
| 2 | SVM (Sigmoid Kernel) | Kernel-based | Effective in high-dimensional space | **99%** |
| 3 | Random Forest (100 trees) | Ensemble (Bagging) | Robust to noise, reduces variance | 98% |
| 4 | Gaussian Naive Bayes | Probabilistic | Handles mixed feature types well | 98% |
| 5 | KNN (k=5, Minkowski) | Instance-based | Non-parametric, no training phase | 95% |

> 🏆 **Best Models:** Logistic Regression & SVM — tied at **99% accuracy** with zero false positives on CKD-negative patients, critical in a clinical screening context.

## 📊 Cross-Validation (Random Forest · 5-Fold)

```python
scores           = [0.9375, 1.0000, 0.9750, 0.9875, 1.0000]
average_accuracy = "98.00%"
std_deviation    = "±2.3%"
```

Stable performance across all 5 folds confirms the model generalises well and is not overfitting to the train split.

## 🛠️ Tech Stack

```python
libraries = {
    "Data Wrangling"  : ["pandas", "numpy"],
    "ML Models"       : ["scikit-learn"],
    "Classifiers"     : ["LogisticRegression", "SVC", "RandomForestClassifier",
                         "KNeighborsClassifier", "GaussianNB"],
    "Preprocessing"   : ["StandardScaler", "train_test_split"],
    "Evaluation"      : ["confusion_matrix", "classification_report",
                         "f1_score", "roc_auc_score", "cross_val_score"],
    "Tuning"          : ["GridSearchCV"],
}
```

## 📁 Folder Structure

```
Week_4/
├── Classification_Assignment.ipynb   # Full ML pipeline & model benchmarking
└── README.md                         # This file
```

## 💡 Key Learnings

- In medical classification, **recall on the positive class** matters more than raw accuracy — a missed CKD diagnosis is far costlier than a false alarm
- **Logistic Regression** matched kernel-based SVM at 99% — clean, well-engineered features often outperform model complexity
- **StandardScaler** is essential for distance-based (KNN, SVM) and gradient-based (Logistic Regression) models; raw clinical features vary wildly in scale
- **One-Hot Encoding with `drop_first=True`** prevents the dummy variable trap while preserving all categorical information from `sg`
- **5-Fold Cross-Validation** (98% avg, ±2.3%) rules out a lucky train/test split and confirms real-world generalisability

---

[← Back to Main Repo](https://github.com/Rajasekaren-S-K/12-Week-AI-Engineering-Journey)

Week 4 of the Hope AI Master Program — Applied AI, Gen AI & Data Science 🚀
