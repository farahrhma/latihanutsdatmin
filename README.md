# Prediksi Performa Mahasiswa

## Pendahuluan
Dalam era digital, analisis data menjadi hal penting dalam memahami pola serta mendukung pengambilan keputusan berbasis data. Pada studi kasus ini dilakukan analisis terhadap dataset performa siswa untuk memprediksi apakah seorang siswa tergolong Baik atau Tidak Baik.

Dataset yang digunakan berisi berbagai variabel, antara lain:
1) Data demografi (jenis kelamin, usia, alamat)
2) Latar belakang keluarga (pendidikan dan pekerjaan orang tua)
3) Kebiasaan belajar (waktu belajar, aktivitas, absensi)
4) Nilai akademik (G1, G2, G3)

Variabel utama yang digunakan sebagai acuan adalah nilai akhir (G3), yang kemudian dikategorikan menjadi:
- Baik → jika G3 ≥ 10
- Tidak Baik → jika G3 < 10

## Tujuan utama:
Membangun model machine learning yang mampu memprediksi performa siswa pada data baru yang belum memiliki label.

# Data Understanding & Visualisasi
Tahap awal dilakukan eksplorasi data untuk memahami karakteristik dataset.
Langkah yang dilakukan:
1) Melihat distribusi label performa
2) Visualisasi korelasi antar variabel numerik menggunakan heatmap
  
Hasil:
1) Jumlah data kategori: Baik (265 data) dan Tidak Baik (130 data)
2) Variabel G1 dan G2 memiliki korelasi tinggi terhadap G3
3) Data relatif seimbang sehingga cocok untuk pemodelan

# Data Preprocessing
Langkah yang dilakukan:
1) Mengubah nilai G3 menjadi label kategori (Baik / Tidak Baik)
2) Menghapus variabel G3 dari fitur untuk menghindari data leakage
3) Encoding variabel kategorikal menggunakan LabelEncoder
4) Normalisasi data menggunakan StandardScaler
5) Pembagian data menjadi data training dan validasi

# Clustering (K-Means)
Clustering digunakan untuk menemukan pola pengelompokan alami dalam data tanpa menggunakan label.
Hasil:
1) Data terbagi menjadi 2 cluster: Cluster 1 (239 data) dan Cluster 0 (156 data)
2) Terdapat pola pengelompokan siswa berdasarkan karakteristik tertentu
3) Cluster tertentu cenderung memiliki performa yang lebih baik

# Klasifikasi
Model klasifikasi memberikan akurasi yang baik
Dilakukan perbandingan beberapa model klasifikasi:
1) Logistic Regression: 93.67%
2) Decision Tree: 89.87%
3) Random Forest: 89.87%
4) KNN: 72.15%

Hasil:
1) Model terbaik: Logistic Regression
2) Akurasi: ±94%
   
Model mampu memprediksi performa siswa dengan sangat baik berdasarkan fitur yang tersedia.

# Regresi
Regresi digunakan untuk memprediksi nilai asli G3 sebagai variabel numerik.
Hasil:
1) MSE: 5.03
2) R²: 0.75
3) Model mampu menjelaskan sekitar 75% variasi nilai G3
4) Terdapat hubungan yang cukup kuat antara variabel input dengan nilai akhir

# Prediksi Data Baru
Model terbaik digunakan untuk memprediksi dataset test (tanpa label Y).
Data berhasil diklasifikasikan menjadi:
1) Baik
2) Tidak Baik
Model menunjukkan kemampuan generalisasi yang baik terhadap data baru.

# Kesimpulan
1) Nilai akhir (G3) sangat dipengaruhi oleh nilai sebelumnya (G1 dan G2).
2) Faktor lain seperti kebiasaan belajar dan kondisi keluarga juga berpengaruh
3) Model Logistic Regression memberikan performa terbaik
4) Model regresi menunjukkan hubungan yang kuat antar variabel
5) Model yang dibangun mampu digunakan untuk prediksi data baru

Siswa dengan nilai awal yang baik serta kebiasaan belajar yang konsisten cenderung memiliki performa akhir yang lebih tinggi.
