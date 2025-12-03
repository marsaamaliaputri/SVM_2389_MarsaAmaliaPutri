# Prediksi Status Kelulusan Mahasiswa Menggunakan Support Vector Machine (SVM)

## Identitas Mahasiswa
**Nama   : Marsa Amalia Putri**  
**NPM    : 2457201002389**
**Mata Kuliah : Machine Learning**  
**Dosen Pengampu : Dr. Dwi Wahyu Prabowo, S.Si., M.Eng**  
**Universitas : Universitas Darwan Ali**  

---

Proyek ini dibuat sebagai tugas UTS Mata Kuliah **Machine Learning**.  
Model yang digunakan adalah **Support Vector Machine (SVM)** untuk memprediksi apakah mahasiswa lulus **TEPAT** atau **TERLAMBAT** berdasarkan data akademik dan demografis.

---

## A. Setup & Load Dataset

Tahapan awal penelitian:
- Menghubungkan Google Colab ke Google Drive  
- Memanggil dataset `datakelulusanmahasiswa.xlsx`  
- Menampilkan 10 data awal  
- Menampilkan struktur dataset  
- Mengecek missing values  

Tujuan: memastikan dataset siap diproses.

---

## B. Exploratory Data Analysis (EDA)

EDA dilakukan untuk memahami karakteristik data.

Yang dilakukan:
- Membersihkan nama kolom agar tidak error  
- Menampilkan statistik deskriptif  
- Membuat visualisasi:
  - Histogram distribusi IPK  
  - Countplot status kelulusan  
  - Boxplot IPK terhadap status kelulusan  

---

## C. Preprocessing

Preprocessing mencakup:
1. Menghapus kolom `NAMA`  
2. Menghapus baris yang memiliki missing value  
3. Label encoding `STATUS KELULUSAN`  
4. Memisahkan fitur X dan label y  
5. One-hot encoding  
6. Scaling menggunakan `StandardScaler`  

Tahap ini penting agar model dapat membaca pola data secara optimal.

---

## D. Training Model SVM + Evaluasi

Pada tahap ini dilakukan:
- Train-test split (80:20)  
- Training model menggunakan `SVC(kernel="linear")`  
- Prediksi data testing  
- Menghasilkan:
  - Akurasi
  - Classification report  
  - Confusion matrix (heatmap)  

---

## E. Interpretasi Model

**Interpretasi akurasi:**  
Akurasi menunjukkan persentase prediksi benar oleh model.

**Interpretasi precision–recall:**  
- Kelas TEPAT biasanya lebih mudah diprediksi karena datanya banyak  
- Kelas TERLAMBAT sedikit lebih sulit (class imbalance)  

**Interpretasi confusion matrix:**  
Sebagian besar prediksi berada pada diagonal → model stabil dan akurat.

---

## F. Kesimpulan

1. Model SVM berhasil melakukan klasifikasi kelulusan mahasiswa dengan performa baik.  
2. Preprocessing meningkatkan performa model secara signifikan.  
3. Model mampu mengenali mahasiswa yang lulus **TEPAT** dengan baik.  
4. Kelas **TERLAMBAT** memiliki performa sedikit lebih rendah karena jumlah data tidak seimbang.  
5. Secara keseluruhan, SVM cocok digunakan pada kasus prediksi kelulusan mahasiswa.

---

## Struktur Repository
