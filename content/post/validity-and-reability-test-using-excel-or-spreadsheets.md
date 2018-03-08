---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.jpg"
date: 2018-02-26T13:19:28+07:00
title: "Validity and Reability Test Using Excel"
description: ""
draft: false

categories: []
tags: [stats, math, computer]

linktitle: "Validity and Reability Test Using Excel"
nomenu: "main"
noweight: 10
image: "img/validity.jpg"
next: ""
prev: ""
---

Data yang digunakan dalam artikel ini merupakan data primer yang diambil sendiri dengan bantuan google drive. Data yang digunakan dalam artikel ini dapat anda unduh [disini](https://drive.google.com/open?id=13VPdsvQ2FqPcTLLaauYDTZ1NaBWeZWvQ)

Keterangan data :
1 = SS (Sangat Setuju)
2 = S (Setuju)
3 = TS (Tidak Setuju)
4 = STS (Sangat Tidak Setuju)

Lama waktu tunggu mendapatkan pekerjaan :
1 = 0-6 bulan
2 = > 6 bulan

Keterangan X1 sampai X20 merupakan variabel yang digunakan sebagai ukuran untuk mengetahui variabel apa saja yang dapat mempengaruhi waktu tunggu seseorang mendapatkan pekerjaan. Keterangan lebih rinci untuk masing-masing setiap variabel X dapat [disini](https://rizkynovyantika.github.io/post/variabel-explanation-of-waiting-time-to-get-job-research/)

## Pengertian Validitas, Reabilitas dan Objektif
Dalam penelitian, baik berbentuk kualitatif maupun kuantitatif, kriteria utama yang harus diperhatikan adalah valid, reliabel, dan objektif. 

### Validitas
> Validitas adalah derajat ketepatan antara data yang terdapat di lapangan dan data yang dilaporkan oleh peneliti.

Kalau dalam objek penelitian terdapat warna merah, peneliti akan melaporkan warna merah. Kalau dalam objek penelitian para pegawai bekerja dengan keras, peneliti melaporkan bahwa pegawai bekerja dengan keras. Bila peneliti membuat laporan yang tidak sesuai dengan apa yang terjadi pada objek, data tersebut dapat dinyatakan tidak valid.

### Reabilitas
> Reliabilitas adalah keandalan alat ukur. Dimana untuk mengetahui keandalan kuesioner sebagai alat ukur yang digunakan dalam penelitian ini maka dilakukan uji keandalan alat ukur dengan menggunakan koefesien keandalan Alpha Cronbach.

### Objektif
Pada dasarnya kegunaan data (setelah diolah dan dianalisis) ialah sebagai dasar yang objektif di dalam proses pembuatan keputusan – keputusan / kebijaksanaan – kebijaksanaan dalam rangka untuk memecahkan persoalan oleh pengambil keputusan. Keputusan yang baik hanya bisa diperoleh dari pengambil keputusan yang objektif, dan didasarkan atas data yang baik.

## Menghitung Validitas Menggunakan Excel atau Spreadsheets
Perhitungan validitas dalam sebuah instrumen dapat menggunakan rumus korelasi product moment atau dikenal juga dengan korelasi pearson. Adapun rumusnya sebagai berikut :

![Pearson](/images/validity-and-reability-test-using-excel-or-spreadsheets/0.jpg)

dimana :
r = rxy = koefisien korelasi
N = jumlah responden uji coba
X = skor tiap item
Y = skor seluruh item responden uji coba

Selanjutnya setelah harga koefisien validitas tiap butir soal diperoleh, kemudian hasilnya dibandingkan dengan nilai r dari tabel pada tingkat signifikan 5% dan tingkat signifikansi 1% dengan df= N-2. 

1. Menghitung dalam Excel atau Spreadsheets dengan menginput data hasil kuisioner dalam worksheet

2. Pada kolom paling kanan, terlebih dahulu kita jumlahkan total skor dari tiap responden menggunakan fungsi/rumus yang ada di excel, menggunakan perintah =sum(seluruh kolom cell yang akan dijumlahkan)
![Sum](/images/validity-and-reability-test-using-excel-or-spreadsheets/1.png)

3. Kemudian menghitung korelasi pearson.
	Pada baris paling bawah Rxy, setiap kolom item butir soal kita hitung nilai korelasi pearson-nya dengan rumus excel =pearson(array cell1; array cell2). Array cell 1 warna biru berisikan rentang sel item soal yang akan kita hitung dengan array cell2 warna hijau yang berisi rentang cell dengan jumlah nilai yang telah kita hitung sebelumnya, selanjutnya tekan enter. Untuk mengcopykan tinggal memakai symbol $ di aray sell 2
	![Pearson](/images/validity-and-reability-test-using-excel-or-spreadsheets/2.png)

4. Kemudian mencari nilai t-hitung
	Mencari nilai t-hitung dengan mendefinisikan sebuah rumus di excel, rumusnya dapat kita tuliskan sebagai berikut :
	![THitung](/images/validity-and-reability-test-using-excel-or-spreadsheets/t-hitung.jpg)
	Nilai n diisi dengan jumlah responden instrumen dalam angket adapun nilai rxy diisi dengan nilai korelasi yang telah dihitung sebelumnya. Di contoh ini responden nya sebanyak 83 orang.
	![Thitung](/images/validity-and-reability-test-using-excel-or-spreadsheets/3.png)

5. Nilai t-tabel dapat kita hitung dengan menggunakan rumus excel yaitu dengan cara menuliskan perintah =tinv(probability;degree of freedom).
	Probability diisi dengan tingkat signifikansi yang kita inginkan, misalkan saja jika kita menggunakan alpha=0,05 dengan dua arah, dan degree of freedom dengan derajat kebebasan yang nilainya = n-2.
	![Thitung](/images/validity-and-reability-test-using-excel-or-spreadsheets/4.png)

6. Dalam menentukan signifikan atau tidaknya sebuah validitas instrument dapat menggunakan perintah yang kita tulis pada baris di bawah perhitungan t-hitung yaitu dengan fungsi logika =IF(p>q;"valid";"tidak valid"). Nilai p berisikan nilai t-hitung dan nilai q nilai t-tabel.
![Thitung](/images/validity-and-reability-test-using-excel-or-spreadsheets/5.png)

## Menghitung Reabilitas Menggunakan Excel atau Spreadsheets

Reliabilitas adalah tingkat ketetapan suatu instrumen mengukur apa yang harus diukur. Ada tiga cara pelaksanaan untuk menguji reliabilitas suatu tes, yaitu: (1) tes tunggal (_single test_), (2) tes ulang (_test retest_), dan (3) tes ekuivalen (_alternate test_). Pada bahasan kali ini, kita hanya akan membahas tentang Reliabilitas Tes Tunggal (_Internal Consistency Reliability_).

Langkah-langkahnya adalah sebagai berikut:

1. Pisahkan  jawaban  responden  menjadi  item  bernomor  ganjil  dan  item  bernomor  genap  dan hitung jumlah total masing-masing kelompok. Pada data yang digunakan disini variabel yang merupakan item bernomor ganjil adalah X1, X3, X5, X7, X9, X11, X13, X15, X17, X19 sedangkan item yang merupakan kelompok genap adalah X2, X4, X6, X8, X10, X12, X14, X16, X18, X20 variabel sehingga hasil dari penjumlaha setiap kelompok adalah seperti gambar berikut :

![ganjilgenap](/images/validity-and-reability-test-using-excel-or-spreadsheets/6.png)

2. Menghitung nilai T-hitung dengan menggunakan rumus =CORREL(AG3:AG89;AH3:AH89) seperti gambar dibawah ini :

![ganjilgenap](/images/validity-and-reability-test-using-excel-or-spreadsheets/7.png)

3. Menghitung nilai T-tabel dengan menggunakan rumus =TINV(AF$93;AF$94)/SQRT(AF$94+(TINV(AF$93;AF$94))^2) seperti gambar dibawah ini :

![ganjilgenap](/images/validity-and-reability-test-using-excel-or-spreadsheets/8.png)

Berdasarkan gambar diatas diperoleh nilai r hitung =0,8726 > r tabel =0,2132, maka variabel yang digunakan dalam penelitian tersebut reliabel.