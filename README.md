# Prediksi Kesiapan Redenominasi dalam Mengendalikan Inflasi di Indonesia: Penerapan Analisis Deskriptif Data Mining pada Data Ekonomi Makro

**Ahmad Khoiruzzadi¹ , Maulana Hafif Zulkhoirurroziqin² , Muhamad Kasyfa Hikam Maula³** *¹²³ Fakultas Matematika dan Ilmu Pengetahuan Alam, Universitas Negeri Semarang, Indonesia*

---

## ABSTRAK
Redenominasi merupakan kebijakan penyederhanaan nilai nominal mata uang tanpa mengubah daya beli, namun pelaksanaannya memiliki risiko signifikan terhadap inflasi psikologis dan stabilitas ekonomi makro. Penelitian ini bertujuan untuk menganalisis kesiapan redenominasi di Indonesia berdasarkan empat kriteria simultan menggunakan pendekatan analisis deskriptif data mining, yaitu: inflasi (<5% selama 24 bulan berturut-turut), pertumbuhan Jumlah Uang Beredar (JUB) (≤15% per tahun), pertumbuhan PDB riil (>4% per tahun secara konsisten), dan stabilitas kurs (fluktuasi <5% per bulan). Data yang digunakan adalah data ekonomi makro sekunder periode 2010–2024 dari Bank Indonesia dan Badan Pusat Statistik (BPS), meliputi 128 bulan data inflasi (Januari 2014–Agustus 2024), 139 bulan data JUB (Januari 2012–Juli 2023), 54 triwulan data PDB riil aktual (Triwulan I 2011–Triwulan II 2024), dan 179 bulan data kurs (Februari 2010–Desember 2024). 

Hasil analisis deskriptif menunjukkan bahwa inflasi (83,6% periode memenuhi syarat), JUB (92,1% periode terkendali), dan kurs (100% periode stabil) telah memenuhi kriteria. Namun, pertumbuhan PDB riil hanya memenuhi 47,1% periode dengan durasi pertumbuhan konsisten di atas 4% maksimal empat triwulan (satu tahun) dan tidak pernah mencapai delapan triwulan (dua tahun) berturut-turut. Dengan demikian, secara simultan Indonesia dinyatakan **TIDAK SIAP** melakukan redenominasi pada periode 2010–2024 karena kegagalan memenuhi kriteria konsistensi PDB riil. Redenominasi baru direkomendasikan setelah pertumbuhan PDB riil mampu menunjukkan tren positif >4% minimal selama dua tahun berturut-turut. Penelitian ini berkontribusi sebagai referensi analitik berbasis data untuk pemantauan kesiapan kebijakan redenominasi secara berkelanjutan.

**Kata Kunci:** *Redenominasi, Data Mining, Analisis Deskriptif, Stabilitas Inflasi, PDB Riil, Kesiapan Kebijakan Moneter*

---

## I. PENDAHULUAN

### A. Latar Belakang
Redenominasi merupakan kebijakan moneter yang penting bagi Indonesia karena keberadaan pecahan uang Rupiah dengan nominal terlalu besar, menjadikannya pecahan terbesar kedua di Asia Tenggara setelah Vietnam (Dong). Kondisi ini menyebabkan proses pencatatan pembayaran dan transaksi keuangan, baik tunai maupun nontunai, menjadi kurang efisien (Aulia et al., 2024). Selain itu, banyaknya digit angka pada mata uang mencerminkan lemahnya nilai tukar Rupiah terhadap mata uang asing, sehingga penyederhanaan nilai mata uang melalui redenominasi diharapkan dapat menguatkan nilai Rupiah, menyederhanakan pencatatan keuangan, serta menyetarakan perekonomian Indonesia dengan kawasan regional (Aulia et al., 2024).

Pelaksanaan redenominasi memiliki risiko signifikan, terutama terhadap inflasi. Berdasarkan pengalaman Zimbabwe yang gagal melakukan redenominasi akibat inflasi mencapai 1.096,68 persen (Qushoy et al., 2021), serta temuan bahwa inflasi yang sangat tinggi, perekonomian nasional yang lemah, dan ketidakpercayaan masyarakat terhadap pemerintah menjadi penyebab kegagalan (Febrida & Karolina, 2016). Di sisi lain, inflasi yang stabil dan cenderung menurun justru menjadi syarat mutlak keberhasilan redenominasi (Bemi & Nooraeni, 2019; Pambudi et al., 2014). Penelitian terkini menunjukkan bahwa jumlah uang beredar memiliki hubungan positif terhadap inflasi (Annazah et al., 2018; Mankiw, 2007), dan pertumbuhan uang beredar yang tinggi justru menurunkan tingkat keberhasilan redenominasi (Qushoy et al., 2021; Pambudi et al., 2014).

