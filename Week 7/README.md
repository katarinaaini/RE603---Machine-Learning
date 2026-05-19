# Supervised Learning: Titanic Passenger Classification

Repository ini berisi proyek praktis pembelajaran terbimbing (*Supervised Learning*) menggunakan berbagai algoritma pembelajaran mesin untuk mengklasifikasikan keselamatan penumpang kapal Titanic. Analisis dilakukan secara komprehensif mulai dari eksplorasi data hingga evaluasi performa model klasifikasi tanpa penyetelan hiperparameter awal, serta menyertakan contoh implementasi *Hyperparameter Tuning* menggunakan `GridSearchCV`.

## 📌 Gambaran Umum Proyek
Tujuan utama dari proyek ini adalah membangun model klasifikasi prediktif untuk memprediksi apakah seorang penumpang selamat (`Survived = 1`) atau tidak selamat (`Survived = 0`) berdasarkan fitur-fitur seperti kelas kabin, jenis kelamin, usia, jumlah saudara/pasangan, dan tarif tiket.

## 📊 Dataset: Titanic Dataset
Dataset yang digunakan dalam notebook ini adalah dataset **Titanic** (`titanic.csv`). Kolom-kolom utama meliputi:
- `PassengerId`: ID unik penumpang.
- `Survived`: Status keselamatan (0 = Tidak Selamat, 1 = Selamat).
- `Pclass`: Kelas tiket/kabin penumpang (1 = Kelas 1, 2 = Kelas 2, 3 = Kelas 3).
- `Name`: Nama penumpang.
- `Sex`: Jenis kelamin (male, female).
- `Age`: Usia penumpang.
- `SibSp`: Jumlah saudara kandung atau pasangan di atas kapal.
- `Parch`: Jumlah orang tua atau anak di atas kapal.
- `Ticket`: Nomor tiket.
- `Fare`: Tarif perjalanan.
- `Cabin`: Nomor kabin.
- `Embarked`: Pelabuhan keberangkatan (C = Cherbourg, Q = Queenstown, S = Southampton).

## 🛠️ Prasyarat & Pustaka (Libraries)
Notebook ini dikembangkan menggunakan **Python 3** dengan beberapa pustaka standar berikut:
- `pandas` — Untuk manipulasi dan analisis data tabuler.
- `numpy` — Untuk komputasi numerik dan operasi larik (*array*).
- `matplotlib` & `seaborn` — Untuk visualisasi data interaktif dan grafik statistik.
- `scikit-learn` — Menyediakan algoritma klasifikasi, fungsi prapemrosesan data, penyetelan parameter, dan metrik evaluasi.

## 🔄 Alur Kerja Proyek (*Project Workflow*)

### 1. Persiapan Data & Library
Memuat semua modul klasifikasi dan metrik evaluasi dari `scikit-learn`, serta mengimpor dataset latihan utama.

### 2. Exploratory Data Analysis (EDA)
Melakukan pemeriksaan struktur data menggunakan `.info()` dan ringkasan statistik dengan `.describe()`. Selain itu, grafik distribusi statistik digunakan untuk menganalisis hubungan variabel kualitatif terhadap peluang keselamatan (misalnya korelasi jenis kelamin `Sex` terhadap status keselamatan `Survived`).

### 3. Rekayasa Fitur (*Feature Engineering*)
Melakukan pembersihan data (*data cleaning*) termasuk:
- Penanganan nilai yang hilang (*missing values*).
- Transformasi fitur kategorikal menjadi nilai numerik agar dapat diproses oleh model pembelajaran mesin.
- Pemilihan kolom fitur operasional (`X`) dan variabel target (`y`).

### 4. Pelatihan Model & Evaluasi
Mengimplementasikan beberapa algoritma klasifikasi secara sekuensial tanpa tuning parameter awal:
* **Logistic Regression**
* **K-Nearest Neighbors (KNN)**
* **Naive Bayes (GaussianNB)**
* **Decision Tree**

Setiap model dievaluasi menggunakan data uji (*test set*) berdasarkan metrik performa standar:
- **Accuracy Score**
- **Precision, Recall, & F1-Score** (melalui `classification_report`)
- **Confusion Matrix**

### 5. Penyetelan Hiperparameter (*Hyperparameter Tuning*)
Sebagai demonstrasi tingkat lanjut, notebook ini menyediakan bagian khusus untuk mengoptimalkan performa model menggunakan teknik pencarian menyeluruh via `GridSearchCV` (menggunakan model KNN sebagai contoh kasus) untuk menemukan kombinasi parameter terbaik seperti metrik jarak (`metric`) dan jumlah tetangga terdekat (`n_neighbors`).

### 6. Prediksi Data Penumpang Baru
Pada bagian akhir, model terbaik digunakan untuk memprediksi probabilitas keselamatan dari sampel data penumpang baru secara instan.

## 🚀 Cara Menjalankan Proyek
1. Clone atau unduh repositori ini ke dalam direktori lokal Anda.
2. Pastikan file dataset `titanic.csv` berada di direktori yang sama dengan berkas notebook `.ipynb`.
3. Jalankan notebook menggunakan lingkungan Jupyter Notebook, JupyterLab, atau unggah langsung ke Google Colab.
4. Eksekusi sel kode secara berurutan dari atas ke bawah.

---
