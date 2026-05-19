# Machine Learning Week 8: Unsupervised Learning

Repository ini berisi materi perkuliahan Minggu 8 untuk Program Studi **D4 Teknik Robotika (Robotics Engineering)** di **Politeknik Negeri Batam**. Materi berfokus pada konsep dasar dan implementasi praktis dari *Unsupervised Learning*.

## 📋 Daftar Isi Materi
1. **Introduction to Unsupervised Learning**
   - Perbedaan mendasar antara *Supervised* vs *Unsupervised Learning*.
   - Konsep belajar mandiri tanpa label data.
2. **Dimensionality Reduction**
   - **PCA (Principal Component Analysis)**: Konsep, langkah-langkah, dan reduksi dimensi data.
3. **Clustering**
   - **K-Means Clustering**: Pengelompokkan data berdasarkan jarak pusat klaster (centroid).
   - **DBSCAN**: Klasterisasi berbasis kepadatan data (*density-based*) dan deteksi *outlier* secara otomatis.
4. **Model Evaluation**
   - **Elbow Method**: Menentukan jumlah klaster ($k$) optimal menggunakan grafik WCSS.
   - **Silhouette Score**: Validasi kualitas performa klaster (rentang nilai -1 hingga +1).

## 🛠️ Tech Stack & Library
- **Python**
- **scikit-learn** (untuk implementasi PCA, K-Means, dan DBSCAN)
- **Matplotlib / Seaborn** (untuk visualisasi grafik evaluasi)

## 📚 Buku Teks & Referensi Utama
- Bishop, C.M. (2006). *Pattern Recognition and Machine Learning*. Springer.
- Géron, A. (2022). *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow*. O'Reilly.
- James, G. et al. (2021). *An Introduction to Statistical Learning*. Springer.
- Dokumentasi Resmi `scikit-learn`.
