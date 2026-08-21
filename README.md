## Tugas-Akhir-Melvin Marly

>Perbandingan Cakupan Radius Layanan Minimarket Menggunakan Buffer Analysis di Quantum GIS (Studi kasus Kecamatan Penjaringan, Jakarta Utara)

 ----------------------------------------------------------------------------------------------------------------------------

 ## Deskripsi Proyek
 
Repository ini merupakan dokumentasi pendamping tugas akhir yang membahas perbandingan cakupan radius layanan Minimarket X dan Minimarket Y menggunakan metode Buffer Analysis pada QGIS. Penelitian dilakukan di Kecamatan Penjaringan, Jakarta Utara, dengan menggunakan titik lokasi Minimarket X dan Minimarket Y serta data populasi penduduk. Analisis spasial dilakukan menggunakan radius buffer sebesar 500 meter untuk mengidentifikasi wilayah yang tercakup dan tidak tercakup oleh radius layanan kedua jenis minimarket. Hasil penelitian digunakan untuk membandingkan persebaran gerai, cakupan radius layanan, serta jumlah penduduk yang berada di dalam dan di luar cakupan radius layanan minimarket.

---

## Tujuan Penelitian

Penelitian ini bertujuan untuk:

1. Menganalisis persebaran Minimarket X dan Minimarket Y di Kecamatan Penjaringan, Jakarta Utara.
2. Menganalisis dan membandingkan wilayah yang tercakup dan tidak tercakup oleh radius layanan kedua minimarket berdasarkan Buffer Analysis.
3. Mengidentifikasi jumlah penduduk yang tercakup dan tidak tercakup oleh radius layanan Minimarket X dan Minimarket Y.
4. Mengidentifikasi wilayah yang masih memiliki keterbatasan cakupan radius layanan minimarket.

---

## Data

Data yang digunakan dalam penelitian terdiri dari:

| Dataset | Sumber | Fungsi |
|---|---|---|
| Lokasi Minimarket X | Indopaket / Google Maps | Titik input Buffer Analysis |
| Lokasi Minimarket Y | Google Maps | Titik input Buffer Analysis |
| Data populasi penduduk | Badan Pusat Statistik Kota Jakarta Utara | Analisis jumlah penduduk yang tercakup radius Buffer |
| Batas wilayah penelitian | gadm41_IDN | Clipping batas wilayah administrasi |

### Jumlah Observasi atau Titik Data

Data lokasi minimarket yang digunakan dalam penelitian terdiri dari:

- 64 titik lokasi Minimarket X
- 40 titik lokasi Minimarket Y
- 104 titik lokasi minimarket secara keseluruhan

Setiap titik minimarket digunakan sebagai objek spasial untuk membentuk zona layanan menggunakan Buffer Analysis dengan radius 500 meter.Data populasi penduduk tidak diperlakukan sebagai titik observasi minimarket, tetapi digunakan sebagai data untuk menghitung jumlah penduduk yang berada di dalam wilayah cakupan buffer. Batas wilayah gadm41_IDN digunakan sebagai data spasial pembatas untuk memastikan analisis dilakukan pada wilayah Kecamatan Penjaringan.

### Variabel yang Digunakan
1. **Lokasi minimarket**  
   Menunjukkan posisi spasial setiap gerai Minimarket X dan Minimarket Y.

2. **Jenis minimarket**  
   Digunakan untuk membedakan objek Minimarket X dan Minimarket Y dalam proses perbandingan.

3. **Koordinat lokasi**  
   Digunakan sebagai informasi spasial titik minimarket untuk proses Buffer Analysis.

4. **Radius buffer**  
   Menggunakan jarak **500 meter** dari setiap titik minimarket sebagai batas cakupan layanan.

5. **Jumlah penduduk**  
   Digunakan untuk menghitung jumlah penduduk yang berada di dalam wilayah cakupan radius buffer.

6. **Batas administrasi**  
   Digunakan untuk membatasi wilayah analisis pada Kecamatan Penjaringan.

- Data lokasi titik minimarket yang berawal dari data mentah di transformasi menjadi data spasial untuk melakukan proses buffer
- data raw yang digunakan adalah data batas wilayah seluruh administrasi kemudian di processed menjadi batas wilayah yang diperlukan


## Area Penelitian

Wilayah penelitian berada di: **Kecamatan Penjaringan, Jakarta Utara, DKI Jakarta, Indonesia.**

Kecamatan Penjaringan terdiri dari lima kelurahan yang menjadi cakupan penelitian:
- Penjaringan
- Pejagalan
- Pluit
- Kapuk Muara
- Kamal Muara