Kajian mengenai hubungan antara jumlah uang beredar, inflasi, dan kesiapan redenominasi masih banyak dilakukan dengan metode statistik klasik atau analisis regresi linier, belum memanfaatkan pendekatan data mining untuk mengekstraksi pola dari data time series ekonomi yang kompleks. Dengan pendekatan data mining seperti analisis deskriptif, klasifikasi, dan forecasting, peneliti dapat mengidentifikasi periode inflasi stabil yang kondusif untuk redenominasi secara lebih terstruktur (Aulia et al., 2024). Oleh karena itu, penelitian ini menjawab pertanyaan mendasar: kapan Indonesia benar-benar siap melakukan redenominasi tanpa memicu inflasi yang justru menggagalkan kebijakan itu sendiri?

### B. Tujuan Penelitian
**Tujuan Umum:** Membangun kerangka analisis berbasis data mining deskriptif untuk menilai kesiapan redenominasi di Indonesia berdasarkan empat indikator ekonomi makro secara simultan.

**Tujuan Khusus:** * Menganalisis data inflasi, JUB, PDB riil, dan kurs menggunakan statistik deskriptif dan visualisasi tren.
* Mengevaluasi pemenuhan empat kriteria kesiapan redenominasi berdasarkan literatur (Bemi & Nooraeni, 2019; Pambudi et al., 2014; Putri, 2011).
* Mengidentifikasi periode dan durasi kesiapan atau ketidaksiapan Indonesia untuk redenominasi.
* Memberikan rekomendasi berbasis data kepada pemangku kebijakan moneter.

### C. Batasan Penelitian
* Penelitian menggunakan data ekonomi makro sekunder periode 2010–2024 dari BPS dan Bank Indonesia. Data PDB riil yang digunakan hanya mencakup data aktual Triwulan I 2011 hingga Triwulan II 2024 (54 triwulan); data proyeksi setelah 2024 tidak digunakan dalam analisis ini.
* Variabel yang dianalisis meliputi inflasi (YoY), jumlah uang beredar (M2), kurs IDR/USD, dan PDB riil atas dasar harga konstan 2010. Variabel non-ekonomi seperti stabilitas politik, persepsi masyarakat, dan sentimen media tidak termasuk dalam lingkup penelitian.
* Definisi operasional “siap redenominasi” didasarkan pada kriteria literatur: inflasi stabil <5% selama minimal 24 bulan berturut-turut, pertumbuhan JUB ≤15% per tahun, pertumbuhan PDB riil >4% per tahun secara konsisten minimal 2 tahun berturut-turut, serta fluktuasi kurs <5% per bulan.
* Penelitian ini menggunakan pendekatan analisis deskriptif dan evaluasi kriteria berbasis data, bukan implementasi model machine learning secara penuh. Pengembangan model klasifikasi (Random Forest, XGBoost, SVM) dan forecasting (LSTM, ARIMA) direncanakan sebagai tahap lanjutan setelah basis analitik ini tersedia.
* Output penelitian bersifat prediktif-rekomendatif, bukan implementasi kebijakan secara nyata.

---

## II. KAJIAN LITERATUR

### A. Redenominasi, Inflasi, dan Parameter Keberhasilan
Redenominasi didefinisikan sebagai penyederhanaan nilai nominal mata uang tanpa mengurangi nilai tukar riil atau daya beli masyarakat. Berbeda dengan sanering, redenominasi bersifat netral secara ekonomi namun memiliki dampak psikologis yang signifikan. Pratama & Widiastuti (2023) menyatakan bahwa tantangan terbesar redenominasi di Indonesia adalah risiko inflasi yang dipicu oleh perilaku pembulatan ke atas (*rounding up*) oleh pelaku usaha, yang jika tidak dimitigasi, dapat menyebabkan kenaikan harga barang secara masif.

