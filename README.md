# 📊 Adidas Sales Analysis & Prediction

Proyek analisis data penjualan Adidas yang mencakup pembersihan data, eksplorasi data, visualisasi, dan prediksi penjualan menggunakan Prophet untuk forecasting Total Sales dan Operating Profit.

## 📋 Deskripsi Proyek

Proyek ini menganalisis data penjualan Adidas dari berbagai retailer, region, dan produk. Analisis mencakup data cleaning, exploratory data analysis (EDA), dan prediksi penjualan untuk masa depan menggunakan model Prophet.

## 🎯 Tujuan

-   Melakukan data cleaning dan preprocessing pada dataset penjualan Adidas
-   Menganalisis pola penjualan berdasarkan berbagai dimensi (retailer, region, produk, musim, dll)
-   Membangun model prediksi untuk Total Sales dan Operating Profit
-   Memberikan insights bisnis untuk strategi penjualan

## 📊 Dataset

Dataset berisi informasi penjualan Adidas dengan kolom-kolom berikut:

-   **Retailer**: Bisnis atau individu yang menjual produk Adidas
-   **Retailer ID**: ID unik untuk setiap retailer
-   **Invoice Date**: Tanggal transaksi penjualan
-   **Region**: Wilayah geografis (West, Northeast, South, Southeast, Midwest)
-   **State**: Negara bagian tempat penjualan
-   **City**: Kota tempat penjualan
-   **Product**: Kategori produk Adidas
-   **Price per Unit**: Harga per unit produk
-   **Units Sold**: Jumlah unit yang terjual
-   **Total Sales**: Total pendapatan penjualan
-   **Operating Profit**: Keuntungan operasional
-   **Sales Method**: Metode penjualan (Online, Outlet, In-store)

## 🛠️ Teknologi yang Digunakan

-   **Python 3.x**
-   **Pandas**: Manipulasi dan analisis data
-   **NumPy**: Operasi numerik
-   **Matplotlib & Seaborn**: Visualisasi data
-   **Prophet**: Time series forecasting
-   **gdown**: Download data dari Google Drive
-   **scikit-learn**: Evaluasi metrik model

## 📁 Struktur Proyek

```
BD-Adidas-Sales/
│
├── Big Data (D)_Kelompok 1_adidas-sales.ipynb  # Notebook utama analisis
├── predicted_data_sales_profit.csv              # Hasil prediksi
└── README.md                                     # Dokumentasi proyek
```

## 🚀 Cara Menjalankan

### Prerequisites

```bash
pip install pandas numpy matplotlib seaborn gdown prophet scikit-learn
```

### Menjalankan Notebook

1. Clone repository ini:

```bash
git clone https://github.com/rai-pramana/BD-Adidas-Sales.git
cd BD-Adidas-Sales
```

2. Buka Jupyter Notebook:

```bash
jupyter notebook "Big Data (D)_Kelompok 1_adidas-sales.ipynb"
```

3. Jalankan semua cell secara berurutan

## 🔍 Proses Analisis

### 1. Data Loading & Preprocessing

-   Download dataset dari Google Drive
-   Handling missing values
-   Penghapusan kolom yang tidak diperlukan (Retailer ID)
-   Konversi tipe data (Invoice Date ke datetime)
-   Feature engineering (ekstraksi Month, Year, Day, Season)

### 2. Data Cleaning

-   Memperbaiki inkonsistensi pada kolom Product ("Men's aparel" → "Men's Apparel")
-   Menghapus simbol $ dan koma dari kolom numerik
-   Konversi tipe data numerik
-   Menghapus rows dengan Units Sold = 0
-   Koreksi nilai Total Sales dan Operating Profit

### 3. Exploratory Data Analysis (EDA)

#### Bivariate Analysis:

-   **Retailer**: West Gear (27%) dan Foot Locker (24%) adalah retailer teratas
-   **Region**: West (30%) dan Northeast (21%) memiliki penjualan tertinggi
-   **Product**: Men's Street Footwear, Women's Apparel, dan Men's Athletic Footwear (60% dari total sales)
-   **Season**: Summer (29%) dan Winter (24%) memiliki penjualan tertinggi
-   **Sales Method**: Online (37%) dan Outlet (33%) adalah metode penjualan utama
-   **Year Trend**: Penjualan 2021 jauh lebih tinggi dibanding 2020 (dampak COVID-19)

#### Multivariate Analysis:

-   Analisis korelasi antar variabel numerik
-   Pairplot untuk melihat hubungan antar variabel
-   Heatmap korelasi

### 4. Prediksi dengan Prophet

-   Model dikembangkan untuk setiap kombinasi Sales Method, Region, Retailer, dan Product
-   Prediksi untuk 60 periode ke depan (5 tahun)
-   Prediksi mencakup Total Sales dan Operating Profit
-   Adjustment untuk memastikan prediksi Total Sales tidak negatif

### 5. Evaluasi Model

Metrik evaluasi pada data historis:

-   **Mean Absolute Error (MAE)** untuk Total Sales dan Operating Profit
-   **Root Mean Squared Error (RMSE)** untuk Total Sales dan Operating Profit

## 📈 Hasil Utama

1. **Top Performers**:

    - Retailer: West Gear, Foot Locker
    - Region: West, Northeast
    - Products: Men's Street Footwear, Women's Apparel

2. **Seasonal Patterns**:

    - Penjualan meningkat di Summer dan Winter
    - Kemungkinan terkait musim sekolah dan liburan

3. **Sales Channel**:

    - Online menjadi metode penjualan teratas (37%)
    - Tren shift ke digital commerce

4. **Growth Trend**:
    - Pemulihan signifikan dari 2020 ke 2021 pasca-COVID
    - Prediksi menunjukkan trend positif untuk periode mendatang

## 📄 Output

File `predicted_data_sales_profit.csv` berisi:

-   Invoice Date (prediksi)
-   Sales Method
-   Region
-   Retailer
-   Product
-   Predicted Total Sales
-   Predicted Operating Profit

## 📝 Lisensi

Proyek ini dibuat untuk keperluan akademis/pembelajaran.

## 🔗 Link Repository

[https://github.com/rai-pramana/BD-Adidas-Sales](https://github.com/rai-pramana/BD-Adidas-Sales)

---

**Note**: Dataset asli diunduh dari Google Drive. Pastikan memiliki koneksi internet untuk menjalankan bagian download data.