Objek penelitian berupa titik lokasi Minimarket X dan Minimarket Y yang berada di wilayah Kecamatan Penjaringan.

---

Jumlah objek minimarket yang digunakan:

| Minimarket | Jumlah Gerai |
|---|---:|
| Minimarket X | 64 |
| Minimarket Y | 40 |
| Total | 104 |

Sebaran gerai berdasarkan kelurahan:

| Kelurahan | Minimarket X | Minimarket Y |
|---|---:|---:|
| Pluit | 14 | 17 |
| Penjaringan | 19 | 4 |
| Pejagalan | 11 | 9 |
| Kapuk Muara | 5 | 3 |
| Kamal Muara | 15 | 7 |
| **Total** | **64** | **40** |

Data populasi penduduk Kecamatan Penjaringan yang digunakan dalam analisis berjumlah **372.132 penduduk**

---

## Metodologi

Tahapan penelitian dilakukan sebagai berikut:

1. Identifikasi masalah.
2. Studi literatur.
3. Menentukan wilayah penelitian.
4. Mengumpulkan data lokasi Minimarket X dan Minimarket Y.
5. Mengumpulkan data populasi penduduk.
6. Melakukan digitasi data menggunakan QGIS.
7. Membuat zona Buffer pada lokasi minimarket.
8. Menggunakan radius buffer 500 meter.
9. Melakukan Dissolve terhadap zona buffer.
10. Melakukan Union untuk menggabungkan informasi spasial.
11. Melakukan Clip terhadap wilayah penelitian.
12. Menggunakan Symmetrical Difference untuk mengidentifikasi wilayah yang tidak saling bertumpang tindih.
13. Menggunakan Zonal Statistics untuk menghitung jumlah populasi.
14. Membandingkan cakupan radius layanan Minimarket X dan Minimarket Y.
15. Melakukan interpretasi hasil.
16. Menyusun laporan penelitian.

---

## Buffer Analysis

Buffer Analysis digunakan untuk membentuk zona berdasarkan jarak tertentu dari titik lokasi minimarket.

Dalam penelitian ini, setiap titik Minimarket X dan Minimarket Y diberikan zona buffer dengan radius: **500 meter**
Radius 500 meter digunakan sebagai batas analisis spasial untuk mengidentifikasi cakupan radius layanan minimarket terhadap populasi penduduk.


---

## Parameter

| Parameter | Nilai |
|---|---|
| Software | QGIS |
| Metode utama | Buffer Analysis |
| Radius Buffer | 500 meter |
| Objek | Minimarket X dan Minimarket Y |
| Wilayah | Kecamatan Penjaringan, Jakarta Utara |
| Analisis populasi | Zonal Statistics |
| Analisis perbandingan | Union, Dissolve, Symmetrical Difference |
| Data populasi | Data raster populasi penduduk |
| Jumlah Minimarket X | 64 gerai |
| Jumlah Minimarket Y | 40 gerai |

---

# Hasil utama

## 1. Persebaran Minimarket X

<img width="3507" height="2480" alt="Foto Persebaran Minimarket X" src="https://github.com/user-attachments/assets/d402e3f4-b627-4d49-8fa7-020e3b0082f6" />

Terdapat **64 gerai Minimarket X** yang tersebar di lima kelurahan.

| Kelurahan | Jumlah |
|---|---:|
| Pluit | 14 |
| Penjaringan | 19 |
| Pejagalan | 11 |
| Kapuk Muara | 5 |
| Kamal Muara | 15 |
| **Total** | **64** |

Jumlah gerai terbanyak terdapat di Kelurahan Penjaringan dengan 19 gerai, sedangkan jumlah paling sedikit terdapat di Kelurahan Kapuk Muara dengan 5 gerai.

---

## 2. Persebaran Minimarket Y

<img width="3507" height="2480" alt="Foto Persebaran Minimarket Y" src="https://github.com/user-attachments/assets/110bf18f-2c4c-4ea8-9632-60dd886ffb33" />

Terdapat **40 gerai Minimarket Y** yang tersebar di lima kelurahan.

| Kelurahan | Jumlah |
|---|---:|
| Pluit | 17 |
| Penjaringan | 4 |
| Pejagalan | 9 |
| Kapuk Muara | 3 |
| Kamal Muara | 7 |
| **Total** | **40** |

Jumlah gerai terbanyak terdapat di Kelurahan Pluit dengan 17 gerai, sedangkan jumlah paling sedikit terdapat di Kelurahan Kapuk Muara dengan 3 gerai.

---

## 3. Zona Buffer Minimarket X dan Y

