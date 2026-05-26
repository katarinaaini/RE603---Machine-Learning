# WineQT K-Means Clustering

Project ini berisi implementasi **Unsupervised Learning** menggunakan algoritma **K-Means Clustering** pada dataset **WineQT**.

## 📌 Deskripsi Project

Notebook ini dibuat untuk melakukan proses clustering terhadap data karakteristik wine menggunakan metode K-Means. Analisis dilakukan mulai dari preprocessing data, exploratory data analysis (EDA), feature engineering, hingga evaluasi hasil clustering menggunakan Silhouette Score dan visualisasi cluster.

---

## 📂 Isi Project

### 1. Prepare
Tahap persiapan environment dan import library:
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

---

### 2. Load Our Dataset
Dataset WineQT dibaca menggunakan pandas dan dilakukan pengecekan:
- struktur data
- jumlah data
- tipe data
- missing value

---

### 3. Exploratory Data Analysis (EDA)
Analisis awal dataset meliputi:
- statistik deskriptif
- distribusi quality wine
- correlation heatmap
- analisis hubungan antar fitur

---

### 4. Feature Engineering
Tahapan preprocessing data:
- menghapus duplicate
- menghapus kolom ID
- menentukan feature dan label
- feature scaling menggunakan StandardScaler

---

### 5. K-Means Clustering
Implementasi algoritma K-Means untuk melakukan pengelompokan data wine berdasarkan kemiripan karakteristik fitur.

---

### 6. Metode Elbow
Digunakan untuk menentukan jumlah cluster optimal dengan melihat nilai inertia pada beberapa jumlah cluster.

---

### 7. Bandingkan Dengan Label Anotator
Hasil cluster dibandingkan secara visual dengan label quality asli dari dataset.

---

### 8. Via Score Plot
Evaluasi clustering menggunakan Silhouette Score untuk mengukur kualitas cluster.

---

### 9. Evaluasi K-Means Menggunakan Visualisasi
Visualisasi silhouette plot digunakan untuk melihat:
- kepadatan cluster
- pemisahan antar cluster
- kualitas tiap cluster

---

## 🛠️ Teknologi yang Digunakan

- Python
- Jupyter Notebook
- Scikit-Learn
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## 📊 Dataset

Dataset yang digunakan:
- WineQT Dataset

Berisi karakteristik kimia wine seperti:
- alcohol
- acidity
- sulphates
- pH
- density
- dan fitur lainnya

---

## 🚀 Cara Menjalankan

1. Clone repository ini
2. Install dependency yang dibutuhkan
3. Jalankan Jupyter Notebook

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Kemudian jalankan:

```bash
jupyter notebook
```

---

## 📁 Struktur File

```bash
├── WineQT.csv
├── wine_dataset.ipynb
└── README.md
```

---

## 📌 Hasil

- Clustering berhasil dilakukan menggunakan K-Means
- Jumlah cluster optimal diperoleh menggunakan Elbow Method
- Evaluasi silhouette menunjukkan kualitas clustering yang cukup baik

---

