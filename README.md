# 🏥 Chronic Kidney Disease Prediction using Singular Value Decomposition (SVD)  

📌 **Author**: Sivachandra K B  
📅 **Project ID**: CB.SC.P2DSC24018  
📜 **Keywords**: Chronic Kidney Disease, Singular Value Decomposition, Logistic Regression, Machine Learning  

---

## 📌 Project Overview  
This study aims to predict **Chronic Kidney Disease (CKD)** using a **dimensionality reduction approach based on Singular Value Decomposition (SVD)**, followed by a **logistic regression classifier**. The methodology involves:  
- **Data Preprocessing**: Handling missing values, encoding categorical variables  
- **Dimensionality Reduction**: Applying **SVD** to extract significant features  
- **Model Training**: Logistic Regression for CKD classification  
- **Evaluation**: Performance analysis using accuracy, confusion matrix, and visualization  

---

## 🛠 Methodology  

### 🔹 Data Preprocessing  
1. **Dataset**: Patient health features (age, blood pressure, blood glucose levels, etc.)  
2. **Binary Encoding**: Target variable `"class"` is encoded as **1 (CKD)**, **0 (Non-CKD)**  
3. **Handling Missing Values**: Missing values are replaced with the column mean  

### 🔹 Dimensionality Reduction with SVD  
Singular Value Decomposition (SVD) is applied to reduce the dataset’s dimensionality while preserving critical information.  

- **Matrix Factorization**:  
  Given a feature matrix `X`, we decompose it as:
X = U * S * Vᵀ

where:  
- `U` is an orthogonal matrix representing the left singular vectors  
- `S` is a diagonal matrix containing singular values  
- `V` is an orthogonal matrix representing the right singular vectors  

- **Choosing Principal Components**:  
The singular values in `S` indicate the importance of each component. To retain **maximum variance**, the top `k` components are selected:  

