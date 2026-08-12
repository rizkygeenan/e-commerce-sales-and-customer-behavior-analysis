# 🛍️ E-Commerce Sales & Customer Behavior Analysis

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![Matplotlib & Seaborn](https://img.shields.io/badge/Visualization-Matplotlib%20%7C%20Seaborn-green.svg)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📖 Table of Contents
1. [Project Overview & Objectives](#-project-overview--objectives)
2. [Dataset Overview](#-dataset-overview)
3. [Key Steps & Exploratory Data Analysis (EDA)](#-key-steps--exploratory-data-analysis-eda)
4. [Key Insights & Business Recommendations](#-key-insights--business-recommendations)
5. [How to Run / Installation Guide](#-how-to-run--installation-guide)
6. [Project Structure](#-project-structure)
7. [Author & Acknowledgments](#-author--acknowledgments)

---

## 🎯 1. Project Overview & Objectives

Proyek ini bertujuan untuk menganalisis data transaksi penjualan e-commerce guna menggali wawasan strategis (*actionable insights*) terkait perilaku pelanggan dan performa penjualan. 

**Tujuan Utama Analisis:**
* **Memahami Tren Penjualan:** Mengidentifikasi pola transaksi berdasarkan waktu (hari dan bulan) untuk mengetahui periode puncak (*peak season*) bisnis.
* **Analisis Pendapatan:** Menghitung total pendapatan (*revenue*) dan distribusi pembelian per transaksi maupun produk.
* **Korelasi Variabel:** Menganalisis hubungan antara kuantitas produk, harga satuan (*unit price*), dan total nilai transaksi.
* **Segmentasi Perilaku Pelanggan:** Mengetahui pola pembelian pelanggan berdasarkan ID unik dan wilayah geografis/negara asal transaksi.

---

## 📊 2. Dataset Overview

Dataset yang digunakan berisi catatan transaksi e-commerce dengan total **4.870 baris** dan **8 kolom awal**.

### Skema Kolom Dataset
| Nama Kolom | Tipe Data | Deskripsi / Penjelasan |
| :--- | :--- | :--- |
| `InvoiceNo` | Object / String | Nomor unik faktur atau transaksi |
| `StockCode` | Object / String | Kode unik pengenal barang/produk |
| `Description` | Object / String | Nama atau deskripsi lengkap produk |
| `Quantity` | Integer | Jumlah barang yang dibeli per transaksi |
| `InvoiceDate` | Datetime | Tanggal dan waktu terjadinya transaksi |
| `UnitPrice` | Float | Harga satuan produk |
| `CustomerID` | Float / String | ID unik identifikasi pelanggan |
| `Country` | Object / String | Negara tempat transaksi dilakukan |

> **Catatan Kebersihan Data (*Data Cleanliness*):** Dataset berada dalam kondisi yang sangat bersih dengan **0 nilai kosong (*missing values*)** dan **0 data duplikat**, sehingga siap untuk langsung diolah ke tahap *feature engineering*.

---

## 🔍 3. Key Steps & Exploratory Data Analysis (EDA)

Proses pengolahan data melalui beberapa tahapan utama:
1. **Data Cleaning & Understanding:** Memuat dataset, memvalidasi tipe data, serta memastikan tidak ada anomali atau data duplikat.
2. **Feature Engineering:** 
   * Konversi kolom `InvoiceDate` menjadi format *datetime* terstruktur, serta mengekstrak informasi tambahan berupa `year`, `month`, dan `day_name`.
   * Pembuatan kolom baru `total_price` yang dihitung dari perkalian `Quantity` $\times$ `UnitPrice`.
3. **Multivariate Analysis & Correlation:** Menganalisis korelasi antar variabel numerik (seperti hubungan antara harga satuan, jumlah barang yang dibeli, dan total pendapatan) menggunakan matriks korelasi dan visualisasi *seaborn heatmap*.

---

## 💡 4. Key Insights & Business Recommendations

### 🔑 Temuan Penting (*Key Insights*):
* **Pola Waktu Transaksi:** Terdapat hari-hari tertentu dalam seminggu yang menunjukkan lonjakan volume transaksi signifikan, mencerminkan kebiasaan belanja mingguan pelanggan.
* **Distribusi Pendapatan:** Sebagian besar transaksi didominasi oleh pembelian kuantitas menengah dengan variasi harga produk yang kompetitif.
* **Korelasi Harga & Kuantitas:** Analisis menunjukkan bagaimana penyesuaian harga satuan berdampak langsung terhadap total nilai penjualan per transaksi.

### 📈 Rekomendasi Strategis (*Business Recommendations*):
* **Optimasi Stok & Promosi Berjadwal:** Jalankan kampanye diskon atau *flash sale* khusus pada hari-hari yang terbukti memiliki volume transaksi paling tinggi untuk memaksimalkan *revenue*.
* **Personalisasi Pelanggan:** Manfaatkan data `CustomerID` untuk membuat program loyalitas (*loyalty program*) bagi pelanggan dengan frekuensi belanja tertinggi.
* **Strategi Bundling Produk:** Tawarkan *bundling* produk untuk barang-barang yang sering dibeli bersamaan guna meningkatkan rata-rata nilai transaksi (*average order value*).

---

## 🚀 Cara Menjalankan
Anda dapat menjalankan kode ini dengan dua cara:

### 1. Google Colab
*    Klik file .ipynb yang ada di repositori ini atau link berikut https://colab.research.google.com/drive/18RyKawKNKPYh7VxFXFcW_GBNygRV8TUx?usp=sharing.
*    Klik tombol "Open in Colab" jika tersedia, atau unggah file tersebut ke Google Colab.

### 2. Lokal
*    Pastikan Anda telah menginstal Python.
*    Instal Jupyter Notebook dengan perintah: pip install notebook.
*    Buka terminal, arahkan ke direktori file, dan jalankan perintah: jupyter notebook.

## 📁 6. Project Structure
Struktur direktori repository ini disusun sebagai berikut:
```bash
ecommerce-sales-analysis/
│
├── data/
│   └── ecommerce.csv            # Dataset utama e-commerce
│
├── notebooks/
│   └── e_commerce_analysis.ipynb # Jupyter Notebook berisi proses EDA & pemodelan
│
├── outputs/
│   └── figures/                 # Hasil visualisasi grafik (PNG/JPG)
│
├── README.md                    # Dokumentasi proyek
└── requirements.txt             # Daftar pustaka / dependencies Python
```
