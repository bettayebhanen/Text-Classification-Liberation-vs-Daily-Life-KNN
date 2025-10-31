

# 🕊️ Text-Classification-Liberation-vs-Daily-Life-KNN

## 📋 Project Overview
This project focuses on **text classification** — distinguishing between sentences that express the **Meaning of Liberation** and those related to **Everyday Life**.  
It uses the **K-Nearest Neighbors (KNN)** algorithm combined with **TF-IDF vectorization** and **Stratified K-Fold Cross-Validation** to ensure consistent and reliable results.

---

## 🎯 Results

### **Cross-Validation**
- **Average Accuracy**: `0.8625`  
- **Observation**: Stable and consistent performance across all folds.

### **Final Test Evaluation**
- **Accuracy**: `0.90`  
- **Precision, Recall, and F1-score** all indicate strong generalization and balanced performance between both classes.

---

## 📊 Dataset

- **Source**: Custom dataset of 100 sentences  
- **Samples**: 100 total  
- **Classes**:  
  - `0` : Meaning of Liberation  
  - `1` : Everyday Life  
- **Format**:  
  - `id`: Sentence index  
  - `text`: The actual sentence  
  - `target`: Class label  

Example rows:

| id | text | target |
|----|------|---------|
| 1 | Freedom is not given, it is taken. | 0 |
| 50 | We go shopping on weekends. | 1 |

---

## 🛠️ Technical Implementation

### **Algorithms & Tools**
- **Algorithm**: K-Nearest Neighbors (KNN)  
- **Validation**: Stratified K-Fold (k = 5)  
- **Libraries**: scikit-learn, pandas, numpy, matplotlib, seaborn  
- **Vectorization**: TF-IDF (Term Frequency–Inverse Document Frequency)  
- **Normalization**: L2 Normalizer  
- **Evaluation Metrics**: Accuracy, Precision, Recall, F1-Score, Confusion Matrix  

---

### **Model Configuration**
| Parameter | Value |
|------------|--------|
| n_neighbors | 5 |
| Cross-Validation Splits | 5 (Stratified) |
| Test Split | 20% hold-out for final evaluation |
| Vectorizer | TF-IDF |
| Normalization | L2 Normalizer |

---

## 🧩 Key Insights

- **TF-IDF** captures meaningful words rather than just frequent ones — helping the model focus on the *semantic value* of the text.  
- **Normalizer** was preferred over `StandardScaler` for text-based feature spaces because TF-IDF vectors are sparse and represent direction more than magnitude.  
- **KNN** provides an interpretable, distance-based decision-making approach, ideal for small text datasets.  
- **Cross-validation** ensures stable performance and prevents overfitting, even on a limited dataset.

---

 

---

> “True freedom begins when we learn — and teach — how to make data meaningful.”  
> — Hanen bettayeb
