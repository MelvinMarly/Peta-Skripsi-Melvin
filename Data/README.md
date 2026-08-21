
## Data

Data yang digunakan dalam penelitian terdiri dari:

| Dataset | Sumber | Fungsi |
|---|---|---|
| Lokasi Minimarket X | Indopaket / Google Maps | Titik input Buffer Analysis |
| Lokasi Minimarket Y | Google Maps | Titik input Buffer Analysis |
| Data populasi penduduk | Badan Pusat Statistik Kota Jakarta Utara | Analisis jumlah penduduk yang tercakup radius Buffer |
| Batas wilayah penelitian | gadm41_IDN | Clipping batas wilayah administrasi |

---
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

## Pembersihan dan Transformasi Data

Data lokasi minimarket terlebih dahulu dipersiapkan agar dapat digunakan sebagai data titik dalam QGIS. Data kemudian digunakan sebagai input Buffer Analysis dengan radius 500 meter.

Tahapan pengolahan spasial meliputi pembuatan Buffer, Dissolve, Union, Clip, Symmetrical Difference, dan Zonal Statistics sesuai kebutuhan analisis.

## Repository ini membedakan antara data raw dan data processed:

data "raw" berisi data yang diperoleh dari sumber awal sebelum dilakukan pengolahan dalam penelitian.
data "processed" berisi data yang telah dipersiapkan atau diolah sehingga dapat langsung digunakan dalam analisis QGIS.   



