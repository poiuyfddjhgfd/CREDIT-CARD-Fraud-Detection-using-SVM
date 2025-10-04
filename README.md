# Fraud Detection using SVM

This project implements a fraud detection system using a Support Vector Machine (SVM) classifier. The model is trained and tested on credit card transaction data to identify fraudulent activities.

---

## 📁 Dataset

The dataset used is `fraudTest.csv`, which contains 555,719 transactions with 23 features. The target variable is `is_fraud`, indicating whether a transaction is fraudulent (1) or not (0).

---

## 🧹 Data Preprocessing

- Dropped irrelevant columns:  
  `Unnamed: 0`, `cc_num`, `first`, `last`, `street`, `city`, `state`, `zip`, `dob`, `trans_num`, `trans_date_trans_time`
- Converted date columns to datetime format
- Encoded categorical variables using `LabelEncoder`:
  - `merchant`
  - `category`
  - `gender`
  - `job`

---

## 📊 Exploratory Data Analysis

- Visualized the distribution of fraud vs. non-fraud transactions using a pie chart
- Only ~0.4% of transactions are fraudulent, indicating a highly imbalanced dataset

---

## 🤖 Model Training

- Used `SVC` from `sklearn.svm`
- Features used for training:
  - `merchant`, `category`, `amt`, `gender`, `lat`, `long`, `city_pop`, `job`, `unix_time`, `merch_lat`, `merch_long`
- Target variable: `is_fraud`

---

## 📈 Model Performance

- **Training Accuracy**: 99.61%
- **Test Accuracy**: 99.61%

---

## 🚀 How to Run

1. Ensure the following Python libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
2.Place fraudTest.csv in the same directory as the notebook.

3.Run the Jupyter notebook FRAUD DETECTION (1).ipynb cell by cell.   
