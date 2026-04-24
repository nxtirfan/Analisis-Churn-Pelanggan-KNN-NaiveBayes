# Analisis Prediktif Churn Pelanggan  
### Menggunakan K-Nearest Neighbors (KNN) dan Naive Bayes

## Deskripsi Proyek

Proyek ini bertujuan untuk membangun model machine learning yang mampu memprediksi kemungkinan pelanggan melakukan churn (berhenti menggunakan layanan) pada platform e-commerce. Prediksi ini penting untuk membantu perusahaan dalam mengambil langkah preventif guna meningkatkan retensi pelanggan.

Dalam proyek ini digunakan dua pendekatan algoritma klasifikasi, yaitu:

- **K-Nearest Neighbors (KNN)** → model berbasis jarak yang mengklasifikasikan data berdasarkan kedekatan dengan tetangga terdekat  
- **Naive Bayes (GaussianNB)** → model probabilistik yang mengasumsikan independensi antar fitur  

Selain membangun model, analisis ini juga berfokus pada bagaimana meningkatkan performa prediksi melalui preprocessing data yang tepat dan evaluasi model yang komprehensif.

---

## 🔍 Pendekatan Analisis

Untuk menghasilkan model yang optimal, dilakukan beberapa tahapan utama sebagai berikut:

### 1. Exploratory Data Analysis (EDA)
- Menganalisis distribusi data, terutama variabel target (churn)
- Mengidentifikasi pola hubungan antara fitur dengan churn
- Visualisasi data menggunakan grafik (countplot, heatmap, boxplot)

### 2. Data Preprocessing
- Menangani missing value menggunakan imputasi median
- Mengubah variabel kategorikal menjadi numerik (one-hot encoding)
- Melakukan pembagian data (train-test split) secara stratified

### 3. Feature Scaling
- Normalisasi data menggunakan StandardScaler  
- Penting untuk algoritma berbasis jarak seperti KNN

### 4. Penanganan Imbalanced Data
- Menggunakan **SMOTE (Synthetic Minority Oversampling Technique)**
- Bertujuan untuk menyeimbangkan distribusi kelas churn dan non-churn

### 5. Modeling
- **Naive Bayes** sebagai baseline model
- **KNN dengan GridSearchCV** untuk mendapatkan hyperparameter terbaik:
  - jumlah tetangga (`n_neighbors`)
  - metode pembobotan (`weights`)
  - metrik jarak (`metric`)

### 6. Evaluasi Model
- Menggunakan metrik:
  - Accuracy
  - Recall (fokus pada churn)
  - F1-Score
- Confusion matrix untuk analisis kesalahan prediksi
- Cross-validation untuk mengukur kestabilan model

---

## 🎯 Tujuan Akhir

Model yang dihasilkan diharapkan mampu:
- Mengidentifikasi pelanggan yang berpotensi churn secara akurat  
- Membantu pengambilan keputusan berbasis data  
- Mendukung strategi retensi pelanggan dalam bisnis e-commerce  

---
