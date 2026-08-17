# 📊 Sales Performance & Data Cleaning Dashboard - Power BI

End-to-end Power BI project focusing on raw data cleaning (Power Query), handling anomalies & custom column calculations, and building an interactive sales performance dashboard.

![Power BI Sales Dashboard](Screenshot%202026-08-17%20233829.png)

---

## 📌 Project Overview
Proyek ini berfokus pada **pembersihan data mentah (*Data Cleaning*)** yang tidak terstruktur serta pembuatan **Dashboard Interaktif** menggunakan **Power BI (Power Query)**. Data mentah diolah dari kondisi penuh *anomaly* hingga menghasilkan metrik bisnis yang akurat dan siap dianalisis secara *real-time*.

## 🛠️ Data Cleaning & Transformation (Power Query)
Proses pembersihan data dilakukan secara mendalam pada Power Query Editor:

* **Text Standardization:** Mengubah format teks acak (*uppercase/lowercase*) pada kolom `category` dan `channel` menjadi format *Capitalize Each Word / Proper Case* yang konsisten.
* **Handling Extra Spaces & Duplicates:**
  * Menghapus spasi berlebih pada teks menggunakan fitur **Trim & Clean**.
  * Menghapus baris duplikat berdasarkan kombinasi `order_id` dan atribut terkait.
* **Outlier & Anomaly Handling:**
  * Mengatasi *blank values* pada kolom krusial.
  * Menangani nilai *quantity* yang tidak valid (seperti `-99`) dengan melakukan penyaringan (*filtering*) / *replacement* data.
* **Custom & Calculated Columns:**
  * Menambahkan kalkulasi baru untuk kolom `total_sales` dengan rumus:
    $$\text{total\_sales} = (\text{price} \times \text{quantity} \times (1 - \text{discount})) + \text{shipping\_fee}$$

---

## 📊 Dashboard Visualizations & Key Metrics

* **KPI Cards:**
  * **Sum of Total Sales:** Menampilkan akumulasi total omzet sebesar **876M**.
  * **Average Rating:** Menampilkan rata-rata tingkat kepuasan pelanggan sebesar **3.00**.
* **Monthly Sales Trend (Line Chart):** Tren penjualan bulanan dari *January* hingga *December* untuk melihat pergerakan omzet sepanjang tahun.
* **Sales by Category (Bar Chart):** Perbandingan total penjualan pada kategori **Makanan**, **Perawatan**, dan **Pembersih**.
* **Channel Distribution (Donut Chart):** Proporsi kontribusi penjualan berdasarkan saluran pembelian (**Offline**, **Online - Toko Hijau**, dan **Online - Toko Oren**).
* **Interactive Slicer:** Filtrasi dinamis berdasarkan lokasi wilayah/kota (*Bali, Bandung, Bekasi, Bogor, Depok, Jakarta, dll.*).

---

## 🚀 How to Open & Run
1. Unduh file `.pbix` dari repositori ini.
2. Buka menggunakan **Power BI Desktop**.
3. *Dataset* mentah juga disertakan dalam repositori untuk keperluan audit proses Power Query.