Menurut laporan Bank Indonesia (2024), kebijakan redenominasi hanya dapat dijalankan pada saat kondisi ekonomi stabil, karena inflasi yang rendah dan terkendali merupakan prakondisi absolut agar tidak terjadi distorsi harga selama masa transisi. Literatur ekonomi makro modern menyepakati tiga syarat utama keberhasilan redenominasi:
* **Stabilitas Moneter:** Inflasi berada pada level rendah (di bawah 5%) secara konsisten minimal dua tahun berturut-turut.
* **Stabilitas Nilai Tukar:** Kurs mata uang domestik tidak sedang dalam tekanan depresiasi yang tinggi.
* **Kepercayaan Publik:** Adanya jaminan keamanan politik dan sosial agar tidak terjadi *panic buying*.

### B. Data Mining untuk Analisis Kebijakan Moneter
Penggunaan teknik data mining dalam menganalisis kesiapan redenominasi dianggap lebih komprehensif dibandingkan model ekonometrika klasik karena kemampuannya menangkap pola nonlinear dari data time series yang kompleks. Santoso & Setiawan (2025) menegaskan bahwa algoritma machine learning memiliki kemampuan superior dalam menangkap pola nonlinear dan volatilitas ekstrem pada data makroekonomi yang seringkali gagal dideteksi oleh model statistik tradisional seperti ARIMA atau GARCH. Beberapa algoritma yang relevan dalam konteks ini meliputi Long Short-Term Memory (LSTM) untuk data time series (Kusuma & Hidayat, 2024), serta XGBoost yang mampu melakukan seleksi fitur secara otomatis.

Siregar & Yulianti (2022) menjelaskan bahwa penggunaan platform berbasis cloud dalam riset data mining memfasilitasi reproduksibilitas penelitian dan mempercepat proses analisis data makroekonomi yang kompleks. Namun demikian, sebelum tahap pemodelan machine learning dapat dilakukan, diperlukan fondasi analisis deskriptif yang kokoh untuk memahami karakteristik distribusi, tren, dan volatilitas data sebagai langkah awal data mining.

---

## III. METODOLOGI

### A. Deskripsi Dataset
Dataset yang digunakan dalam penelitian ini adalah data ekonomi makro Indonesia periode 2010–2024 dari institusi resmi BPS dan Bank Indonesia. Penelitian ini menggunakan data aktual (bukan proyeksi) dengan rincian sebagai berikut:

**Tabel 3.1. Rincian Dataset yang Digunakan**

| Variabel | Sumber | Periode | Frekuensi | Jumlah Data | Asal File Data Mentah |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Inflasi (YoY) | Bank Indonesia | Jan 2014 – Agu 2024 | Bulanan | 128 bulan | `inflasi_olahan.csv` |
| Jumlah Uang Beredar (M2) | Bank Indonesia | Jan 2012 – Jul 2023 | Bulanan | 139 bulan | `jub_olahan.csv` |
| PDB Riil (harga konstan 2010) | BPS | Triwulan I 2011 – Triwulan II 2024 | Triwulanan | 54 triwulan | `pdb_olahan.csv` |
| Kurs IDR/USD | Bank Indonesia | Feb 2010 – Des 2024 | Bulanan | 179 bulan | `kurs_olahan.csv` |

*Catatan: Perbedaan periode dan frekuensi antar variabel mencerminkan ketersediaan data dari sumber resmi. Variabel PDB riil berfrekuensi triwulanan karena BPS menerbitkan data PDB dalam satuan tersebut. Tidak ada data proyeksi yang diikutsertakan dalam analisis.*

Berdasarkan kriteria literatur (Bemi & Nooraeni, 2019; Pambudi et al., 2014; Putri, 2011), suatu periode dinyatakan **SIAP REDENOMINASI** jika memenuhi keempat kondisi berikut secara simultan:

**Tabel 3.2. Kriteria Kesiapan Redenominasi**

| Kriteria | Kondisi yang Dipersyaratkan |
| :--- | :--- |
| **Inflasi (YoY)** | <5% selama minimal 24 bulan (2 tahun) berturut-turut |
| **Pertumbuhan JUB (M2)** | ≤15% per tahun |
| **Pertumbuhan PDB Riil** | >4% per tahun secara konsisten minimal 2 tahun (8 triwulan) berturut-turut |
| **Fluktuasi Kurs** | <5% per bulan |