<img width="3507" height="2480" alt="Foto buffer minimarket X dan Y" src="https://github.com/user-attachments/assets/7302834d-77cb-4f8b-a2db-48edf6547bee" />


Buffer dengan radius 500 meter menunjukkan adanya wilayah dengan cakupan layanan yang saling bertumpang tindih.
Wilayah Penjaringan, Pluit, dan Pejagalan memiliki cakupan buffer yang relatif luas. Beberapa zona buffer pada wilayah tersebut saling bertumpang tindih karena lokasi gerai yang relatif berdekatan. Sebaliknya, sebagian wilayah Kapuk Muara dan Kamal Muara masih memiliki area yang berada di luar cakupan radius buffer kedua minimarket.

---

## 4. Wilayah yang Tercakup Radius Buffer

<img width="3507" height="2480" alt="Foto populasi yang tercakup radius" src="https://github.com/user-attachments/assets/2b93f792-95bd-4e99-ab37-5cb2dbecfd7f" />


Hasil analisis menunjukkan bahwa sebagian besar wilayah Penjaringan, Pluit, dan Pejagalan berada dalam cakupan radius buffer. Wilayah yang berada di luar radius 500 meter menunjukkan area yang secara spasial membutuhkan jarak lebih dari 500 meter dari titik minimarket terdekat. Hasil ini digunakan sebagai pendekatan spasial dan bukan sebagai ukuran aksesibilitas aktual.

---

## 5. Populasi yang Tercakup Minimarket X

<img width="3507" height="2480" alt="Peta populasi minimarket X" src="https://github.com/user-attachments/assets/1dadeca5-3b61-438f-971c-42c9270eb89b" />


Hasil Zonal Statistics menunjukkan jumlah penduduk yang berada dalam cakupan radius 500 meter Minimarket X sebesar: **204.758 penduduk**

| Kelurahan | Penduduk Tercakup |
|---|---:|
| Penjaringan | 51.638 |
| Pejagalan | 30.204 |
| Pluit | 53.589 |
| Kapuk Muara | 27.332 |
| Kamal Muara | 41.995 |
| **Total** | **204.758** |

Kelurahan Pluit memiliki jumlah penduduk tercakup terbesar, yaitu 53.589 penduduk.
Kelurahan Kapuk Muara memiliki jumlah penduduk tercakup paling rendah, yaitu 27.332 penduduk.

---

## 6. Populasi yang Tercakup Minimarket Y

<img width="3507" height="2480" alt="peta populasi minimarket Y" src="https://github.com/user-attachments/assets/de0a5580-2f0e-4b82-8b58-560a1e35b3ae" />


Hasil Zonal Statistics menunjukkan jumlah penduduk yang berada dalam cakupan radius 500 meter Minimarket Y sebesar: **181.332 penduduk**

| Kelurahan | Penduduk Tercakup |
|---|---:|
| Penjaringan | 38.330 |
| Pejagalan | 28.883 |
| Pluit | 57.739 |
| Kapuk Muara | 20.845 |
| Kamal Muara | 35.535 |
| **Total** | **181.332** |

Kelurahan Pluit memiliki jumlah penduduk tercakup terbesar, yaitu 57.739 penduduk.
Kelurahan Kapuk Muara memiliki jumlah penduduk tercakup paling rendah, yaitu 20.845 penduduk.

---

## 7. Populasi yang Tidak Tercakup

<img width="3507" height="2480" alt="foto wilayah yang tidak tercakup" src="https://github.com/user-attachments/assets/50f7d62f-1880-47ff-b45b-f626ecc19ee4" />


Hasil analisis menunjukkan terdapat sekitar: **147.463 penduduk** yang berada di luar cakupan radius layanan Minimarket X maupun Minimarket Y dengan batas analisis 500 meter.
Temuan tersebut menunjukkan bahwa jumlah gerai minimarket yang banyak tidak secara langsung menjamin pemerataan cakupan layanan. Masih terdapat wilayah dengan populasi penduduk yang berada di luar zona buffer kedua minimarket.

---

# Perbandingan

Perbandingan hasil cakupan populasi:

| Indikator | Minimarket X | Minimarket Y |
|---|---:|---:|
| Jumlah gerai | 64 | 40 |
| Populasi tercakup | 204.758 | 181.332 |
| Populasi tercakup terbesar | Pluit: 53.589 | Pluit: 57.739 |
| Populasi tercakup terkecil | Kapuk Muara: 27.332 | Kapuk Muara: 20.845 |

Berdasarkan hasil analisis, Minimarket X memiliki jumlah gerai yang lebih banyak dan total populasi tercakup yang lebih besar dibandingkan Minimarket Y.

---

# Keterbatasan

