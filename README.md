# Drug Approval Prediction 🚀

## 📌 Project Overview
This project aims to predict **drug approval outcomes** (Approved vs. Unapproved) using machine learning models trained on clinical trial and drug-related features.  
The dataset is sourced from the [DrugApp GitHub repository](https://github.com/HUBioDataLab/DrugApp) and enriched with curated drug attributes.

The workflow includes:
- Data preprocessing and cleaning  
- Feature engineering (removal of irrelevant/patent-related features)  
- Model development with **Random Forest Classifier**  
- Model evaluation with **cross-validation** (ROC-AUC, Precision-Recall, F1-score, MCC, etc.)

---

## 📂 Dataset
- **Source**: [DrugApp GitHub](https://github.com/HUBioDataLab/DrugApp)  
- **Target Variable**: `Label` →  
  - `1` → Approved drug  
  - `0` → Unapproved drug  
- **Features**:  
  - Clinical trial study designs  
  - Drug molecular and non-molecular attributes  
  - Patent-related columns (removed in preprocessing since not significant for approval prediction)

---

## ⚙️ Installation & Requirements
Install dependencies before running the notebook:

```bash
pip install -r requirements.txt
```

Key libraries:
- `pandas`
- `scikit-learn`
- `matplotlib`
- `seaborn`

---

## 🚀 Model Training Workflow
1. **Data Preprocessing**  
   - Removed non-informative and patent-related columns  
   - Handled categorical and numeric features  

2. **Model Development**  
   - Base model: **Random Forest Classifier**
   - Based model: **XGboost Classifier**

3. **Hyperparameter Tuning**  
   - Implemented with **Optuna**  
   - Optimized parameters for maximum ROC-AUC and F1-score  

4. **Evaluation Metrics**  
   - Accuracy  
   - Precision & Recall   
   - ROC-AUC curve  
   - Precision-Recall curve  


---

## 📊 Results & Insights
The model shows competitive performance in predicting **drug approval status**.  

- **ROC-AUC Curve** demonstrates strong discriminative power.  
- **Precision-Recall Curve** highlights effectiveness in imbalanced datasets.  

📌 Future work: compare with **Nature article benchmark** (https://www.nature.com/articles/s41598-024-72868-0), where the authors used deep learning on clinical trial features.  

---

## 🖼️ Feature Image
![Drug Approval Prediction](https://raw.githubusercontent.com/HUBioDataLab/DrugApp/main/drugapp_image.png)

---

## 📌 References
- HUBioDataLab DrugApp Dataset → [GitHub](https://github.com/HUBioDataLab/DrugApp)  
- Related Research → [Nature Scientific Reports (2024)](https://www.nature.com/articles/s41598-024-72868-0)  


