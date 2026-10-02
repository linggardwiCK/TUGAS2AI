Bagian B - Perhitungan Manual Tsukamoto

NIM: 2415354053
Nama: I Made Wika Sastrawan

Input yang dipakai:
Pengalaman kerja = 12 tahun
Nilai ujian = 7.0

1. Perhitungan fuzzifikasi

Di bagian ini saya menghitung nilai keanggotaan untuk nilai ujian Sedang. Pada program, nilai Sedang memakai titik 2, 4, 6, dan 8. Karena nilai 7.0 ada di bagian menurun, maka perhitungannya seperti:

miu Sedang = (8 - nilai ujian) / (8 - 6)
miu Sedang = (8 - 7.0) / (8 - 6)
miu Sedang = 1 / 2
miu Sedang = 0,50

Jadi, nilai ujian 7.0 mempunyai nilai keanggotaan Sedang sebesar 0,50

Untuk menghitung salah satu rule yang dipilih, saya juga nilai keanggotaan pengalaman kerja Banyak. Pengalaman 12 tahun berada di bagian naik, yaitu antara 10 sampai 20 tahun

miu Banyak = (pengalaman - 10) / (20 - 10)
miu Banyak = (12 - 10) / (20 - 10)
miu Banyak = 2 / 10
miu Banyak = 0,20

Jadi, pengalaman kerja 12 tahun mempunyai nilai keanggotaan Banyak sebesar 0,20

Nilai keanggotaan lain yang dipakai untuk menghitung semua rule adalah:

miu Sedikit = (15 - 12) / (15 - 5) = 0,30
miu Rendah = 0,00, karena nilai ujian 7.0 sudah lebih dari 5
miu Tinggi = (7.0 - 5) / (10 - 5) = 0,40

2. Perhitungan alpha-predikat dan nilai z

- Rule 1:

IF Exp Sedikit AND nilai Rendah, MAKA gaji Kecil

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 1 = min(miu Sedikit, miu Rendah)
alpha 1 = min(0,30, 0,00)
alpha 1 = 0,00

Jadi, nilai alpha untuk Rule 1 adalah 0,00

Karena hasil dari Rule 1 adalah gaji Kecil, rumus nilai z yang dipakai adalah:

