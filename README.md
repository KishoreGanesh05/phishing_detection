

# 🔐 Phishing Website Detection using Machine Learning

## 📌 Overview

This project focuses on detecting **phishing websites** using machine learning techniques. It analyzes URL patterns, domain information, and webpage content to classify websites as:

* ✅ Legitimate
* ❌ Phishing

The system uses multiple ML algorithms and feature extraction techniques to identify malicious websites with high accuracy.

---

## 🚀 Key Features

* 🔍 URL-based, domain-based, and content-based feature extraction
* 🤖 Multiple machine learning models:

  * Random Forest
  * Support Vector Machine (SVM)
  * Gradient Boosting
  * Logistic Regression
  * Naïve Bayes
* 📊 Feature selection using:

  * SelectKBest
  * Recursive Feature Elimination (RFE)
* 📈 Performance evaluation with multiple metrics
* 💾 Model saving using `joblib`
* 🔗 End-to-end **prediction pipeline for any URL**

---

## 🧠 Methodology

```id="flow123"
Data Collection → Preprocessing → Feature Extraction → Feature Selection →
Model Training → Evaluation → Prediction Pipeline
```

---

## 📂 Dataset

* Source: **PhishTank + Kaggle dataset** 
* Includes:

  * Phishing URLs
  * Legitimate URLs
* Approx split:

  * 80% Training
  * 20% Testing

---

## ⚙️ Feature Engineering

### 🔹 URL-Based Features

* URL length
* Presence of `@`, `-`, `//`
* Number of dots, slashes, digits
* Redirection detection

### 🔹 Domain-Based Features

* Domain age
* Domain registration length
* DNS availability

### 🔹 Content-Based Features

* Number of links/scripts
* Presence of forms & iframes
* External link ratio

---

## 🤖 Machine Learning Models

* Random Forest (Best performing)
* Support Vector Machine (SVM)
* Gradient Boosting
* Logistic Regression
* Naïve Bayes

---

## 📊 Evaluation Metrics

* Accuracy
* Precision
* Recall
* F1-Score
* AUC-ROC
* Cross-validation accuracy

---

## 📈 Results

| Model               | Accuracy | F1 Score | AUC  |
| ------------------- | -------- | -------- | ---- |
| Random Forest       | 86%      | 0.86     | 0.91 |
| SVM                 | 85%      | 0.85     | 0.92 |
| Gradient Boosting   | 84%      | 0.84     | 0.91 |
| Logistic Regression | 83%      | 0.82     | 0.91 |
| Naïve Bayes         | 77.5%    | 0.74     | 0.86 |

👉 **Best Model:** Random Forest 

---

## 🖥️ Project Structure

```id="struct456"
├── data_preprocessing.py
├── feature_extraction.py
├── feature_selection.py
├── model_training.py
├── evaluation.py
├── prediction_pipeline.py
├── saved_models/
│   ├── phishing_model.joblib
│   ├── scaler.joblib
│   ├── selected_features.joblib
├── dataset/
│   └── dataset_phishing.csv
```

---


## 🔮 Prediction Pipeline

The system:

1. Extracts features from URL
2. Cleans & preprocesses data
3. Applies scaling
4. Selects important features
5. Predicts using trained model

👉 Output:

* Prediction: Phishing / Legitimate
* Confidence score

---

## 📊 Visualizations

* ROC Curves
* Confusion Matrix
* Feature Importance Plot
* Model Comparison Graph

---

## ⚠️ Limitations

* Feature extraction can be slow (especially content-based)
* Depends on dataset quality
* May struggle with highly sophisticated zero-day phishing attacks

---

## 🔮 Future Enhancements

* 🌐 Real-time browser extension
* 🧠 Deep learning models (CNN, RNN)
* 📄 NLP-based phishing detection
* ☁️ Deployment as API / web app
* 🔍 Explainable AI integration

