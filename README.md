# Prediksi Performa Mahasiswa

## Pendahuluan
Dalam era digital, analisis data menjadi hal penting dalam memahami pola dan mengambil keputusan. Pada studi kasus ini, dilakukan analisis terhadap data mahasiswa untuk memprediksi apakah performa mahasiswa tergolong Baik atau Tidak Baik.

Dataset terdiri dari beberapa variabel seperti:
1) Jam belajar
2) Penghasilan orang tua
3) Aktivitas akademik
4) dan variabel lainnya

## Tujuan utama:
Membangun model yang mampu memprediksi performa mahasiswa pada data baru yang belum memiliki label.

# Data Understanding & Visualisasi
Visualisasi membantu memahami pola awal data
Dilakukan eksplorasi data menggunakan:
1) Distribusi label
2) Heatmap korelasi
  
Insight:
1) Terdapat hubungan antar fitur tertentu dengan performa
2) Data cukup seimbang antar kelas

# Data Preprocessing
Langkah yang dilakukan:
1) Encoding data kategorikal
2) Normalisasi menggunakan StandardScaler
3) Split data training dan validasi

# Clustering (K-Means)
Clustering menunjukkan adanya pengelompokan alami
Clustering digunakan untuk melihat pola alami dalam data tanpa label.
Hasil:
1) Data terbagi menjadi 2 cluster
2) Cluster tertentu cenderung memiliki performa lebih baik

Menunjukkan adanya pola tersembunyi dalam data mahasiswa

# Klasifikasi
Model klasifikasi memberikan akurasi yang baik
Digunakan beberapa model:
1) Logistic Regression
2) Decision Tree
3) Random Forest
4) KNN

Hasil:
1) Model terbaik
2) Akurasi
   
Model mampu memprediksi performa dengan cukup baik.

# Regresi
Regresi digunakan untuk melihat hubungan antar variabel numerik.
Hasil:
1) Nilai R² menunjukkan bahwa model mampu menjelaskan hubungan antar variabel dengan cukup baik
2) Variabel tertentu memiliki pengaruh signifikan

# Prediksi Data Baru
Model terbaik digunakan untuk memprediksi dataset test (tanpa label Y).
Data berhasil diklasifikasikan menjadi:
1) Baik
2) Tidak Baik

# Kesimpulan
Nilai akhir (G3) sangat dipengaruhi oleh nilai sebelumnya (G1 dan G2), serta faktor seperti waktu belajar dan dukungan keluarga. Model Random Forest memberikan performa terbaik dalam mengklasifikasikan siswa.
