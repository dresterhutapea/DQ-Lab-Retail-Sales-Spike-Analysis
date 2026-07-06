<img width="1387" height="690" alt="image" src=https://photos.app.goo.gl/WamW9cjKVgWa8yuf7/>

# **Analisis Tren Penjualan dan Identifikasi Sales Spike untuk Optimasi Strategi Bisnis Retail**

## **Ringkasan Proyek (*Executive Summary*)**
Analisis ini bertujuan untuk mengevaluasi tren performa penjualan produk berdasarkan data transaksi historis perusahaan. Dengan melakukan penggabungan data transaksi (tbl_transaction) dan data produk (tbl_product), disaring 5 produk teratas (*Top 5 Products*) dengan volume penjualan tertinggi untuk memetakan fluktuasi permintaan sepanjang periode berjalan. Fokus utama dari analisis ini adalah mengidentifikasi adanya lonjakan penjualan mendadak (*sales spike*) guna memahami faktor pemicunya secara bisnis.

### **Lembar Kerja Jupyter Notebook**: *https://github.com/dresterhutapea/DQ-Lab-Retail-Sales-Spike-Analysis/blob/main/Identifikasi%20Spike.ipynb*

## **Langkah Teknis & Metodologi**
* **Data Preparation & Feature Engineering**: Mengubah data tanggal transaksi menjadi format periode bulan (to_period('M')) dan mengembalikannya ke format timestamp untuk kebutuhan visualisasi.
* **Agregasi & Filtering**: Menggunakan fungsi .groupby() dan .nlargest(5) untuk menyaring 5 produk dengan volume penjualan tertinggi.
* **Data Visualization**: Menggunakan library seaborn dan matplotlib untuk membuat line plot yang interaktif lengkap dengan legenda posisi eksternal agar grafik scannable dan rapi.

<img width="1387" height="690" alt="image" src="https://github.com/user-attachments/assets/5b13fe6f-5049-4199-8dec-c076261cd4d5" />

## **Hasil dan Analisis (Insights)**
Berdasarkan grafik visualisasi line plot yang dihasilkan menggunakan seaborn dan matplotlib, berikut adalah beberapa poin analisis penting:
* **Dominasi Produk**: Dari 5 produk teratas yang ditampilkan, Sticky Notes DQ Lab secara konsisten menunjukkan volume unit terjual yang paling tinggi dibandingkan produk lainnya sepanjang periode pengamatan.
* **Identifikasi Sales Spike**: Terjadi lonjakan penjualan (*sales spike*) yang sangat signifikan pada **September 2024 hingga Maret 2025** untuk produk **Sticky Notes DQ Lab**. Pada titik ini, volume penjualan melonjak tajam hingga mencapai puncaknya di angka **10.000 unit** pada bulan Maret 2025. Di urutan kedua, produk Kertas Warna DQ Lab juga mengalami lonjakan penjualan pada Desember 2024 hingga April 2025, dengan puncak penjualan tertinggi pada April 2025 yakni sebanyak 7500 unit.
* **Pola Anomali / Musiman**: Setelah mencapai titik puncak tersebut, tren penjualan kedua produk menunjukkan penurunan kembali ke titik normal pada bulan Agustus 2025. Hal ini mengindikasikan bahwa *spike* tersebut bersifat momentum (kondisional/musiman) dan bukan merupakan pertumbuhan organik jangka panjang (*long-term organic growth*).

## **Rekomendasi Bisnis**
Berdasarkan temuan visualisasi di atas, berikut adalah rekomendasi strategis yang dapat diimplementasikan oleh tim manajemen, inventaris, dan pemasaran:

### 1. Optimasi Manajemen Inventaris (Supply Chain)
* **Pre-emptive Stocking**: Tim operasional harus mengantisipasi sales spike berulang di masa mendatang dengan meningkatkan kapasitas stok Sticky Notes DQ Lab sebesar 20-30% setidaknya 1 bulan sebelum memasuki periode sibuk (September - Maret). Lakukan tindakan antisipasi serupa untuk produk Kertas Warna DQ Lab menjelang bulan Desember - April. Langkah ini krusial untuk mencegah terjadinya stockout (kehabisan barang) saat permintaan memuncak.
* **Efisiensi Gudang**: Alokasikan ruang penyimpanan utama (*golden zone*) di gudang untuk kategori produk Top 5 ini menjelang bulan-bulan sibuk demi mempercepat proses penyiapan barang (*fulfillment*).

### 2. Strategi Pemasaran Berbasis Momentum
* **Duplikasi Kampanye Sukses**: Selidiki aktivitas pemasaran atau faktor eksternal yang terjadi pada rentang bulan September - Maret (misalnya: musim tahun ajaran baru, promo akhir tahun, *flash sale*, atau hari raya). Jika spike dipicu oleh promo tertentu, tim marketing direkomendasikan untuk mereplikasi formula kampanye tersebut pada produk atau periode potensial lainnya.
* **Retensi Pelanggan Pasca-Spike**: Manfaatkan lonjakan basis pelanggan baru yang didapat selama periode spike untuk dimasukkan ke dalam program loyalty atau email remarketing agar mereka melakukan pembelian berulang (repeat order) di bulan-bulan sepi (low season).

### 3. Penyesuaian Strategi Harga (*Pricing Strategy*)
**Dynamic Pricing**: Pada saat volume permintaan mendekati titik spike, perusahaan dapat mempertimbangkan strategi bundling produk terlaris (Sticky Notes / Kertas Warna) dengan produk yang kurang laku (*slow-moving items*). Strategi ini efektif untuk membersihkan stok gudang secara keseluruhan tanpa menurunkan profitabilitas grup produk utama.
