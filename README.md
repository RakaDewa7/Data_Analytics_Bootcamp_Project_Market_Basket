# Dashboard Analisis Groceries Dataset & Market Basket Analysis

## Ringkasan
Membangun dasbor analitik interaktif untuk melakukan analisis keranjang belanja (*Market Basket Analysis*) pada dataset transaksi ritel *groceries*. Proyek ini bertujuan untuk mengidentifikasi pola pembelian konsumen, produk terlaris, serta hubungan antarproduk menggunakan aturan asosiasi (*association rules*) guna mengoptimalkan tata letak toko dan strategi promosi.

## Problem Statement
Banyak perusahaan ritel dan produk yang penjualannya tidak optimal atau mengalami penurunan akibat gagal mengikuti perkembangan tren serta teknologi[cite: 143]. Berdasarkan studi literatur terkait Analisis Data Transaksi menggunakan Market Basket Analysis[cite: 143], penting bagi manajemen toko untuk mengidentifikasi produk terlaris serta produk yang sering dibeli secara bersamaan agar pengelolaan stok dan penataan produk menjadi lebih terarah[cite: 143].

## Data Exploration
* **Sumber Data:** Dataset Groceries (*Groceries dataset.csv*) dari Kaggle[cite: 145].
* **Ukuran Dataset:** 38.765 baris dan 3 kolom[cite: 144].
* **Struktur Kolom Utama:** 
  * `Member_number`: ID unik pelanggan[cite: 145].
  * `Date`: Tanggal pembelian transaksi[cite: 145].
  * `itemDescription`: Deskripsi produk yang dibeli[cite: 145].
* **Tipe Data Awal:** 1 kolom bertipe *integer* dan 2 kolom bertipe *string*[cite: 144].

## Data Preparation & Cleaning
* **Missing Value:** Pengecekan menggunakan Python menunjukkan **tidak terdapat missing value (0%)** pada seluruh kolom[cite: 146].
* **Duplikasi:** Ditemukan 759 data duplikat (1.96%), namun data tersebut **dipertahankan** karena merepresentasikan transaksi ritel wajar di mana pelanggan dapat membeli produk yang sama[cite: 146, 151].
* **Deteksi Outlier:** Pengujian menggunakan *Boxplot* dan metode *IQS (Interquartile Range)* menunjukkan **tidak terdapat outlier (0%)** pada data[cite: 147, 148].
* **Inkonsistensi / Typo:** Pemeriksaan nilai unik (*unique*) pada tanggal dan deskripsi item membuktikan **tidak ada data yang typo**[cite: 149].
* **Transformasi Tipe Data:** Kolom `Date` berhasil dikonversi dari tipe string ke format tanggal standar (*Datetime*)[cite: 150].

## Visualization Output & Dashboard Insights
* **Line Chart (Total Pembelian Pertahun dan Bulan):** Tren pembelian menunjukkan peningkatan dari tahun 2014 hingga 2016, dengan lonjakan signifikan pada Januari 2015 yang mencapai 1.797 transaksi[cite: 152].
* **Treemap Chart (Total Pembelian/Barang):** Produk yang paling sering dibeli didominasi oleh kebutuhan pokok seperti *Whole milk* (2.502), *Rolls/buns* (1.716), *Other vegetables* (1.698), *Soda* (1.514), dan *Yogurt* (1.334)[cite: 153].
* **Bar Chart (Total Pembelian yang Terkuat / Association Rules):** Menampilkan aturan asosiasi terkuat, contohnya konsumen yang membeli *yogurt, other vegetables, dan rolls/buns* memiliki peluang 1,43x lebih tinggi (*Lift 1.4336*) untuk membeli *whole milk* dengan tingkat kepercayaan (*Confidence*) mencapai 65,69%[cite: 154].

## Conclusion
* Penjualan produk ritel menunjukkan tren positif yang stabil dan dipengaruhi oleh pola kebutuhan pokok konsumen[cite: 152, 153].
* Analisis keranjang belanja berhasil memetakan produk-produk yang memiliki korelasi tinggi untuk dibeli secara bersamaan, memberikan wawasan mendalam bagi strategi penataan produk[cite: 154].

## Recommendation
* **Optimalisasi Rantai Pasok:** Perusahaan perlu meningkatkan pasokan produk-produk teratas seperti *whole milk, vegetables,* dan *rolls/buns* menjelang bulan-bulan puncak untuk mencegah kehabisan stok (*out-of-stock*)[cite: 156].
* **Strategi Promosi Bundling:** Membuat paket promosi atau potongan harga khusus untuk pembelian kombinasi *yogurt, rolls/buns, other vegetables,* dan *whole milk* guna menaikkan nilai rata-rata transaksi per pelanggan[cite: 156].
* **Tata Letak Toko (*Store Layout*):** Menempatkan produk-produk kebutuhan pokok yang sering dibeli bersamaan (seperti *yogurt, rolls/buns,* dan *other vegetables*) pada posisi yang berdekatan dengan *whole milk* agar lebih mudah dijangkau oleh konsumen[cite: 156].

## Tools yang Digunakan
Tableau (Dashboard Interaktif) · Python (Pandas, IQR, Data Cleaning) · Market Basket Analysis (Association Rules) · Exploratory Data Analysis (EDA)

---
*Bagian dari Portofolio Graphic Design & Data Analytics Career Accelerator — Tempat Belajar (2026)*[cite: 135]  
*Disusun oleh: Raka Dewa Dipamahahesa Arsandy*[cite: 134]