Penelitian ini memiliki beberapa keterbatasan:

- Hanya menggunakan Buffer Analysis.
- Hanya analisis satu Kecamatan.
- Analisis belum mempertimbangkan jaringan jalan.
- Analisis belum mempertimbangkan kondisi lalu lintas.
- Analisis belum mempertimbangkan waktu tempuh aktual masyarakat.
- Radius 500 meter merupakan batas analisis spasial, bukan ukuran aksesibilitas aktual.
- Data hanya berfokus pada dua jenis minimarket.
- Hasil cakupan populasi merupakan hasil analisis spasial berdasarkan data yang tersedia.

---

# Cara reproduksi

## Software

Analisis dilakukan menggunakan:

- Quantum Geographic Information System (QGIS 3.42.2)
- Processing Toolbox QGIS
- Tools Buffer
- Tools Dissolve
- Tools Union
- Tools Clip
- Tools Symmetrical Difference
- Zonal Statistics

## Langkah Reproduksi

1. Buka QGIS.
2. Buka file proyek `Peta Penjaringan` pada folder `Map Utara`.
3. Masukkan data lokasi Minimarket dengan menandakan titik (point) dengan manual pada peta (sumber: Indopaket & Google Maps)
4. Masukkan data populasi penduduk.
5. Masukkan batas wilayah Kecamatan Penjaringan.
6. Pastikan sistem koordinat data sesuai dengan kebutuhan analisis.
7. Jalankan Buffer terhadap titik (point) lokasi minimarket.
8. Gunakan radius 500 meter.
9. Lakukan Dissolve pada hasil buffer.
10. Lakukan Clip berdasarkan batas Kecamatan Penjaringan.
11. Gabungkan informasi buffer menggunakan Union.
12. Gunakan Symmetrical Difference untuk mengidentifikasi area yang tidak tumpang tindih.
13. Gunakan Zonal Statistics untuk menghitung populasi.
14. Bandingkan hasil Minimarket X dan Minimarket Y.
15. Simpan hasil peta dan tabel analisis pada folder.

---

-----------------------------------------------------------------------------------------------------------------

## Peta Sebaran Kedua Jenis Minimarket di Kecamatan Penjaringan, Jakarta Utara

<img width="3507" height="2480" alt="Foto persebaran Minimarket X dan Y" src="https://github.com/user-attachments/assets/fae84df9-0cd1-4a7d-8e1e-253fb7ca947f" />

---------------------------------------------------------------------------------------------------------------------

## Peta hasil Buffer dari kedua Minimarket

<img width="3507" height="2480" alt="Foto buffer minimarket X dan Y" src="https://github.com/user-attachments/assets/b615deeb-d44d-4fc9-9b74-bb577ae279e7" />

----------------------------------------------------------------------------------------------------------------------

## Peta hasil dari wilayah tercakup radius layanan Buffer

<img width="3507" height="2480" alt="foto wilayah yang tercakup radius" src="https://github.com/user-attachments/assets/e3d6a8ef-c266-4d6a-85f3-c71e5ebc38b0" />

-----------------------------------------------------------------------------------------------------------------------

## Peta hasil dari wilayah yang tidak tercakup radius layanan Buffer

<img width="3507" height="2480" alt="foto wilayah yang tidak tercakup" src="https://github.com/user-attachments/assets/fb33e220-20c7-4f41-8272-520413b22b4b" />

------------------------------------------------------------------------------------------------------------------------

## Peta hasil populasi yang tercakup radius layanan Minimarket X

<img width="3507" height="2480" alt="Peta populasi minimarket X" src="https://github.com/user-attachments/assets/588648bb-a171-4c1e-b248-38a31aa672ac" />

-------------------------------------------------------------------------------------------------------------------------

## Peta hasil populasi yang tercakup radius layanan Minimarket Y

<img width="3507" height="2480" alt="peta populasi minimarket Y" src="https://github.com/user-attachments/assets/b36826fc-b2b8-4de6-834b-0df36f9767ab" />

--------------------------------------------------------------------------------------------------------------------------

## Hasil Zonal Statistics Populasi Penduduk Berdasarkan Radius Buffer Minimarket

<img width="649" height="149" alt="tabel minimarket x" src="https://github.com/user-attachments/assets/f5d0b6d4-c0d3-4a21-a35b-8aa134625817" />
<img width="647" height="142" alt="tabel minimarket y" src="https://github.com/user-attachments/assets/b4a27f02-43ba-4339-86a5-29575bae6bda" />

--------------------------------------------------------------------------------------------------------------------------

Penulis

Melvin Marly

Program Studi Sistem Informasi

Universitas Bakrie

2026
