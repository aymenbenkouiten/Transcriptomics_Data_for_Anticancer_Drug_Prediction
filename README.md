# 🧬 Drug Response Prediction from Transcriptomic Data

This project aims to predict cancer cell line sensitivity to anticancer drugs using transcriptomic profiles (gene expression data). It includes both regression and classification tasks, using machine learning models and interpretability tools.

---

## 📁 Dataset

The dataset contains:
- Gene expression profiles of cancer cell lines
- Drug information (ID, name, min/max concentrations)
- Response measurements: **AUC** and **LN_IC50**

Each row represents a **cell line × drug** pair.

---

## 🎯 Objectives

- Predict **AUC** and **LN_IC50** using gene expression and drug features (regression)
- Convert the problem into a binary classification: sensitive vs resistant
- Test several thresholds (median, 0.3, 0.5, 0.7)
- Train and evaluate models (Random Forest, XGBoost, Lasso, SVM)
- Identify most important genes using SHAP and feature importances
- Visualize sample distributions and model behavior (PCA, t-SNE)

---

## 🧪 Models Used

### Regression
- Random Forest Regressor
- XGBoost Regressor
- Lasso

### Classification
- Random Forest Classifier
- XGBoost Classifier
- Support Vector Machine (SVM)

---

## ⚙️ Main Steps

1. **Data preprocessing**  
   - Check for duplicates and missing values  
   - One-hot encoding of drug IDs  
   - Feature normalization

2. **Exploratory Data Analysis (EDA)**  
   - Distributions of AUC and LN_IC50  
   - Class balance for different thresholds

3. **Model training & evaluation**  
   - Regression: MAE, RMSE, R²  
   - Classification: Accuracy, F1-score, ROC AUC, confusion matrices

4. **Interpretation**  
   - SHAP summary plots  
   - Feature importances  
   - PCA and t-SNE visualizations

---

## 📊 Key Findings

- **Random Forest and XGBoost** show strong performance for both regression and classification.
- **AUC is easier to predict** than LN_IC50 (less noise, smoother response).
- **Median threshold (~0.628)** provides balanced classes and stable models.
- **Seuil 0.70** improves sensitive detection.
- SHAP reveals biologically relevant genes for each drug.

---

## 📁 Project Structure

```bash
.
├── data/                 # Raw data files (not included here)
├── figures/              # All generated plots and figures
├── notebook.ipynb        # Main analysis notebook
├── README.md             # Project summary
```

---

## 📌 Requirements

```bash
scikit-learn
xgboost
pandas
numpy
matplotlib
seaborn
shap
tqdm
```

Install via:

```bash
pip install -r requirements.txt
```

---

## 📜 License

This project is for academic and educational purposes only.
```