### B. Tahapan Preprocessing
Tahapan preprocessing data meliputi: 
1. Impor dan pembersihan data menggunakan `pandas`.
2. Penyeragaman frekuensi melalui interpolasi linier untuk data PDB triwulanan yang dikonversi ke bulanan.
3. Deteksi outlier menggunakan metode IQR dan Z-score, dengan penanganan melalui teknik *winsorizing*.
4. Normalisasi dan standarisasi data.
5. *Feature engineering* (*lag features*, *rolling window*).
6. Pembagian data *training-testing* secara berurutan (80:20) tanpa pengacakan untuk mencegah *data leakage*.

### C. Pendekatan Analisis
Penelitian ini menggunakan pendekatan analisis deskriptif data mining sebagai tahap eksplorasi dan evaluasi kriteria. Pendekatan ini mencakup: statistik deskriptif (rata-rata, median, standar deviasi, nilai minimum-maksimum); analisis distribusi dan frekuensi pemenuhan kriteria; analisis tren jangka panjang; dan analisis konsistensi (durasi berturut-turut pemenuhan kriteria). Implementasi model machine learning klasifikasi dan forecasting direncanakan sebagai pengembangan lanjutan.

### D. Perbandingan dengan Penelitian Sebelumnya

**Tabel 3.3. Perbandingan dengan Penelitian Terdahulu**

| No | Peneliti (Tahun) | Metode | Hasil | Keterbatasan |
| :---: | :--- | :--- | :--- | :--- |
| 1 | Aulia et al. (2024) | GARCH | Forecasting JUB untuk kebijakan redenominasi | Hanya satu variabel, tidak menilai kesiapan simultan |
| 2 | Annazah et al. (2018) | Regresi Linier Berganda | Faktor pemengaruh keberhasilan redenominasi | Tidak menangkap pola nonlinear |
| 3 | Qushoy et al. (2021) | Analisis deskriptif kualitatif | Studi kasus kegagalan Zimbabwe | Tidak menghasilkan model prediktif |
| 4 | Pambudi et al. (2014) | Regresi Logistik | Probabilitas keberhasilan redenominasi | Asumsi distribusi tertentu, akurasi terbatas |

**Tabel 3.4. Kebaruan Penelitian**

| Aspek | Penelitian Sebelumnya | Penelitian Ini |
| :--- | :--- | :--- |
| **Metode** | Regresi linier, GARCH, regresi logistik | Analisis deskriptif data mining multi-variabel |
| **Cakupan Variabel** | Satu atau dua variabel | Empat variabel simultan (inflasi, JUB, PDB, kurs) |
| **Evaluasi Konsistensi** | Tidak dianalisis | Analisis durasi berturut-turut pemenuhan kriteria |
| **Transparansi Data** | Data sering tidak diperinci | Periode dan sumber data disebutkan eksplisit |
| **Output** | Rekomendasi umum | Evaluasi kriteria spesifik dengan rekomendasi berbasis data |

### E. Matriks Evaluasi
Evaluasi kesiapan dilakukan secara deskriptif berdasarkan pemenuhan keempat kriteria. Untuk analisis lanjutan dengan model machine learning (tahap berikutnya), matriks evaluasi klasifikasi yang akan digunakan meliputi:

**Tabel 3.5. Matriks Evaluasi Rencana Model Machine Learning**

| Algoritma | Matriks Utama | Target | Metode Validasi |
| :--- | :--- | :--- | :--- |
| Random Forest | Accuracy, F1-Score | >85% | Time Series Split |
| XGBoost | Accuracy, AUC-ROC | >85%, >0,90 | Time Series Split |
| SVM | Precision, Recall | >80% | Time Series Split |
| LSTM | RMSE, MAPE | <0,5; <10% | Walk-Forward Validation |
| ARIMA (baseline) | RMSE, MAPE | Sebagai pembanding | Walk-Forward Validation |

---

## IV. HASIL DAN PEMBAHASAN

### A. Hasil Pengolahan Data Inflasi
Data inflasi yang diperoleh dari Bank Indonesia periode Januari 2014 hingga Agustus 2024 menghasilkan 128 bulan data inflasi bulanan (*year-on-year*) yang siap dianalisis.

