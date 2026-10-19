# 🫀 Klasifikasi Penerapan Machine Learning untuk Deteksi Dini Risiko Penyakit Jantung

Proyek ini bertujuan untuk membangun model *Machine Learning* yang mampu mendeteksi secara dini risiko penyakit jantung pada pasien berdasarkan indikator klinis kesehatan.

---

## 📌 1. Masalah (Problem Statement)
Penyakit jantung merupakan salah satu penyebab kematian tertinggi di dunia. Diagnosis medis yang terlambat atau tidak akurat dapat berisiko fatal bagi pasien. Dalam dunia medis, mengidentifikasi risiko penyakit jantung secara manual membutuhkan analisis kompleks terhadap berbagai indikator klinis. Oleh karena itu, diperlukan sistem berbasis *Machine Learning* yang dapat membantu mendeteksi risiko ini secara cepat, objektif, dan akurat berdasarkan rekam medis pasien.

---

## 🛠️ 2. Proses (Workflow & Methodology)

Proyek ini menggunakan **Heart Disease Cleveland Dataset** (303 baris data dan 14 atribut/fitur) dengan tahapan pengerjaan sebagai berikut:

1. **Eksplorasi & Pembersihan Data (*Data Exploration*)**:
   - Memeriksa struktur data, tipe data, serta memastikan tidak terdapat *missing values*.
2. **Pemisahan Fitur & Target**:
   - Fitur (X): Indikator medis seperti usia, tekanan darah, kadar kolesterol, detak jantung maksimum, dll.
   - Target (y): Status risiko penyakit jantung (0 = Sehat, 1 = Berisiko/Sakit).
3. **Pembagian Data (*Data Splitting*)**:
   - Membagi data menjadi 80% untuk *Training Set* dan 20% untuk *Testing Set*.
4. **Standarisasi Fitur (*Feature Scaling*)**:
   - Menggunakan `StandardScaler` untuk menyamakan skala seluruh fitur numerik agar proses pelatihan model berjalan adil dan optimal.
5. **Pelatihan Model (*Model Training*)**:
   - Membandingkan dua algoritma klasifikasi: **Logistic Regression** dan **Random Forest Classifier**.

---

## 💡 3. Solusi & Hasil Evaluasi (Solution & Results)

Sistem membandingkan performa kedua algoritma pada data uji (*testing data*):

### 📊 Perbandingan Akurasi Model
- **Logistic Regression**: Akurasi sebesar **86.9%**
- **Random Forest Classifier**: Akurasi sebesar **88.5%**

Model **Random Forest Classifier** terpilih sebagai solusi terbaik karena memberikan akurasi yang lebih tinggi dalam mendiagnosis status pasien.

### 🔍 Evaluasi Detail (Confusion Matrix - Random Forest)
Dari total 61 data uji pasien, performa model Random Forest adalah sebagai berikut:
- **54 Pasien (88.5%) Terprediksi Akurat**:
  - **27 pasien sehat** berhasil diprediksi **Sehat** secara tepat.
  - **27 pasien sakit** berhasil diprediksi **Sakit** secara tepat.
- **7 Pasien Terprediksi Meleset**:
  - 6 pasien sehat diprediksi sakit (*False Positive*).
  - 1 pasien sakit diprediksi sehat (*False Negative*).

---

## 🚀 Kesimpulan
Model klasifikasi **Random Forest** terbukti efektif dan dapat diandalkan sebagai alat bantu keputusan (*decision support system*) bagi tenaga medis dalam melakukan skrining awal risiko penyakit jantung secara lebih akurat.

---
Data Mining: Classification
