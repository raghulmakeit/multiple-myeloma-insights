# 📊 AI & ML-Driven Analysis of Multiple Myeloma Survival 📈

## 🔬 Project Overview  
This repository contains my **MSc dissertation** titled **"Exploring the Potential of Routine Cancer Data"**, submitted to the *University of Leeds, School of Mathematics*. The study applies **Artificial Intelligence (AI), Machine Learning (ML), and Statistical Modeling** to predict survival outcomes and analyze key risk factors for **Multiple Myeloma**, a malignancy of plasma cells.  

### **🚀 Key Contributions**
- **Data Engineering & Preprocessing:** Handling missing values, outlier detection, and feature engineering on a real-world cancer dataset.  
- **Exploratory Data Analysis (EDA):** Statistical summaries, visualizations, and correlation heatmaps to uncover trends in cancer survival.  
- **Survival Analysis:** Kaplan-Meier estimators & Cox Proportional Hazards Model to quantify survival risk factors.  
- **Machine Learning Models:** XGBoost, Random Forest, Logistic Regression, and SVM for patient outcome prediction.  
- **Deep Learning (DL):** Implementing ANN models for non-linear risk prediction.  
- **Model Evaluation:** Concordance Index, Log-Rank Tests, and AIC for statistical validation.  
- **Clinical & AI Integration:** Bridging AI insights with oncology research for **real-world medical applications**.

---

## 📂 **Repository Structure**
msc-myelo-research/ │── 📄 Dissertation.pdf # Full MSc dissertation document │── 📂 data/ # Datasets (processed and raw) │ ├── multiple_myeloma_data.csv # Filtered dataset for ML models │ ├── raw_data.csv # Original dataset before preprocessing │── 📂 notebooks/ # Jupyter Notebooks for analysis │ ├── 1_data_preprocessing.ipynb │ ├── 2_exploratory_analysis.ipynb │ ├── 3_survival_analysis.ipynb │ ├── 4_ml_models.ipynb │ ├── 5_deep_learning.ipynb │── 📂 models/ # Trained machine learning models │ ├── cox_model.pkl │ ├── xgboost_model.pkl │ ├── deep_learning_model.h5 │── 📂 results/ # Visualizations & reports │ ├── feature_importance.png │ ├── kaplan_meier_plot.png │ ├── cox_hazard_ratios.png │ ├── model_comparison.csv │── 📄 README.md # Project documentation │── 📄 requirements.txt # Python dependencies │── 📄 LICENSE # Project license


---

## 📊 Dataset & Preprocessing
### 📌 Data Source & Description
- The dataset consists of **12,492 patient observations** and **62 clinical variables**, collected from **Simulacrum**, a synthetic representation of National Health Service (NHS) cancer records.
- Includes demographic features (age, gender, ethnicity), comorbidities, treatment regimens, and survival outcomes.

### 🔧 Data Preprocessing Steps
- **Handling Missing Data:** Imputed using mean/median/mode; missing categorical values filled with ‘Unknown’.
- **Feature Selection:** Removed redundant/low-variance features to enhance model performance.
- **Data Normalization:** Scaled numerical features using MinMaxScaler.
- **Encoding Categorical Variables:** One-hot encoding for categorical features like `GENDER`, `INTENT OF TREATMENT`, etc.
- **Outlier Detection:** Identified and treated extreme values in BMI and Comorbidity Scores.

---

## 📈 Exploratory Data Analysis (EDA)
### Key Findings:
✔️ **Age Distribution:** Majority of patients aged 40-95 years, with survival decreasing in higher age groups.  
✔️ **Gender Impact:** Males (57%) had a slightly higher mortality rate than females.  
✔️ **Kaplan-Meier Survival Analysis:** Significant drop in survival rate for high comorbidity patients.  
✔️ **Treatment Effectiveness:** Earlier treatment initiation linked to better survival outcomes.  

---

## 🏥 Survival Analysis & Statistical Models
We implemented **Kaplan-Meier Estimators and Cox Proportional Hazards Model** to analyze patient survival probabilities.

### 1️⃣ Kaplan-Meier Survival Curve
📌 **Findings:**  
- **Higher Age = Lower Survival Probability**
- **Early Treatment = Improved Outcomes**
- **Comorbidity Score = Key Predictor of Survival**

![Kaplan-Meier Curve](results/kaplan_meier_plot.png)

### 2️⃣ Cox Proportional Hazards Model
- Used to estimate **hazard ratios (HR)** for various predictors.
- **Age, BMI, Comorbidity Score, and Time to First Treatment** were found to be **statistically significant** predictors.  
- **Concordance Index = 0.668**, indicating a **moderate predictive power**.

---

## 🤖 Machine Learning & AI Models
We experimented with various **ML & AI models** to predict patient survival outcomes.

### 📌 Models Implemented:
| Model               | Accuracy  | Precision | Recall | AUC-ROC |
|---------------------|----------|----------|--------|---------|
| Logistic Regression | 73.4%    | 70.2%    | 68.9%  | 0.76    |
| Random Forest       | 79.8%    | 76.4%    | 75.1%  | 0.82    |
| XGBoost            | 82.1%    | 80.3%    | 79.5%  | 0.85    |
| SVM                | 78.9%    | 74.5%    | 73.2%  | 0.81    |
| ANN (Deep Learning)| 85.7%    | 83.2%    | 82.8%  | 0.88    |

- **XGBoost & Deep Learning** provided the best results with **85.7% accuracy**.  
- **Feature Importance:**  
  - **Age**, **Time to First Treatment**, and **Comorbidity Score** were the top **3 predictors**.  

![Feature Importance](results/feature_importance.png)



🔮 Future Work & Enhancements
Hyperparameter tuning: Improve ML model performance using Bayesian Optimization.
Deep Learning Advancements: Experiment with LSTMs & Transformers for time-series survival prediction.
Explainability & Interpretability: Use SHAP values for better model explainability.
Deploy as Web App: Integrate models into a Flask/Django API for real-time survival predictions.
🎓 Author & Acknowledgments
👤 Raghul Seerangan | MS Data Science, University of Leeds
🔗 Dissertation Advisor: Duncan Wilson, Kara-Lousie Royle, Lesley Smith
