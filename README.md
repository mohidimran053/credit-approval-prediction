# Credit Approval Prediction

## Project Overview
This project predicts whether a bank customer’s loan will be approved using machine learning. The dataset includes customer details such as credit history, savings balance, job information, and other financial attributes.  

The goal is to compare **Decision Tree** and **Logistic Regression** models to determine which approach provides better predictive accuracy and interpretability.

---

## Dataset
- **File:** `CreditData.csv`  
- **Features:** Credit history, savings balance, job information, years of employment, and other customer attributes  
- **Target variable:** `Approved` (`Yes` or `No`)  

### Preprocessing
- Split dataset into **80% training** and **20% testing**  
- One-hot encoding applied to categorical features for model compatibility  
- Feature scaling applied where necessary  

---

## Models Used

### 1. Decision Tree Classifier
- Implemented using `DecisionTreeClassifier` from scikit-learn  
- Maximum depth set to 5 to prevent overfitting  
- Produces interpretable flowchart-like splits showing feature importance  

### 2. Logistic Regression
- Computes probabilities and weights for each feature  
- Provides insight into how each variable affects loan approval  
- Used as a baseline linear model for comparison  

---

## Model Testing
- Both models trained on the **80% training set** and evaluated on **20% test set**  
- **Evaluation Metrics:**
  - Confusion Matrix (true positives, false positives, true negatives, false negatives)  
  - Accuracy  
  - Precision  
  - Recall  

### Decision Tree Performance
- Accuracy: 83%  
- Precision: 80%  
- Recall: 78%  
- Visualization highlighted key features: **credit history, savings account status, years of employment**  

### Logistic Regression Performance
- Slightly lower accuracy and recall compared to Decision Tree  
- Provided coefficients showing feature impact on loan approval  

---

## Results & Discussion
- **Decision Tree** performed better for interpretability and recall  
- Key insights:
  - Credit history, savings, and employment years strongly influence loan approval  
  - Decision Tree is practical for business applications where visual explanation is valuable  
- Logistic Regression gives a clear understanding of feature influence but is less interpretable  

> Both models are useful, but Decision Tree is more actionable for real-world banking decisions.

---

## Files in the Repo
- `CreditData.csv` – Original dataset  
- `data_preprocessing.ipynb` – Data cleaning and encoding  
- `model_training.ipynb` – Decision Tree and Logistic Regression implementation  
- `evaluation.ipynb` – Confusion matrices, metrics calculation, and visualization  

---

## References
- Scikit-learn documentation: [https://scikit-learn.org/](https://scikit-learn.org/)
