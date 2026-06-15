# Perbandingan Performa Multi-Layer Perceptron (MLP) pada Dataset Iris

Repositori ini berisi eksperimen mengenai pengaruh berbagai **fungsi aktivasi** terhadap performa klasifikasi algoritma *Neural Network* **Multi-Layer Perceptron (MLP)** dengan menggunakan salah satu dataset benchmark paling populer, yaitu **Iris Dataset**.

Eksperimen ini ditulis dalam format Jupyter Notebook (`.ipynb`) menggunakan bahasa pemrograman Python dan pustaka *Machine Learning* populer `scikit-learn`.

## 📌 Pendahuluan & Tujuan
Fungsi aktivasi memegang peranan krusial dalam menentukan bagaimana sebuah jaringan saraf tiruan (*Artificial Neural Network*) mempelajari pola non-linear dari data. Tujuan utama dari praktikum/eksperimen ini adalah:
1. Membandingkan performa tiga jenis fungsi aktivasi populer pada arsitektur MLP:
   * **Sigmoid (Logistic)**
   * **Hyperbolic Tangent (Tanh)**
   * **Rectified Linear Unit (ReLU)**
2. Mengevaluasi metrik klasifikasi yang dihasilkan oleh masing-masing fungsi aktivasi untuk mengetahui fungsi mana yang paling optimal untuk karakteristik data kecil dan terstandardisasi.

## 📊 Deskripsi Dataset
Dataset yang digunakan adalah **Iris Dataset** yang dimuat langsung dari `sklearn.datasets`.
* **Jumlah Sampel:** 150 sampel bunga Iris.
* **Jumlah Fitur:** 4 fitur numerik (*Sepal Length*, *Sepal Width*, *Petal Length*, *Petal Width*).
* **Jumlah Kelas:** 3 kelas target (*Iris-Setosa*, *Iris-Versicolor*, *Iris-Virginica*) dengan distribusi seimbang (masing-masing 50 sampel).
* **Kondisi Data:** Tidak memiliki *missing values* (data lengkap).

## 🛠️ Tahapan Preprocessing Data
Untuk memastikan pelatihan model berjalan secara optimal dan adil, dilakukan tahapan berikut:
1. **Splitting Data:** Membagi data menjadi 80% Data Latih (120 sampel) dan 20% Data Uji (30 sampel) secara proporsional menggunakan metode *Stratified Sampling*.
2. **Feature Scaling:** Menormalisasi fitur numerik menggunakan `StandardScaler` (Z-score normalization) agar seluruh fitur berada pada skala yang seragam ($mean=0, \sigma=1$).

## ⚙️ Konfigurasi Model MLP
Setiap model MLP dikonfigurasi dengan parameter dasar yang **identik** agar hasil perbandingan bersifat objektif (*fair comparison*):
* **Hidden Layer Architecture:** 1 Hidden Layer dengan 16 neuron (`hidden_layer_sizes=(16,)`).
* **Solver:** `lbfgs` (sangat optimal untuk dataset berukuran kecil).
* **Max Iterations:** 1500 (ditingkatkan untuk menjamin konvergensi penuh model).
* **Random State:** 42 (untuk memastikan hasil dapat direplikasi secara konsisten).

## 📈 Hasil Evaluasi Performa
Model dievaluasi menggunakan data uji (*testing data*) berdasarkan 4 metrik evaluasi utama (*Weighted Average*):

| Fungsi Aktivasi | Accuracy | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic (Sigmoid)** | **0.9667** | **0.9697** | **0.9667** | **0.9666** |
| **Tanh** | **0.9667** | **0.9697** | **0.9667** | **0.9666** |
| **ReLU** | 0.9000 | 0.9024 | 0.9000 | 0.8997 |

### 💡 Kesimpulan Eksperimen
1. **Keunggulan Kurva Halus:** Pada dataset skala kecil dan terdistribusi normal seperti Iris, fungsi aktivasi berbasis kurva kontinu dan halus (**Logistic/Sigmoid** dan **Tanh**) terbukti menghasilkan performa yang lebih tinggi (**Akurasi 96.67%**) dibandingkan dengan fungsi linear sepotong seperti **ReLU** (Akurasi 90.00%).
2. **Pentingnya Hyperparameter Tuning:** Penggunaan solver `lbfgs` dikombinasikan dengan iterasi yang cukup (`max_iter=1500`) berhasil mengatasi masalah gagal konvergensi (*ConvergenceWarning*) dan membawa akurasi model masuk ke dalam rentang target optimal (0.90 - 1.00).

## 🚀 Cara Menjalankan Project

### Prerequisites
Pastikan Anda sudah menginstal Python (versi 3.8 atau yang lebih baru) beserta beberapa *libraries* berikut:
```bash
pip install pandas numpy scikit-learn matplotlib notebook