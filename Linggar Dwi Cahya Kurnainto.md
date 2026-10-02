Bagian B - Laporan Dokumentasi Perhitungan Manual Tsukamoto
NIM: 2415354009
Nama: linggar dwi cahya kurnianto
Input Uji Coba: Pengalaman Kerja = 4.0 Tahun, Nilai Ujian = 6.7

Langkah 1: Menghitung Derajat Keanggotaan (Fuzzifikasi)

Pada tahap ini, kita masukkan nilai input riil ke dalam rumus fungsi keanggotaan linier untuk mendapatkan nilai derajat keanggotaan (skala 0 sampai 1).

1. Variabel Pengalaman Kerja (4.0 Tahun)

    Himpunan Sedikit (Rentang 5 sampai 15 tahun):
    Karena input 4.0 tahun di bawah atau sama dengan batas bawah (5 tahun), maka nilainya 1.00.

    Himpunan Banyak (Rentang 10 sampai 20 tahun):
    Karena input 4.0 tahun di bawah batas minimal (10 tahun), maka nilainya 0.00.


2. Variabel Nilai Ujian (6.7)

    Himpunan Rendah:
    Karena nilai 6.7 lebih tinggi dari batas maksimal kategori rendah, maka nilainya 0.00.

    Himpunan Sedang:
    Berdasarkan fungsi keanggotaan pada program, nilai 6.7 berada pada kurva naik kategori Sedang.
    Hasil: 0.65 (artinya nilai 6.7 berada di posisi 65% pada skala Sedang).

    Himpunan Tinggi (Rentang 5 sampai 10):
    Angka 6.7 berada di antara rentang naik 5 sampai 10.

    1. Kurangi input dengan batas bawah: 6.7 - 5 = 1.7
    2. Cari lebar rentang domain: 10 - 5 = 5
    3. Bagi hasil langkah 1 dengan langkah 2: 1.7 / 5 = 0.34
    Hasil: 0.34 (artinya nilai 6.7 berada di posisi 34% pada skala Tinggi).


Langkah 2: Evaluasi Aturan (Alpha Predikat) dan Nilai Z

Pada metode Tsukamoto, setiap aturan menggunakan kondisi AND, sehingga kita mengambil nilai derajat terkecil (minimum). Nilai Z (gaji) kemudian dihitung menggunakan rumus kebalikan (inversi) dari rentang Gaji Rp1.000.000 sampai Rp20.000.000 (selisihnya Rp19.000.000).

Rumus Inversi Gaji Kecil: Z = 20.000.000 - (Alpha x 19.000.000)
Rumus Inversi Gaji Besar: Z = 1.000.000 + (Alpha x 19.000.000)

Penjelasan Hitungan per Aturan:

1. Rule 1 (JIKA Pengalaman Sedikit DAN Nilai Rendah MAKA Gaji Kecil):
    Cari Alpha 1: Ambil nilai terkecil antara Sedikit (1.00) dan Rendah (0.00) -> min(1.00, 0.00) = 0.00
    Cari Z1: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

2. Rule 2 (JIKA Pengalaman Sedikit DAN Nilai Sedang MAKA Gaji Kecil):
    Cari Alpha 2: Ambil nilai terkecil antara Sedikit (1.00) dan Sedang (0.65) -> min(1.00, 0.65) = 0.65
    Cari Z2:
      1. Kalikan Alpha dengan selisih gaji: 0.65 x 19.000.000 = 12.350.000
      2. Kurangi dari gaji maksimal (20 juta): 20.000.000 - 12.350.000 = 7.650.000
    Hasil Z2: Rp 7.650.000

3. Rule 3 (JIKA Pengalaman Sedikit DAN Nilai Tinggi MAKA Gaji Kecil):
    Cari Alpha 3: Ambil nilai terkecil antara Sedikit (1.00) dan Tinggi (0.34) -> min(1.00, 0.34) = 0.34
    Cari Z3:
      1. Kalikan Alpha dengan selisih gaji: 0.34 x 19.000.000 = 6.460.000
      2. Kurangi dari gaji maksimal (20 juta): 20.000.000 - 6.460.000 = 13.540.000
    Hasil Z3: Rp 13.540.000

4. Rule 4 (JIKA Pengalaman Banyak DAN Nilai Rendah MAKA Gaji Kecil):
    Cari Alpha 4: Ambil nilai terkecil antara Banyak (0.00) dan Rendah (0.00) -> min(0.00, 0.00) = 0.00
    Cari Z4: 20.000.000 - (0.00 x 19.000.000) = Rp 20.000.000

5. Rule 5 (JIKA Pengalaman Banyak DAN Nilai Sedang MAKA Gaji Besar):
    Cari Alpha 5: Ambil nilai terkecil antara Banyak (0.00) dan Sedang (0.65) -> min(0.00, 0.65) = 0.00
    Cari Z5: 1.000.000 + (0.00 x 19.000.000) = Rp 1.000.000

6. Rule 6 (JIKA Pengalaman Banyak DAN Nilai Tinggi MAKA Gaji Besar):
    Cari Alpha 6: Ambil nilai terkecil antara Banyak (0.00) dan Tinggi (0.34) -> min(0.00, 0.34) = 0.00
    Cari Z6: 1.000.000 + (0.00 x 19.000.000) = Rp 1.000.000


Langkah 3: Menghitung Defuzzifikasi (Rata-Rata Terbobot)

Langkah terakhir adalah menghitung nilai akhir dengan membagi total perkalian (Alpha x Z) dengan total seluruh nilai Alpha.

1. Hitung Bagian Atas (Perkalian Alpha x Z):
    Rule 1: 0.00 x 20.000.000 = 0
    Rule 2: 0.65 x 7.650.000 = 4.972.500
    Rule 3: 0.34 x 13.540.000 = 4.603.600
    Rule 4: 0.00 x 20.000.000 = 0
    Rule 5: 0.00 x 1.000.000 = 0
    Rule 6: 0.00 x 1.000.000 = 0
Total Bagian Atas: 0 + 4.972.500 + 4.603.600 + 0 + 0 + 0 = 9.576.100

2. Hitung Bagian Bawah (Total Nilai Alpha):
Total Alpha: 0.00 + 0.65 + 0.34 + 0.00 + 0.00 + 0.00 = 0.99

3. Pembagian Akhir:
    Bagi total bagian atas dengan total bagian bawah:
    9.576.100 / 0.99 = Rp 9.672.828,28