**Tabel 4.1. Statistik Deskriptif Inflasi (2014–2024)**

| Statistik | Nilai |
| :--- | :--- |
| Rata-rata | 3,71% |
| Standar Deviasi | 1,70% |
| Inflasi Teringgi | 8,36% (Desember 2014) |
| Inflasi Terendah | 1,32% (Agustus 2020) |
| Jumlah Data | 128 bulan |

Inflasi Indonesia cenderung terkendali dalam satu digit, dengan puncak pada 2014–2015 pasca kenaikan harga BBM dan akhir 2022 akibat tekanan energi global. Pada masa pandemi COVID-19, inflasi mencapai titik terendah 1,32% (Agustus 2020).

* **Gambar 4.1. Tren Inflasi Indonesia (2014–2024)** (Grafik dapat dilihat pada folder `visuals/trend_inflasi.png`)
* **Gambar 4.2. Distribusi Tingkat Inflasi (2014–2024)** (Grafik dapat dilihat pada folder `visuals/distribusi_inflasi.png`)

#### 1. Analisis Kesiapan Redenominasi Berdasarkan Kriteria Inflasi

**Tabel 4.2. Distribusi Kesiapan Redenominasi Berdasarkan Kriteria Inflasi**

| Kesiapan | Kriteria (Inflasi) | Jumlah Bulan | Persentase |
| :--- | :--- | :---: | :---: |
| Siap Redenominasi | Inflasi <5% | 107 | 83,6% |
| Tidak Siap | Inflasi ≥5% | 21 | 16,4% |
| **Total** | — | **128** | **100%** |

#### 2. Analisis Durasi Inflasi Stabil

**Tabel 4.3. Periode Inflasi Stabil (<5%)**

| Periode | Durasi | Keterangan |
| :--- | :--- | :--- |
| November 2015 – Agustus 2022 | 75 bulan | Inflasi stabil terpanjang, memenuhi syarat 24 bulan |
| Maret 2023 – Agustus 2024 | 18 bulan | Masih berlangsung, belum mencapai 24 bulan |

Temuan ini menunjukkan bahwa Indonesia pernah memiliki *window of opportunity* yang sangat panjang untuk redenominasi (2015–2022). Namun, inflasi kembali melampaui 5% pada September–Desember 2022 sebelum kembali stabil.

### B. Hasil Pengolahan Data Jumlah Uang Beredar (M2)

**Tabel 4.4. Statistik Deskriptif Jumlah Uang Beredar (M2) Periode 2012–2023**

| Statistik | Nilai (Miliar Rp) |
| :--- | :--- |
| Rata-rata M2 | 6.271.344,85 |
| Standar Deviasi | 2.092.680,17 |
| M2 Terendah | 2.994.474,39 (Januari 2012) |
| M2 Tertinggi | 10.355.113,40 (Juli 2023) |
| Jumlah Data | 139 bulan |

JUB Indonesia meningkat signifikan dari sekitar Rp3.000 triliun (awal 2012) menjadi lebih dari Rp10.000 triliun (pertengahan 2023), mencerminkan ekspansi moneter dalam 11,5 tahun.

#### 1. Analisis Kesiapan Redenominasi Berdasarkan Kriteria JUB

**Tabel 4.5. Distribusi Kesiapan Berdasarkan Kriteria JUB**

| Kesiapan | Kriteria (Pertumbuhan JUB) | Jumlah Bulan | Persentase |
| :--- | :--- | :---: | :---: |
| JUB Terkendali (Siap) | ≤15% per tahun | 128 | 92,1% |
| Tidak Siap | >15% per tahun | 11 | 7,9% |
| **Total** | — | **139** | **100%** |

Sebelas bulan dengan pertumbuhan JUB >15% terkonsentrasi pada awal 2012–2013 dan satu bulan di awal pandemi (Februari 2020). Sejak Maret 2013, pertumbuhan JUB konsisten di bawah 15% selama lebih dari 10 tahun, dengan tren menurun menjadi rata-rata 7,74% pada periode 2021–2023.

* **Gambar 4.3. Tren Jumlah Uang Beredar (M2) Indonesia Periode 2012–2023** (Lihat `visuals/trend_m2.png`)
* **Gambar 4.4. Pertumbuhan Tahunan JUB (YoY) Periode 2012–2023** (Lihat `visuals/pertumbuhan_jub.png`)

