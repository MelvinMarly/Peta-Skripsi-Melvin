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

# Cara reproduksi

## Software

- Quantum Geographic Information System (QGIS 3.42.2)
- Processing Toolbox QGIS
- Tools Buffer
- Tools Dissolve
- Tools Union
- Tools Clip
- Tools Symmetrical Difference
- Zonal Statistics
