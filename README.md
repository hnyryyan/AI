# Tugas Praktikum AI Regresi dan Klasifikasi

Repositori ini berisi hasil praktikum penerapan AI menggunakan Python. Terdapat empat model utama yang dieksplorasi: Regresi Linear Sederhana, Regresi Linear Berganda, Regresi Logistik, dan K-Nearest Neighbors (KNN). 


---

## 1. Regresi Linear Sederhana
- **Skenario Data:** Memprediksi jumlah **Penjualan** berdasarkan **Biaya Iklan** yang dikeluarkan.
- **Variabel:** - Independen (X): Biaya Iklan (Juta Rupiah)
  - Dependen (Y): Penjualan (Unit)
- **Hasil & Interpretasi:** Dari model yang dilatih, diperoleh nilai koefisien sebesar **2.73**. Nilai positif ini mengindikasikan hubungan yang searah; artinya setiap penambahan biaya iklan sebesar 1 Juta Rupiah akan meningkatkan penjualan rata-rata sebanyak **2.73** unit.
- **Evaluasi Model:** Nilai *Mean Absolute Error* (MAE) yang didapatkan adalah **1.50**. Angka ini menunjukkan bahwa rata-rata kesalahan tebakan model dibandingkan data aktual hanya meleset sebesar **1.50** unit.
- **Kesimpulan:** Model ini cukup baik dan membuktikan bahwa biaya iklan sangat efektif untuk mendongkrak angka penjualan perusahaan.

---

## 2. Regresi Linear Berganda
- **Skenario Data:** Memprediksi **Harga Rumah** berdasarkan beberapa spesifikasi fisik bangunan.
- **Variabel:**
  - Independen (X): Luas Tanah (m2), Jumlah Kamar, Usia Bangunan (Tahun)
  - Dependen (Y): Harga Rumah (Ratus Juta Rupiah)
- **Hasil & Interpretasi:** Berdasarkan koefisien regresi `[0.023, 0.895, -0.074]`, fitur yang paling memberikan pengaruh positif terhadap kenaikan harga rumah adalah **Jumlah Kamar** (koefisien 0.895). Sebaliknya, fitur **Usia Bangunan** memiliki bobot negatif (-0.074), yang sangat logis karena semakin tua bangunan, harganya cenderung menurun.
- **Evaluasi Model:** Model ini menghasilkan nilai *Root Mean Squared Error* (RMSE) sebesar **0.60**, yang berarti rata-rata penyimpangan prediksi harga rumah dari harga aktualnya adalah sekitar **60 Juta Rupiah** (0.60 x 100 Juta).

---

## 3. Regresi Logistik
- **Skenario Data:** Model klasifikasi biner untuk menentukan apakah pengajuan **Kredit Disetujui** atau **Ditolak**.
- **Variabel:**
  - Independen (X): Gaji Bulanan, Skor Kredit
  - Dependen (Y): Status Disetujui (1 = Ya, 0 = Tidak)
- **Hasil & Evaluasi:** Model ini berhasil mengklasifikasikan data pengajuan kredit dengan tingkat Akurasi sebesar **1.0 (100%)**. 
- **Kesimpulan:** Dengan menggunakan Gaji Bulanan dan Skor Kredit, model mampu memetakan pola status pengajuan dengan sempurna pada data *testing*. Hal ini membantu bank atau lembaga keuangan dapat mengotomatisasi keputusan penerimaan kredit dengan tingkat kepercayaan yang tinggi.

---

## 4. Klasifikasi K-Nearest Neighbors (KNN)
- **Skenario Data:** Menggunakan dataset publik **Social Network Ads** untuk memprediksi apakah seorang pengguna akan **Membeli Produk** setelah melihat iklan di media sosial.
- **Variabel:**
  - Independen (X): *Age* (Umur) dan *Estimated Salary* (Estimasi Gaji)
  - Dependen (Y): *Purchased* (1 = Membeli, 0 = Tidak)
- **Preprocessing:** Mengingat KNN bekerja berdasarkan perhitungan jarak (*Euclidean Distance*), fitur *Age* dan *Estimated Salary* wajib melalui tahap normalisasi menggunakan `StandardScaler` agar tidak ada fitur yang mendominasi perhitungan hanya karena rentang skalanya lebih besar. Parameter tetangga terdekat yang digunakan adalah **K = 5**.
- **Hasil & Evaluasi:** Model klasifikasi KNN mendapatkan Akurasi sebesar **0.93 (93%)** pada data pengujian.
- **Kesimpulan:** Algoritma KNN sangat responsif dan akurat dalam memetakan pola segmentasi pengguna berdasarkan umur dan pendapatan untuk menentukan target *marketing* yang tepat.
