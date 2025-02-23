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
- **Computing SVD**:  
  \[
  X = U S V^T
  \]
- **Choosing Principal Components**: Selecting the top `k = 5` components to retain maximum variance  
- **Feature Transformation**:  
  \[
  X_{\text{reduced}} = U(:,1:k) \times S(1:k,1:k)
  \]  

### 🔹 Model Training & Evaluation  
- **Classifier**: Logistic Regression (`fitclinear` in MATLAB)  
- **Train-Test Split**: **70% Train, 30% Test**  
- **Performance Metrics**:  
  - **Accuracy**  
  - **Confusion Matrix**  
  - **Singular Value Plot & Data Projection**  

---

## 📊 Results  

- **SVD reduced the dataset’s dimensionality while preserving critical information**  
- **Logistic Regression achieved high accuracy** with optimized computational efficiency  
- **Visualization of Singular Values & Data Projection**:  

📌 **Singular Value Plot**  

📌 **2D Projection of Data**   

📌 **Confusion Matrix**  
![Confusion Matrix](https://via.placeholder.com/400)  

---

## 🔍 Prediction Output  

### ✅ Sample Prediction Pipeline  
1. **Input**: Patient’s health parameters (age, BP, glucose levels, etc.)  
2. **Preprocessing**: Handling missing values, normalization  
3. **Feature Transformation**: SVD-based dimensionality reduction  
4. **Model Processing**: Logistic Regression  
5. **Output**: CKD Prediction (`1 = CKD`, `0 = Not CKD`)  

### 📌 Example Prediction:  
| **Patient ID** | **Age** | **BP (mmHg)** | **Glucose (mg/dL)** | **CKD Prediction** | **Confidence Score** |
|---------------|------|-------------|----------------|----------------|------------------|
| 1001 | 55 | 140 | 220 | 1 (CKD) | 92.5% |
| 1002 | 45 | 130 | 180 | 0 (Not CKD) | 89.3% |
| 1003 | 65 | 160 | 250 | 1 (CKD) | 95.1% |

📢 _Note: Replace with actual model predictions._

---


