# Prediksi Kesiapan Redenominasi dalam Mengendalikan Inflasi di Indonesia: Penerapan Analisis Deskriptif Data Mining pada Data Ekonomi Makro

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Data Mining](https://img.shields.io/badge/Data%20Mining-Descriptive-orange)
![Status](https://img.shields.io/badge/Status-Research%20Project-green)

Repository ini berisi kerangka analisis dan kode sumber untuk menilai kesiapan kebijakan redenominasi mata uang Rupiah di Indonesia. Pendekatan yang digunakan adalah **Analisis Deskriptif Data Mining** multi-variabel secara simultan pada data ekonomi makro periode 2010–2024.

## 👥 Tim Peneliti
* **Ahmad Khoiruzzadi** (Universitas Negeri Semarang)
* **Maula Hafif Zulkhoirurroziqin** (Universitas Negeri Semarang)
* **Muhamad Kasyfa Hikam Maula** (Universitas Negeri Semarang)

---

## 📌 Ringkasan Penelitian
Redenominasi adalah penyederhanaan nilai nominal mata uang tanpa mengubah daya beli. Penelitian ini mengevaluasi kesiapan Indonesia berdasarkan **4 Kriteria Simultan** yang dipersyaratkan oleh literatur ekonomi makro untuk menghindari risiko inflasi psikologis (*rounding up*).

Hasil analisis deskriptif data mining menunjukkan bahwa secara simultan Indonesia dinyatakan **TIDAK SIAP** melakukan redenominasi pada periode 2010–2024. Meskipun sektor moneter (Inflasi, JUB, Kurs) sangat stabil, **pertumbuhan PDB Riil gagal memenuhi kriteria konsistensi** (tidak pernah bertahan >4% selama 2 tahun berturut-turut).

---

## 📊 Indikator & Kriteria Kesiapan

| Variabel | Sumber Data | Kriteria Kesiapan | Hasil Analisis | Status |
| :--- | :--- | :--- | :--- | :---: |
| **Inflasi (YoY)** | Bank Indonesia | <5% selama $\ge$ 24 bulan berturut-turut | 83,6% periode memenuhi (ada window 75 bulan stabil) | **MEMENUHI** |
| **JUB (M2)** | Bank Indonesia | $\le$ 15% pertumbuhan per tahun | 92,1% periode terkendali (konsisten sejak 2013) | **MEMENUHI** |
| **PDB Riil** | BPS (Harga Konstan 2010) | >4% per tahun konsisten $\ge$ 2 tahun (8 kuartal) | Hanya 50% kuartal memenuhi; Maksimal hanya bertahan 4 kuartal | ❌ **GAGAL** |
| **Kurs IDR/USD**| Bank Indonesia | Fluktuasi <5% per bulan | 100% periode stabil (Rata-rata fluktuasi 0,22%) | **MEMENUHI** |

> **Kesimpulan Simultan:** **TIDAK SIAP**. Redenominasi baru direkomendasikan setelah pertumbuhan PDB riil mampu menunjukkan tren positif >4% minimal selama dua tahun berturut-turut.

---

## 🛠️ Tahapan Preprocessing Data (Pipeline)
1. **Data Cleaning:** Impor dan pembersihan data menggunakan pustaka `pandas`.
2. **Resampling/Interpolasi:** Menyelaraskan frekuensi data PDB (Triwulanan) ke Bulanan menggunakan *Linear Interpolation*.
3. **Outlier Handling:** Deteksi menggunakan IQR & Z-Score, ditangani dengan teknik *Winsorizing*.
4. **Feature Engineering:** Pembuatan *lag features* dan *rolling window* untuk melihat durasi berturut-turut.
5. **Data Splitting:** Pembagian data *Training:Testing* (80:20) menggunakan *Sequential Split* (tanpa pengacakan) untuk menjaga sifat *time-series* dan mencegah *data leakage*.

---

## 🚀 Rencana Pengembangan Lanjutan
Proyek ini merupakan fondasi analitik deskriptif. Tahap berikutnya adalah implementasi model *Machine Learning* penuh dengan matriks evaluasi sebagai berikut:

* **Klasifikasi Kesiapan:** Random Forest, XGBoost, dan SVM (Target Akurasi >85%).
* **Forecasting Ekonomi:** LSTM (*Long Short-Term Memory*) dan ARIMA untuk memprediksi *window of opportunity* di masa depan.

---

## 📂 Cara Menggunakan Repository ini

### 1. Clone Repository
```bash
git clone [https://github.com/USERNAME-ANDA/nama-repo-anda.git](https://github.com/USERNAME-ANDA/nama-repo-anda.git)
cd nama-repo-anda
