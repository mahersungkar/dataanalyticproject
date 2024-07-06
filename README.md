# Marketing Analytics Exploratory/Statistical Analysis

## Pendahuluan

Analisis ini dilakukan untuk memahami efektivitas kampanye pemasaran dan mengidentifikasi faktor-faktor yang mempengaruhi penjualan. Dataset yang digunakan mencakup informasi tentang pendapatan pelanggan, jumlah tanggungan, pengeluaran pada berbagai produk, dan interaksi dengan kampanye pemasaran.

## Data Preprocessing

1. **Memuat Dataset**:
    - Dataset berhasil dimuat dengan baik.

2. **Penanganan Nilai Null**:
    - Nilai null pada kolom `Income` diisi dengan nilai median untuk menjaga distribusi data.

3. **Penghapusan Data yang Tidak Valid**:
    - Baris dengan nilai `Age` lebih dari 120 dihapus untuk menghindari kesalahan entri data.

4. **Rekayasa Fitur**:
    - Menambahkan kolom `TotalDependents` sebagai jumlah dari `Kidhome` dan `Teenhome`.
    - Menambahkan kolom `TotalSpending` sebagai jumlah dari pengeluaran pada berbagai produk (`MntWines`, `MntFruits`, `MntMeatProducts`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds`).
    - Menambahkan kolom `TotalPurchases` sebagai jumlah dari pembelian melalui berbagai saluran (`NumDealsPurchases`, `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases`).

## Analisis Data Eksploratif

### Heatmap Korelasi

- Heatmap korelasi digunakan untuk mengidentifikasi hubungan antara variabel. Korelasi positif kuat ditemukan antara pendapatan dan pengeluaran total.

### Regresi Linear

- Model regresi linear digunakan untuk memprediksi `TotalSpending` berdasarkan `Income`, `TotalDependents`, dan `Age`. Hasil menunjukkan bahwa pendapatan memiliki pengaruh terbesar terhadap pengeluaran total.

### Analisis Segmentasi Pelanggan

- Segmentasi pelanggan dilakukan berdasarkan pengeluaran total dan interaksi dengan kampanye pemasaran. Hasil segmentasi membantu dalam memahami kelompok pelanggan yang paling responsif terhadap kampanye pemasaran.

## Kesimpulan

- Pendapatan merupakan faktor utama yang mempengaruhi pengeluaran total pelanggan.
- Kampanye pemasaran perlu difokuskan pada segmen pelanggan dengan pendapatan tinggi untuk meningkatkan efektivitas.

## Saran

- Optimalkan kampanye pemasaran dengan menargetkan segmen pelanggan yang telah diidentifikasi memiliki pengeluaran tinggi.
- Pertimbangkan untuk melakukan analisis lebih lanjut menggunakan metode machine learning untuk meningkatkan prediktabilitas model.
