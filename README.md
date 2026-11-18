# Pembersihan Data & Analisis Eksploratif Properti Residensial (Python EDA)

👤 **Penyusun:** Shafwan Mumtaz (NIM: 241011450529 — S1 Teknik Informatika, Universitas Pamulang)  
📚 **Bidang:** Data Mining / Exploratory Data Analysis (EDA) & Data Cleansing

---

## 1. Latar Belakang & Permasalahan Data

Dataset properti residensial (`property_without_duplicates.csv`) yang dikumpulkan dari berbagai sumber memiliki sejumlah permasalahan kualitas data (*dirty data*), antara lain:
- Penamaan kolom dan entri teks kategorikal yang tidak konsisten (misalnya variasi kapitalisasi dan singkatan pada nama jalan `ST_NAME` seperti `LXT`, `LEXINGTON`, `berkeley`, `Berkeley`).
- Nilai hilang (*missing values*) tidak standar serta ketidakseragaman tipe data numerik pada atribut `NUM_BEDROOMS`, `NUM_BATH`, dan `SQ_FT`.
- Potensi anomali pada kolom status kepemilikan hunian (`OWN_OCCUPIED`: `Y` / `N`).

---

## 2. Metodologi & Tahapan Analisis

1. **Inspeksi Awal Dataset:** Memeriksa dimensi data, tipe data tiap atribut (`df.info()`), dan ringkasan statistik deskriptif (`df.describe()`).
2. **Pembersihan & Standarisasi Data (*Data Cleansing*):**
   - Menyeragamkan nama kolom (`PID`, `ST_NUM`, `ST_NAME`, `OWN_OCCUPIED`, `NUM_BEDROOMS`, `NUM_BATH`, `SQ_FT`).
   - Menormalisasi penulisan nama jalan (`ST_NAME`) menjadi huruf kapital seragam dan memperbaiki singkatan (`LXT` menjadi `LEXINGTON`).
   - Menangani *missing values* serta mengonversi tipe data jumlah kamar tidur (`NUM_BEDROOMS`) dan kamar mandi (`NUM_BATH`) menjadi bilangan bulat (*integer*).
3. **Exploratory Data Analysis (EDA) & Visualisasi:**
   - Membandingkan distribusi luas bangunan (`SQ_FT`) di setiap lokasi jalan.
   - Menganalisis proporsi hunian milik sendiri (`OWN_OCCUPIED = Y`) dibandingkan non-milik sendiri (`N`).
   - Mengeksplorasi hubungan antara jumlah kamar tidur/kamar mandi dengan luas bangunan menggunakan `matplotlib` dan `seaborn`.

---

## 3. Struktur File Repositori

```text
├── Data_Analysis_Shafwan_Mumtaz_UTS.ipynb   # Notebook utama Data Cleansing & EDA lengkap
├── Eksplorasi_Data_Properti_Shafwan.ipynb   # Notebook ringkasan visualisasi perbandingan properti
├── property_without_duplicates.csv          # Dataset sebelum standarisasi teks & tipe data
├── file_csv_shafwan.csv                     # Dataset properti bersih hasil standarisasi
├── Analisis_Data_Properti.html              # Laporan hasil ekspor notebook dalam format HTML
└── requirements.txt                         # Daftar pustaka Python yang digunakan
```

---

## 4. Cara Menjalankan Notebook

```bash
pip install -r requirements.txt
jupyter notebook Data_Analysis_Shafwan_Mumtaz_UTS.ipynb
```
