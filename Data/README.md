
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

- Data lokasi titik minimarket yang berawal dari data mentah di transformasi menjadi data spasial untuk melakukan proses buffer
- data raw yang digunakan adalah data batas wilayah seluruh administrasi kemudian di processed menjadi batas wilayah yang diperlukan

