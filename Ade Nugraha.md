LAPORAN PENGERJAAN MANUAL TSUKAMOTO
Nama:Ade Nugraha Sambara
NIM:2415354077

1. Tujuan

Menentukan perkiraan gaji pegawai baru menggunakan metode Fuzzy
Tsukamoto berdasarkan dua input:

-   Pengalaman kerja
-   Nilai ujian

Hasil akhir diperoleh melalui proses fuzzifikasi, evaluasi rule,
perhitungan nilai Z, dan defuzzifikasi.

2. Data yang Digunakan

Input

**Pengalaman Kerja** - Rentang: 0--25 tahun - Himpunan fuzzy: Sedikit
dan Banyak

**Nilai Ujian** - Rentang: 0--10 - Himpunan fuzzy: Rendah, Sedang, dan
Tinggi

Output

Gaji Pegawai - Rentang: Rp1.000.000--Rp20.000.000 - Himpunan fuzzy:
Kecil dan Besar

Nilai Input

Dari pengerjaan pada notebook:

-   Pengalaman kerja = 4 tahun
-   Nilai ujian = 6,7

3. Langkah Pengerjaan Manual

Langkah 1  Fuzzifikasi Pengalaman Kerja

Himpunan pengalaman kerja terdiri dari:

-   Sedikit
-   Banyak

Untuk pengalaman kerja 4 tahun:

Pengalaman Sedikit

Pada rentang 0--5 tahun, derajat keanggotaan masih penuh.

Maka:

μ Sedikit(4) = 1

Pengalaman Banyak

Himpunan Banyak mulai meningkat dari sekitar 10 tahun.

Karena pengalaman hanya 4 tahun:

**μ Banyak(4) = 0**

Jadi hasil fuzzifikasi pengalaman:

  Himpunan     Derajat Keanggotaan
  
  Sedikit                     1,00
  Banyak                      0,00

4. Fuzzifikasi Nilai Ujian

Nilai ujian yang digunakan adalah 6,7.

Himpunan nilai ujian:

-   Rendah
-   Sedang
-   Tinggi

Nilai Rendah
Pada nilai 6,7, derajat keanggotaan Rendah sudah mencapai 0.
μ Rendah(6,7) = 0

Nilai Sedang
Untuk nilai 6,7, bagian turun dari fungsi Sedang berada pada rentang
6--8.
Rumus:
μ Sedang(x) = (8 - x) / (8 - 6)
Masukkan x = 6,7:
μ Sedang(6,7) = (8 - 6,7) / 2
= 1,3 / 2
= 0,65

Nilai Tinggi
Untuk nilai 6,7, fungsi Tinggi berada pada rentang 5--10.
Rumus:
μ Tinggi(x) = (x - 5) / (10 - 5)
Masukkan x = 6,7:
μ Tinggi(6,7) = (6,7 - 5) / 5
= 1,7 / 5
= 0,34
Jadi hasil fuzzifikasi nilai ujian:

  Himpunan     Derajat Keanggotaan
  
  Rendah                      0,00
  Sedang                      0,65
  Tinggi                      0,34

5. Menentukan Rule Fuzzy

Terdapat 6 rule:

  Rule   Kondisi                                    Output
  
  R1     Jika pengalaman Sedikit dan nilai Rendah   Gaji Kecil
  R2     Jika pengalaman Sedikit dan nilai Sedang   Gaji Kecil
  R3     Jika pengalaman Sedikit dan nilai Tinggi   Gaji Kecil
  R4     Jika pengalaman Banyak dan nilai Rendah    Gaji Kecil
  R5     Jika pengalaman Banyak dan nilai Sedang    Gaji Besar
  R6     Jika pengalaman Banyak dan nilai Tinggi    Gaji Besar

Operator AND menggunakan nilai minimum.

Alpha = min(derajat pengalaman, derajat nilai)

6. Menghitung Alpha dan Nilai Z

R1

Pengalaman Sedikit = 1,00\
Nilai Rendah = 0,00

Alpha:

α1 = min(1,00 ; 0,00) = 0,00

Output = Gaji Kecil.

Karena alpha = 0, nilai Z:

Z1 = Rp20.000.000

R2

Pengalaman Sedikit = 1,00\
Nilai Sedang = 0,65

Alpha:

α2 = min(1,00 ; 0,65) = 0,65

Output = Gaji Kecil.

Untuk Gaji Kecil:

α = (20.000.000 - Z) / 19.000.000

Sehingga:

Z = 20.000.000 - (α × 19.000.000)

Masukkan α = 0,65:

Z2 = 20.000.000 - (0,65 × 19.000.000)

Z2 = 20.000.000 - 12.350.000

Z2 = Rp7.650.000

R3

Pengalaman Sedikit = 1,00\
Nilai Tinggi = 0,34

Alpha:

α3 = min(1,00 ; 0,34) = 0,34

Output = Gaji Kecil.

Z3 = 20.000.000 - (0,34 × 19.000.000)

Z3 = 20.000.000 - 6.460.000

Z3 = Rp13.540.000

R4

Pengalaman Banyak = 0,00\
Nilai Rendah = 0,00

Alpha:

α4 = min(0,00 ; 0,00) = 0,00

Output = Gaji Kecil.

Z4 = Rp20.000.000

R5

Pengalaman Banyak = 0,00\
Nilai Sedang = 0,65

Alpha:

α5 = min(0,00 ; 0,65) = 0,00

Output = Gaji Besar.

Untuk Gaji Besar:

α = (Z - 1.000.000) / 19.000.000

Sehingga:
Z = 1.000.000 + (α × 19.000.000)

Karena α = 0:

Z5 = Rp1.000.000

R6

Pengalaman Banyak = 0,00\
Nilai Tinggi = 0,34

Alpha:

α6 = min(0,00 ; 0,34) = 0,00

Output = Gaji Besar.

Z6 = 1.000.000 + (0 × 19.000.000)

Z6 = Rp1.000.000

7. Tabel Hasil Rule

  Rule     Alpha Output                Z
  
  R1        0,00 Kecil      Rp20.000.000
  R2        0,65 Kecil       Rp7.650.000
  R3        0,34 Kecil      Rp13.540.000
  R4        0,00 Kecil      Rp20.000.000
  R5        0,00 Besar       Rp1.000.000
  R6        0,00 Besar       Rp1.000.000


8. Defuzzifikasi

Metode Tsukamoto menggunakan rata-rata terbobot:

Z akhir = Σ(α × Z) / Σα

Jumlah alpha:

Σα = 0 + 0,65 + 0,34 + 0 + 0 + 0

Σα = 0,99

Jumlah alpha dikali Z:

Σ(α × Z)

= (0 × 20.000.000)\
+ (0,65 × 7.650.000)\
+ (0,34 × 13.540.000)\
+ (0 × 20.000.000)\
+ (0 × 1.000.000)\
+ (0 × 1.000.000)

= 4.972.500 + 4.603.600

= Rp9.576.100

Maka:

Z akhir = 9.576.100 / 0,99

Z akhir = Rp9.672.828,28

9. Kesimpulan

Berdasarkan perhitungan manual menggunakan metode Fuzzy Tsukamoto
dengan:

-   Pengalaman kerja = 4 tahun
-   Nilai ujian = 6,7

diperoleh hasil defuzzifikasi:
Gaji Pegawai Baru = Rp9.672.828,28
