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
  Given a feature matrix \( X \), we decompose it as:  
  \[
  X = U S V^T
  \]
  where:  
  - \( U \) is an orthogonal matrix representing the left singular vectors  
  - \( S \) is a diagonal matrix containing singular values  
  - \( V \) is an orthogonal matrix representing the right singular vectors  

- **Choosing Principal Components**:  
  The singular values in \( S \) indicate the importance of each component. To retain **maximum variance**, the top \( k \) components are selected:  
  \[
  X_{\text{reduced}} = U(:,1:k) \times S(1:k,1:k)
  \]  
  where \( k \) is the optimal number of dimensions chosen based on variance explained.

- **Singular Value Plot**:  
  A plot of singular values helps determine the optimal value of \( k \) by analyzing the **elbow point**.

### 🔹 Model Training & Evaluation  
- **Classifier**: Logistic Regression (`fitclinear` in MATLAB)  
- **Train-Test Split**: **70% Train, 30% Test**  
- **Performance Metrics**:  
  - **Accuracy**  
  - **Confusion Matrix**  
  - **Singular Value Plot & Data Projection**  

---

## 📊 Results  

- **SVD effectively reduced dataset dimensionality while preserving key information**  
- **Logistic Regression achieved high accuracy** with optimized computational efficiency  
- **Visualization of Singular Values & Data Projection**:  

📌 **Singular Value Plot**  

📌 **2D Projection of Data**   

📌 **Confusion Matrix**  

---

## 🔍 Prediction Output  

### ✅ Sample Prediction Pipeline  
1. **Input**: Patient’s health parameters (age, BP, glucose levels, etc.)  
2. **Preprocessing**: Handling missing values, normalization  
3. **Feature Transformation**: SVD-based dimensionality reduction  
4. **Model Processing**: Logistic Regression  
5. **Output**: CKD Prediction (`1 = CKD`, `0 = Not CKD`)  

