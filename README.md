# 🧠 WiDS Datathon 2025 – Sex-Specific ADHD Prediction
**Unraveling the Mysteries of the Female Brain: Sex Patterns in ADHD Diagnosis**

This project was developed as part of the 2025 WiDS Datathon Global Challenge, focusing on building predictive models to uncover brain activity and behavioral patterns in ADHD diagnosis — with a spotlight on sex-based differences.

---

## 🔍 Research Question
> Can we build a model that predicts an individual's sex and ADHD diagnosis using functional brain imaging data of children and adolescents along with socio-demographic, emotional, and parenting information?

---

## 🧾 Dataset Overview

The dataset contains over **1,200 training subjects** and **300+ test subjects** and includes:

- ✅ `ADHD_Outcome` and `Sex_F` (targets)
- 🧠 Functional brain imaging data (36P Pearson correlation connectome matrices)
- 📋 Socio-demographic metadata (categorical + quantitative):
  - Handedness, site location, ethnicity, parental education/occupation
- 📊 Psychological & behavioral assessments:
  - Strengths and Difficulties Questionnaire (SDQ)
  - Alabama Parenting Questionnaire (APQ)
  - Emotion and Health Questionnaire (EHQ)

---

## 🧱 Project Structure

### `01_data_preparation.ipynb`
- Load and merge all datasets
- Identify and separate brain vs. non-brain features
- Handle missing values, encoding, and scaling
- Save:
  - `X_brain_scaled.npy`
  - `X_non_brain_processed.npy`
  - `y.npy`
  - `brain_scaler.pkl`
  - `final_preprocessor.pkl`

---

### `02_eda.ipynb` *(in progress)*
- Visualize target distributions
- Analyze feature variance and imbalance
- Correlation matrices for quantitative/categorical variables
- Dimensionality reduction: PCA, t-SNE
- Feature selection: mutual information, F-statistics

---

### `03_classical_modeling.ipynb`
- Train/test split with stratified multi-output logic
- Model benchmarking: Logistic Regression, Random Forest, XGBoost
- Custom weighted F1 evaluation aligned with competition rules:
  > **2× weight on Female ADHD (ADHD=1, Sex_F=1)**
- Hyperparameter tuning with `RandomizedSearchCV`
- ✅ Save best classical model

---

### `04_submission_pipeline.ipynb`
- Load and preprocess test set with **saved pipeline**
- Match encoded features to training
- Generate predictions using saved model
- Format predictions into valid Kaggle submission file

---

### `05_reporting.ipynb` *(planned)*
- Summary of key findings
- Feature importance insights
- Performance metrics with breakdown by sex and diagnosis
- Visuals and final reflection

---

### `06_deep_learning_models.ipynb` *(planned)*
- Tabular deep learning with `MLP`
- Connectome-only modeling with CNNs or 1D ResNets
- Custom loss functions and multi-label output
- Early stopping, dropout, batch norm
- Comparison with classical model performance

---

## 🛠 Tools & Libraries
- Python 3, pandas, NumPy, scikit-learn
- XGBoost, joblib, matplotlib, seaborn
- Google Colab + GitHub
- PyTorch (planned for Part 6)

---

## 🏁 Goal
To build a robust and interpretable model that not only performs well but also highlights potential **gender disparities** in ADHD diagnosis — with a strong focus on scientific integrity and transparency.

---

## 📬 Submission Format

The final submission includes three columns:
participant_id,ADHD_Outcome,Sex_F v1nMpCoLGU0V,1,1 uEZHGukIUQ0k,0,1 ...


---

📌 Stay tuned as we dive into deep learning next and refine this pipeline into a reproducible research asset.