### C. Hasil Pengolahan Data PDB Riil
Data PDB riil yang digunakan merupakan data aktual BPS atas dasar harga konstan 2010, mencakup Triwulan I 2011 hingga Triwulan II 2024 dengan total 54 triwulan (13,5 tahun). Penelitian ini tidak menggunakan data proyeksi pasca-2024.

**Tabel 4.6. Statistik Deskriptif Pertumbuhan PDB Riil Aktual (2011–2024)**

| Statistik | Nilai |
| :--- | :--- |
| Rata-rata Pertumbuhan (YoY) | 4,8% (termasuk periode pandemi) |
| Median Pertumbuhan | 5,1% |
| Pertumbuhan Tertinggi | 7,07% (Triwulan II 2021, pemulihan pasca pandemi) |
| Pertumbuhan Terendah | -5,32% (Triwulan II 2020, puncak pandemi COVID-19) |
| Standar Deviasi | 3,12% |
| Jumlah Data | 54 triwulan |

#### 1. Analisis Kesiapan Redenominasi Berdasarkan Kriteria PDB Riil

**Tabel 4.7. Distribusi Kesiapan Berdasarkan Kriteria PDB Riil (2011–2024)**

| Kesiapan | Kriteria (Pertumbuhan PDB) | Jumlah Triwulan | Persentase |
| :--- | :--- | :---: | :---: |
| Memenuhi Syarat | >4% per tahun | 27 | 50,0% |
| Tidak Memenuhi Syarat | ≤4% per tahun | 27 | 50,0% |
| **Total** | — | **54** | **100%** |

#### 2. Analisis Konsistensi Pertumbuhan PDB

**Tabel 4.8. Durasi Pertumbuhan PDB Riil >4% Berturut-turut (2011–2024)**

| Durasi (Triwulan) | Periode | Keterangan |
| :--- | :--- | :--- |
| 4 triwulan (1 tahun) | Q3 2011–Q2 2012; Q2 2017–Q1 2018 | Durasi terpanjang yang ditemukan |
| 3 triwulan | Beberapa periode | Kurang dari 1 tahun |
| 2 triwulan | Sering terjadi | Konsistensi sangat pendek |
| 8 triwulan (2 tahun) | — | **Tidak pernah terjadi** |

Tidak ditemukan periode dengan pertumbuhan PDB riil di atas 4% selama dua tahun (delapan triwulan) berturut-turut dalam data aktual 2011–2024. Ini merupakan hambatan utama kesiapan redenominasi dari sisi pertumbuhan ekonomi.

* **Gambar 4.5. Tren PDB Riil Indonesia Triwulanan (2011–2024)** (Lihat `visuals/trend_pdb.png`)
* **Gambar 4.6. Pertumbuhan Tahunan PDB Riil (YoY) 2011–2024** (Lihat `visuals/pertumbuhan_pdb.png`)

### D. Hasil Pengolahan Data Kurs IDR/USD

**Tabel 4.9. Statistik Deskriptif Kurs IDR/USD Periode 2010–2024**

| Statistik | Nilai (Rp per USD) |
| :--- | :--- |
| Rata-rata Kurs | 13.081,28 |
| Standar Deviasi | 2.407,22 |
| Kurs Terendah | 8.770,00 (Januari 2011) |
| Kurs Tertinggi | 15.857,00 (Desember 2024) |
| Jumlah Data | 179 bulan |

#### 1. Analisis Kesiapan Redenominasi Berdasarkan Kriteria Kurs

**Tabel 4.10. Distribusi Kesiapan Berdasarkan Kriteria Kurs (2010–2024)**

| Kesiapan | Kriteria (Fluktuasi Bulanan) | Jumlah Bulan | Persentase |
| :--- | :--- | :---: | :---: |
| Kurs Stabil (Siap) | Fluktuasi <5% | 179 | 100% |
| Kurs Tidak Stabil | Fluktuasi ≥5% | 0 | 0% |
| **Total** | — | **179** | **100%** |

Seluruh 179 bulan pengamatan (100%) memenuhi kriteria stabilitas kurs dengan fluktuasi bulanan di bawah 5%. Rata-rata fluktuasi bulanan hanya 0,22%, jauh di bawah batas kriteria.

