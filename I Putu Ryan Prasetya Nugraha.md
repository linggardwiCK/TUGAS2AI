## Bagian B - Laporan Dokumentasi Perhitungan Manual Tsukamoto
NIM:2415354061
Nama:I Putu Ryan Prasetya Nugraha 
Input Uji Coba: Pengalaman Kerja = 17.0 Tahun, Nilai Ujian = 8.5

Langkah 1: Menghitung Derajat Keanggotaan (Fuzzifikasi)

Pada tahap ini, kita masukkan nilai input riil ke dalam rumus fungsi keanggotaan linier untuk mendapatkan nilai derajat keanggotaan (skala 0 sampai 1).

1. Variabel Pengalaman Kerja (17.0 Tahun)

    Himpunan Sedikit (Rentang 5 sampai 15 tahun):
    Karena input 17.0 tahun sudah melewati batas maksimal (15 tahun), maka nilainya.

    Himpunan Banyak (Rentang 10 sampai 20 tahun):
    Angka 17.0 berada di antara rentang naik 10 sampai 20.
  
    1. Kurangi input dengan batas bawah: 17.0 - 10 = 7
    2. Cari lebar rentang domain: 20 - 10 = 10
    3. Bagi hasil langkah 1 dengan langkah 2: 7 / 10 = 0.70
    Hasil:0.70 (artinya input 17 tahun berada di posisi 70% pada skala Banyak).


#### 2. Variabel Nilai Ujian (8.5)

    Himpunan Rendah (Batas maksimal 5):
    Karena nilai 8.5 lebih tinggi dari batas maksimal (5), maka nilainya 0.

    Himpunan Sedang (Rentang 6 sampai 8):
    Karena nilai 8.5 sudah melebihi batas atas (8), maka nilainya 0.

    Himpunan Tinggi (Rentang 5 sampai 10):
    Angka 8.5 berada di antara rentang naik 5 sampai 10.
  
    1. Kurangi input dengan batas bawah: 8.5 - 5 = 3.5
    2. Cari lebar rentang domain: 10 - 5 = 5
    3. Bagi hasil langkah 1 dengan langkah 2: 3.5 / 5 = 0.70
    Hasil:0.70 (artinya nilai 8.5 berada di posisi 70% pada skala Tinggi).


### Langkah 2: Evaluasi Aturan (Alpha Predikat) dan Nilai Z

Pada metode Tsukamoto, setiap aturan menggunakan kondisi AND, sehingga kita mengambil nilai derajat terkecil (minimum). Nilai Z (gaji) kemudian dihitung menggunakan rumus kebalikan (inversi) dari rentang Gaji Rp1.000.000 sampai Rp20.000.000 (selisihnya Rp19.000.000).

Rumus Inversi Gaji Kecil: Z = 20.000.000 - (Alpha x 19.000.000)
Rumus Inversi Gaji Besar: Z = 1.000.000 + (Alpha x 19.000.000)

#### Penjelasan Hitungan per Aturan:

1. Rule 1 (JIKA Pengalaman Sedikit DAN Nilai Rendah MAKA Gaji Kecil):
    Cari Alpha 1: Ambil nilai terkecil antara Sedikit (0.00) dan Rendah (0.00) -> min(0.00, 0.00) = 0.00
    Cari Z1: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

2. Rule 2 (JIKA Pengalaman Sedikit DAN Nilai Sedang MAKA Gaji Kecil):
    Cari Alpha 2: Ambil nilai terkecil antara Sedikit (0.00) dan Sedang (0.00) -> min(0.00, 0.00) = 0.00
    Cari Z2: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

3. Rule 3 (JIKA Pengalaman Sedikit DAN Nilai Tinggi MAKA Gaji Kecil):
    Cari Alpha 3: Ambil nilai terkecil antara Sedikit (0.00) dan Tinggi (0.70) -> min(0.00, 0.70) = 0.00
    Cari Z3: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

4. Rule 4 (JIKA Pengalaman Banyak DAN Nilai Rendah MAKA Gaji Kecil):
    Cari Alpha 4: Ambil nilai terkecil antara Banyak (0.70) dan Rendah (0.00) -> min(0.70, 0.00) = 0.00
    Cari Z4: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

5. Rule 5 (JIKA Pengalaman Banyak DAN Nilai Sedang MAKA Gaji Besar):
    Cari Alpha 5: Ambil nilai terkecil antara Banyak (0.70) dan Sedang (0.00) -> min(0.70, 0.00) = 0.00
    Cari Z5: 1.000.000 + (0.00 x 19.000.000) = Rp 1.000.000

6. Rule 6 (JIKA Pengalaman Banyak DAN Nilai Tinggi MAKA Gaji Besar):
    Cari Alpha 6: Ambil nilai terkecil antara Banyak (0.70) dan Tinggi (0.70) -> min(0.70, 0.70) = 0.70
    Cari Z6:
     1. Kalikan Alpha dengan selisih gaji: 0.70 x 19.000.000 = 13.300.000
     2. Tambahkan ke gaji minimal (1 juta): 1.000.000 + 13.300.000 = 14.300.000
    Hasil Z6: Rp 14.300.000



### Langkah 3: Menghitung Defuzzifikasi (Rata-Rata Terbobot)

Langkah terakhir adalah menghitung nilai akhir dengan membagi total perkalian (Alpha x Z) dengan total seluruh nilai Alpha.

#### 1. Hitung Bagian Atas (Perkalian Alpha x Z):
    Rule 1: 0.00 x 20.000.000 = 0
    Rule 2: 0.00 x 20.000.000 = 0
    Rule 3: 0.00 x 20.000.000 = 0
    Rule 4: 0.00 x 20.000.000 = 0
    Rule 5: 0.00 x 1.000.000 = 0
    Rule 6: 0.70 x 14.300.000 = 10.010.000
Total Bagian Atas: 0 + 0 + 0 + 0 + 0 + 10.010.000 = 10.010.000

#### 2. Hitung Bagian Bawah (Total Nilai Alpha):
Total Alpha: 0.00 + 0.00 + 0.00 + 0.00 + 0.00 + 0.70 = 0.70

#### 3. Pembagian Akhir:
    Bagi total bagian atas dengan total bagian bawah:
  10.010.000 / 0.70 = Rp.14.300.000

