# 🧠 Classification Model Pipeline

Notebook ini merupakan **kelanjutan dari tahapan preprocessing data** yang telah dilakukan sebelumnya. Fokus dari notebook ini adalah membangun dan mengevaluasi model klasifikasi secara menyeluruh, mulai dari data transformation untuk menyesuaikan format data hingga tuning hyperparameter dan evaluasi model menggunakan ROC Curve.

---

## 🧾 Table of Contents

1. [Import Library](#import-library)
2. [Load Dataset](#load-dataset)
3. [Label Encoding](#label-encoding)
4. [Data Splitting](#data-splitting)
5. [Model Fitting](#model-fitting)
6. [Cross-Validation & Learning Curves](#cross-validation--learning-curves)
7. [Hyperparameter Tuning](#hyperparameter-tuning)
8. [Bootstrapping](#bootstrapping)
9. [Metric Evaluation - ROC Curve](#metric-evaluation---roc-curve)

---

## ⚙️ Tools

1. [Pandas](https://pandas.pydata.org/)
2. [NumPy](https://numpy.org/)
3. [Matplotlib](https://matplotlib.org/)
4. [scikit-learn](https://scikit-learn.org/)

---

## 📒 Notebook Sections

### 📌 Import Library
Mengimpor semua pustaka Python yang dibutuhkan untuk manipulasi data, visualisasi, dan pemodelan.

### 📌 Load Dataset
Membaca dataset ke dalam format DataFrame untuk dianalisis dan digunakan dalam pelatihan model.

### 📌 Label Encoding
Mengubah variabel kategorikal menjadi bentuk numerik menggunakan teknik seperti LabelEncoder atau OneHotEncoder.

### 📌 Data Splitting
Membagi data menjadi set pelatihan dan pengujian, biasanya menggunakan `train_test_split` dari scikit-learn.

### 📌 Model Fitting
Melatih model klasifikasi dasar (contoh: Decision Tree, Random Forest, SVM) terhadap data latih.

### 📌 Cross-Validation & Learning Curves
Mengevaluasi model secara lebih menyeluruh menggunakan k-Fold Cross-Validation serta melihat performa melalui kurva pembelajaran (learning curve).

### 📌 Hyperparameter Tuning
Hyperparameter tuning dilakukan menggunakan pendekatan **Randomized Search**, yang mengacak kombinasi parameter dari distribusi tertentu dan memilih yang terbaik berdasarkan skor validasi.

- **Parameter yang dicoba**:
  - `'max_depth'`: `[None, 10, 20, 30]`
  - `'min_samples_split'`: `[2, 5, 10]`
  - `'n_estimators'`: `[50, 100, 200]`
  - `'max_features'`: `['auto', 'sqrt']`
  - `'bootstrap'`: `[True, False]`

### 📌 Bootstrapping
Menggunakan teknik sampling dengan pengembalian untuk mengukur variabilitas estimasi dan meningkatkan ketahanan model.

### 📌 Metric Evaluation - ROC Curve
Mengevaluasi performa model menggunakan kurva ROC (Receiver Operating Characteristic) untuk melihat trade-off antara True Positive Rate dan False Positive Rate, serta menghitung AUC (Area Under Curve).

---

## 📈 Evaluation Metrics
Model dievaluasi menggunakan:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