**Tabel 4.11. Evaluasi Kriteria Kurs terhadap Redenominasi**

| Kriteria | Target | Hasil Analisis | Status |
| :--- | :--- | :--- | :--- |
| Fluktuasi kurs | <5% per bulan | 0,22% rata-rata | Terpenuhi |
| Konsistensi stabilitas | Minimal 2 years | 14 tahun (2010–2024) | Terpenuhi |
| Tidak ada fluktuasi ekstrem | Tidak ada >5% | 0 bulan dari 179 | Terpenuhi |

### E. Evaluasi Keseluruhan Kesiapan Redenominasi

**Tabel 4.12. Ringkasan Evaluasi Kesiapan Redenominasi Indonesia 2010–2024**

| Kriteria | Kondisi Dipersyaratkan | Hasil Analisis | Status |
| :--- | :--- | :--- | :---: |
| **Inflasi (YoY)** | <5% selama ≥24 bulan berturut-turut | Tersedia 75 bulan stabil (Nov 2015–Agu 2022) | **SIAP** |
| **Pertumbuhan JUB** | ≤15% per tahun | 92,1% periode terkendali; stabil sejak 2013 | **SIAP** |
| **Pertumbuhan PDB Riil** | >4% secara konsisten ≥2 tahun berturut-turut | Hanya 50% triwulan memenuhi; durasi maks 4 triwulan | ❌ **TIDAK SIAP** |
| **Fluktuasi Kurs** | <5% per bulan | 100% periode stabil; rata-rata 0,22% | **SIAP** |

> ⚠️ **KESIMPULAN SIMULTAN:** Karena salah satu dari empat kriteria (PDB riil) tidak terpenuhi, maka secara simultan Indonesia dinyatakan **TIDAK SIAP** melakukan redenominasi pada periode 2010–2024.

---

## V. KESIMPULAN
Berdasarkan kriteria yang dikemukakan oleh Bemi & Nooraeni (2019), Pambudi et al. (2014), serta Putri (2011), sebagaimana dirujuk dalam Aulia et al. (2024), suatu periode dinyatakan siap redenominasi hanya jika keempat kriteria terpenuhi secara simultan. Hasil penelitian menunjukkan bahwa:
1. **Inflasi dan kurs** telah memenuhi syarat dengan sangat baik, bahkan melampaui batas minimal yang dipersyaratkan literatur.
2. **Jumlah Uang Beredar (JUB)** juga menunjukkan kondisi terkendali pada hampir seluruh periode pengamatan (92,1%).
3. Namun, **kriteria PDB Riil tidak terpenuhi** karena pertumbuhan ekonomi masih fluktuatif, hanya 50% triwulan aktual yang tumbuh di atas 4%, dan tidak pernah terjadi pertumbuhan positif berkelanjutan selama minimal dua tahun berturut-turut.

Dengan demikian, secara simultan Indonesia dinyatakan **TIDAK SIAP** melakukan redenominasi pada periode pengamatan 2010–2024. Kegagalan memenuhi kriteria konsistensi PDB riil menjadi faktor penghambat utama. Redenominasi baru dapat direkomendasikan jika pertumbuhan PDB riil Indonesia mampu menunjukkan tren positif yang konsisten di atas 4% selama minimal dua tahun berturut-turut.

---

## VI. SARAN

### A. Saran bagi Pemerintah dan Bank Indonesia

**Tabel 6.1. Rekomendasi Kebijakan**

| No | Saran | Tujuan |
| :---: | :--- | :--- |
| 1 | Memperkuat fundamental ekonomi riil melalui diversifikasi sektor produktif dan peningkatan investasi | Menstabilkan pertumbuhan PDB di atas 4% secara konsisten minimal 2 tahun |
| 2 | Menjaga stabilitas makroekonomi yang telah tercapai pada inflasi, JUB, dan kurs | Mempertahankan momentum kesiapan di tiga kriteria yang sudah baik |
| 3 | Menyusun roadmap redenominasi bertahap: sosialisasi 2–3 tahun, dual currency 1–2 tahun, penghapusan unit lama | Mengantisipasi ketidakpastian dan membangun kepercayaan masyarakat |
| 4 | Meningkatkan kualitas dan konsistensi pencatatan data PDB, memisahkan data aktual dari proyeksi | Menghindari bias analisis dan keputusan kebijakan yang keliru |

