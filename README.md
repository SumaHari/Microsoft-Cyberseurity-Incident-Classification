# Cybersecurity Incident Classification using Machine Learning

This project leverages machine learning to classify cybersecurity incidents into three categories:
- **BenignPositive**
- **FalsePositive**
- **TruePositive**

It is part of a Microsoft-sponsored initiative to enhance threat detection workflows and assist SOC (Security Operations Center) teams with reliable automated predictions.

---

## 📌 Objective

To build a robust multi-class classification model using the GUIDE dataset that accurately identifies different cybersecurity incident types and integrates seamlessly into SOC workflows.

---

## 📊 Dataset

- **Source**: GUIDE Cybersecurity Dataset (Microsoft Sponsored)
- **Size**: 1.2M+ entries
- **Target classes**: BenignPositive, FalsePositive, TruePositive
- **Challenges**:
  - Imbalanced classes
  - High dimensionality
  - Missing data

---

## 🧹 Preprocessing & Feature Engineering

- Removed non-informative features
- Handled missing values using domain rules and visual inspection
- Label encoding and one-hot encoding for categorical features
- Stratified sampling (10% / 30%) due to memory limitations
- Feature selection via correlation and feature importance

---

## 🧠 Model Training

- **Model used**: Random Forest Classifier
- **Validation Strategy**: Stratified Train/Validation/Test Split
- **Metrics**: Precision, Recall, F1 Score, Accuracy, Macro-F1

---

## 📈 Results

### ✅ Validation Set
- **Macro F1 Score**: `0.815`
- **Accuracy**: `0.83`

| Class           | Precision | Recall | F1 Score |
|----------------|-----------|--------|----------|
| BenignPositive | 0.83      | 0.89   | 0.86     |
| FalsePositive  | 0.76      | 0.75   | 0.75     |
| TruePositive   | 0.85      | 0.83   | 0.84     |

---

### 🧪 Test Set
- **Macro F1 Score**: `0.780`
- **Accuracy**: `0.80`

| Class           | Precision | Recall | F1 Score |
|----------------|-----------|--------|----------|
| BenignPositive | 0.79      | 0.86   | 0.82     |
| FalsePositive  | 0.75      | 0.69   | 0.72     |
| TruePositive   | 0.83      | 0.82   | 0.83     |

---

## 🔍 Interpretation & Improvements

- **SHAP** used for model interpretability (planned)
- **Class imbalance** affected FalsePositive performance
- **Next Steps**:
  - Try XGBoost and LightGBM
  - Use SMOTE or class weights
  - Threshold tuning per class

---

## 🛠️ Tools & Technologies

- Python, Pandas, NumPy
- Scikit-learn
- Matplotlib & Seaborn
- Jupyter Notebook
- Dask (for scalable data handling)

---

## 📁 Project Structure
Cybersecurity_Incident/
│
├── data/ # Raw and processed data
├── models/ # Trained model files
├── notebooks/ # Jupyter notebooks for EDA and modeling
├── outputs/ # Result logs and plots
├── README.md # Project overview
└── requirements.txt # Python dependencies



