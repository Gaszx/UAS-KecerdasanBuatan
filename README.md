# UAS-KecerdasanBuatan

# 🎯 Proyek AI: Prediksi Ketertarikan Nasabah terhadap Produk Perbankan

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk membangun model kecerdasan buatan berbasis **Random Forest Classifier** guna memprediksi apakah seorang nasabah tertarik atau tidak terhadap penawaran produk perbankan, berdasarkan data historis kampanye pemasaran.

Model ini dibangun menggunakan dataset *Bank Marketing* dari [data.world](https://data.world/xprizeai-ai/bank-marketing), dan dikembangkan menggunakan Python serta pustaka *scikit-learn*, *pandas*, *matplotlib*, dan *seaborn*.

---

## 📂 Struktur Langkah Pengerjaan

### 1. **Data Understanding**
- Dataset terdiri dari 17 atribut (numerik dan kategorikal) serta target `y` (yes/no).
- Data tidak memiliki nilai kosong atau duplikat.
- Dataset imbalanced: mayoritas nasabah menolak penawaran.

### 2. **Data Preparation**
- **Encoding:**
  - Label Encoding dilakukan pada kolom target `y` (yes=1, no=0).
  - One-Hot Encoding diterapkan pada kolom kategorikal seperti `job`, `marital`, `education`.
- **Normalisasi:**
  - Menggunakan `StandardScaler` untuk kolom numerik.
- **Split Data:**
  - 80% data untuk training, 20% untuk testing.
  - `stratify=y` digunakan agar proporsi kelas seimbang dalam pembagian.

### 3. **Modeling**
- Algoritma yang digunakan: **Random Forest Classifier**
- Dilatih dengan `X_train` dan `y_train`
- Dievaluasi menggunakan `X_test` dan `y_test`

### 4. **Evaluasi Model**
- Evaluasi dilakukan dengan:
  - Confusion Matrix
  - Accuracy, Precision, Recall, F1-Score
- Visualisasi:
  - Heatmap Confusion Matrix
  - Bar chart evaluasi metrik
  - Visualisasi pohon keputusan (Decision Tree)

### 5. **Exploratory Data Analysis (EDA)**
- Visualisasi distribusi fitur numerik
- Korelasi antar fitur (Heatmap)
- Deteksi kelas tidak seimbang
- Insight penting:
  - Durasi kontak sangat memengaruhi keputusan nasabah.
  - Riwayat kontak sebelumnya juga signifikan.

---

## 📊 Hasil Evaluasi
| Metrik     | Nilai  |
|------------|--------|
| Accuracy   | 90%    |
| Precision  | 65%    |
| Recall     | 40%    |
| F1-Score   | 49%    |

Model cukup baik dalam mengenali kelas mayoritas, namun perlu perbaikan lebih lanjut (misalnya menggunakan teknik oversampling) untuk menangani data imbalanced agar recall meningkat.

---

## 📚 Referensi
- Ramadhan, M. I. (2021). *Prediksi penerimaan produk perbankan menggunakan machine learning*. Jurnal Teknologi dan Sistem Informasi, 2(1), 1–10. https://jurnal.itny.ac.id/index.php/JTSI/article/view/8163  
- Wijayanti, F. D., & Hidayat, R. (2018). *Strategi promosi perbankan dengan analisis data mining*. JUKATIK, 16(2), 86–94. https://media.neliti.com/media/publications/586486-strategi-promosi-perbankan-dengan-analis-0502b3af.pdf  
- Panggabean, I. M. (2022). *Analisis prediksi kelayakan nasabah kredit menggunakan algoritma Random Forest menggunakan PEGA dan WEKA*. JUKOMIKA, 5(2), 78–90. https://jurnal.ikhafi.or.id/index.php/jukomika/article/view/2813  
- Religia, Y., Nugroho, A., & Hadikristanto, W. (2021). *Analisis perbandingan algoritma optimasi pada Random Forest untuk klasifikasi data bank marketing*. Jurnal RESTI, 5(1), 187–192. https://doi.org/10.29207/resti.v5i1.2813

---

## 👨‍💻 Pengembang
- Bagas Sujiwo (2306018)  
- Romy Zaenul Alam (2306019)  