### B. Saran untuk Penelitian Selanjutnya
1. Menambahkan variabel non-ekonomi (stabilitas politik, literasi keuangan, kesiapan sistem pembayaran) untuk gambaran kesiapan yang lebih komprehensif.
2. Mengimplementasikan model machine learning klasifikasi (Random Forest, XGBoost, SVM) dan forecasting (LSTM, ARIMA) sebagai pengembangan dari analisis deskriptif ini.
3. Melakukan studi komparatif dengan negara yang berhasil redenominasi (Turki 2005, Venezuela 2008) untuk menggali faktor keberhasilan di negara berkembang.
4. Memperpanjang periode pengamatan dengan data aktual terbaru pasca-2024.

---

## VII. DAFTAR PUSTAKA

* Annazah, N., Hidayati, R., & Mustofa, A. (2018). Pengaruh jumlah uang beredar dan suku bunga terhadap tingkat inflasi di Indonesia. *Jurnal Ekonomi dan Bisnis Islam*, 3(2), 112–124.
* Aulia, B. P., Pamungkas, K. A., Mauboy, L. M., & Wijayanti, T. K. (2024). Forecasting money supply menggunakan metode GARCH untuk kebijakan redenominasi Indonesia. *Jurnal BPPK: Badan Pendidikan dan Pelatihan Keuangan*, 17(2). https://doi.org/10.48108/jurnalbppk.v17i2
* Bank Indonesia. (2024). *Laporan Perekonomian Indonesia: Menjaga Momentum di Tengah Ketidakpastian Global*. Jakarta: Departemen Komunikasi Bank Indonesia.
* Bemi, H., & Nooraeni, R. (2019). Analisis kesiapan redenominasi Rupiah berdasarkan indikator ekonomi makro. *Jurnal Riset Ekonomi dan Manajemen*, 19(1), 45–60.
* Febrida, M., & Karolina, S. (2016). Analisis faktor penyebab kegagalan redenominasi mata uang: Studi kasus Zimbabwe. *Jurnal Ekonomi Pembangunan*, 14(2), 88–99.
* Kusuma, R. W., & Hidayat, T. (2024). Forecasting inflation in emerging markets: A comparative study of XGBoost, LSTM, and traditional econometric models. *Journal of Asian Economics*, 89, 102–118. https://doi.org/10.1016/j.asieco.2024.01.005
* Mankiw, N. G. (2007). *Principles of Economics* (5th ed.). Mason, OH: South-Western Cengage Learning.
* Pambudi, D., Firdaus, M., & Siregar, H. (2014). Analisis kesiapan Indonesia melaksanakan redenominasi Rupiah dengan pendekatan regresi logistik. *Jurnal Ekonomi dan Kebijakan Pembangunan*, 3(1), 1–20.
* Pratama, A., & Widiastuti, N. (2023). Analisis risiko psikologis dan stabilitas makroekonomi pada wacana redenominasi Rupiah di era digital. *Buletin Ekonomi Moneter dan Perbankan*, 26(2), 245–268.
* Putri, R. A. (2011). *Analisis kesiapan Indonesia dalam redenominasi Rupiah* (Skripsi). Universitas Indonesia, Depok.
* Qushoy, M., Hakim, L., & Rahmawati, F. (2021). Studi kasus kegagalan redenominasi Zimbabwe dan implikasinya bagi Indonesia. *Jurnal Kajian Ekonomi dan Keuangan*, 5(1), 34–48.
* Santoso, B., & Setiawan, I. (2025). Perbandingan volatilitas model GARCH dan algoritma machine learning dalam memprediksi fluktuasi harga dan inflasi di Indonesia. *Jurnal Ilmu Komputer dan Statistika Terapan*, 12(1), 45–58.
* Siregar, H., & Yulianti, D. (2022). Penerapan machine learning sebagai early warning system dalam mitigasi risiko hiperinflasi pada transisi kebijakan moneter. *Jurnal Ekonomi Kuantitatif Terapan*, 15(2), 112–127.
* Suharto, E., & Rahayu, S. M. (2023). Kesiapan infrastruktur dan stabilitas ekonomi makro menuju redenominasi mata uang: Studi kasus Indonesia. *Jurnal Kajian Ekonomi dan Pembangunan*, 8(3), 89–104.
