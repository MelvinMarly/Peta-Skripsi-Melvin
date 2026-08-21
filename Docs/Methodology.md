## Metodologi

---

## Buffer Analysis

Buffer Analysis digunakan untuk membentuk zona berdasarkan jarak tertentu dari titik lokasi minimarket.

Dalam penelitian ini, setiap titik Minimarket X dan Minimarket Y diberikan zona buffer dengan radius: **500 meter**
Radius 500 meter digunakan sebagai batas analisis spasial untuk mengidentifikasi cakupan radius layanan minimarket terhadap populasi penduduk.

## Union

Proses Union ini digunakan untuk mengintegrasikan dua atau lebih layer 
poligon vektor ke dalam satu berkas data spasial yang terpadu. Berbeda dengan operasi 
penggabungan biasa, proses ini memotong area yang saling tumpang tindih 
(overlapping) dan membentuk poligon-poligon baru, dengan tetap mempertahankan 
seluruh atribut dari kedua layer asal.

## Dissolve

Proses dissolve digunakan untuk mengintegrasikan kumpulan area dari fitur 
titik (point) berdasarkan kesamaan nilai atributnya, guna menghasilkan satu kesatuan 
ruang wilayah yang bebas dari batas-batas internal.

## Symmetrical Difference 

Proses symmetrical difference ini digunakan untuk membandingkan dua layer 
poligon dan mengekstrak area yang tidak saling tumpang tindih (non-overlapping). 
Proses ini akan secara otomatis menghapus area irisan tempat kedua layer saling 
beririsan, sehingga hanya mempertahankan wilayah yang secara eksklusif milik 
masing-masing layer.

## Zonal Statistics

Proses Zonal Statistic ini digunakan untuk menghitung dan mengekstrak nilai
nilai statistik dari data raster berdasarkan pembagian wilayah atau zona dari data vektor. Hasil dari proses ini berupa nilai akumulasi yang tersimpan pada tabel atribut layer.

---