z 1 = 20.000.000 - (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 1 = 20.000.000 - (0,00 x 19.000.000)
z 1 = 20.000.000

Jadi, nilai z dari Rule 1 adalah Rp20.000.000.

- Rule 2:

IF Exp Sedikit AND nilai Sedang, MAKA gaji Kecil

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 2 = min(miu Sedikit, miu Sedang)
alpha 2 = min(0,30, 0,50)
alpha 2 = 0,30

Jadi, nilai alpha untuk Rule 2 adalah 0,30

Karena hasil dari Rule 5 adalah gaji Kecil, rumus nilai z yang dipakai adalah:

z 2 = 20.000.000 - (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 2 = 20.000.000 - (0,30 x 19.000.000)
z 2 = 20.000.000 - 5.700.000
z 2 = 14.300.000

Jadi, nilai z dari Rule 2 adalah Rp14.300.000.

- Rule 3:

IF Exp Sedikit AND nilai Tinggi, MAKA gaji Kecil

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 3 = min(miu Sedikit, miu Tinggi)
alpha 3 = min(0,30, 0,40)
alpha 3 = 0,30

Jadi, nilai alpha untuk Rule 3 adalah 0,30

Karena hasil dari Rule 3 adalah gaji Kecil, rumus nilai z yang dipakai adalah:

z 3 = 20.000.000 - (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 3 = 20.000.000 - (0,30 x 19.000.000)
z 3 = 20.000.000 - 5.700.000
z 3 = 14.300.000

Jadi, nilai z dari Rule 3 adalah Rp14.300.000.

- Rule 4:

IF Exp Banyak AND nilai Rendah, MAKA gaji Kecil

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 4 = min(miu Banyak, miu Rendah)
alpha 4 = min(0,20, 0,00)
alpha 4 = 0,00

Jadi, nilai alpha untuk Rule 4 adalah 0,00

Karena hasil dari Rule 4 adalah gaji Kecil, rumus nilai z yang dipakai adalah:

z 4 = 20.000.000 - (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 4 = 20.000.000 - (0,00 x 19.000.000)
z 4 = 20.000.000

Jadi, nilai z dari Rule 4 adalah Rp20.000.000.

- Rule 5:

IF Exp Banyak AND nilai Sedang, MAKA gaji Besar

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 5 = min(miu Banyak, miu Sedang)
alpha 5 = min(0,20, 0,50)
alpha 5 = 0,20

Jadi, nilai alpha untuk Rule 5 adalah 0,20

Karena hasil dari Rule 5 adalah gaji Besar, rumus nilai z yang dipakai adalah:

z 5= 1.000.000 + (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 5 = 1.000.000 + (0,20 x 19.000.000)
z 5 = 1.000.000 + 3.800.000
z 5 = 4.800.000

Jadi, nilai z dari Rule 5 adalah Rp4.800.000.

- Rule 6:

IF Exp Banyak AND nilai Tinggi, MAKA gaji Besar

Karena memakai operator AND, nilai alpha diambil dari nilai yang paling kecil

alpha 6 = min(miu Banyak, miu Tinggi)
alpha 6 = min(0,20, 0,40)
alpha 6 = 0,20

Jadi, nilai alpha untuk Rule 6 adalah 0,20

Karena hasil dari Rule 5 adalah gaji Besar, rumus nilai z yang dipakai adalah:

z 6 = 1.000.000 + (alpha x 19.000.000)

Selisih 19.000.000 berasal dari gaji tertinggi dikurangi gaji terendah, yaitu 20.000.000 - 1.000.000

z 6 = 1.000.000 + (0,20 x 19.000.000)
z 6 = 1.000.000 + 3.800.000
z 6 = 4.800.000

Jadi, nilai z dari Rule 6 adalah Rp4.800.000.

3. Perhitungan Defuzzifikasi

Rumus yang digunakan adalah:
z = Σ(alpha × z) / Σalpha

Berdasarkan hasil perhitungan sebelumnya, rule yang memiliki nilai alpha lebih dari 0 adalah Rule 2, Rule 3, Rule 5, dan Rule 6. Sedangkan Rule 1 dan Rule 4 memiliki nilai alpha = 0, Jadi nilai alpha dan z adalah:

Rule 1: alpha = 0,00 dan z = Rp20.000.000
Rule 2: alpha = 0,30 dan z = Rp14.300.000
Rule 3: alpha = 0,30 dan z = Rp14.300.000
Rule 4: alpha = 0,00 dan z = Rp20.000.000
Rule 5: alpha = 0,20 dan z = Rp4.800.000
Rule 6: alpha = 0,20 dan z = Rp4.800.000

Maka perhitungan defuzzifikasinya:
z = ((0,00 x 20.000.000) + (0,30 × 14.300.000) + (0,30 × 14.300.000) + (0,00 x 20.000.000) + (0,20 × 4.800.000) +  (0,20 × 4.800.000)) / (0,00 + 0,30 + 0,30 + 0,00 + 0,20 + 0,20)
z = (0 + 4.290.000 + 4.290.000 + 0 + 960.000 + 960.000) / 1,00
z = 10.500.000 / 1,00
z = 10.500.000

Jadi, hasil defuzzifikasi dari sistem fuzzy Tsukamoto untuk pengalaman kerja 12 tahun dan nilai ujian 7.0 adalah Rp10.500.000

Kesimpulan:

Nilai keanggotaan Sedang untuk nilai ujian 7.0 adalah 0,50.
Nilai alpha Rule 1 sampai Rule 6 adalah 0,00; 0,30; 0,30; 0,00; 0,20; dan 0,20.
Nilai z Rule 1 sampai Rule 6 adalah Rp20.000.000; Rp14.300.000; Rp14.300.000; Rp20.000.000; Rp4.800.000; dan Rp4.800.000.
Hasil defuzzifikasi jika pengalaman kerja 12 tahun dan nilai ujian 7.0 adalah Rp10.500.000