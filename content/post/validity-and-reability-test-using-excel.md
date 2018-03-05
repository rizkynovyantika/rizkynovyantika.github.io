---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.png"
date: 2018-02-26T13:19:28+07:00
title: "Analysis of Factors Affecting Waiting Time Getting Jobs with Binary Logistic Regression Methods Using R"
description: ""
draft: true

categories: []
tags: [stats, math, computer]

linktitle: "Validity and Reability Using R"
nomenu: "main"
noweight: 10
image: "img/sampling-2.jpg"
next: ""
prev: ""
---

Data yang digunakan dalam artikel ini merupakan data primer yang diambil sendiri dengan bantuan google drive. Data yang digunakan dalam artikel ini dapat anda unduh [disini](https://drive.google.com/open?id=1qlc_HK10ZY_W4uqz2DCGCYw1OwpdaJ4t)

Keterangan data :
1 = SS (Sangat Setuju)
2 = S (Setuju)
3 = TS (Tidak Setuju)
4 = STS (Sangat Tidak Setuju)

Lama waktu tunggu mendapatkan pekerjaan :
1 = 0-6 bulan
2 = > 6 bulan

Keterangan X1 sampai X20 merupakan variabel yang digunakan sebagai ukuran untuk mengetahui variabel apa saja yang dapat mempengaruhi waktu tunggu seseorang mendapatkan pekerjaan. Keterangan lebih rinci untuk masing-masing setiap variabel X dapat dilihat pada bagian akhir artikel ini.

## Validitas dan Reabilitas Test 
Dalam penelitian, baik berbentuk kualitatif maupun kuantitatif, kriteria utama yang harus diperhatikan adalah valid, reliabel, dan objektif.

Validitas adalah derajat ketepatan antara data yang terdapat di lapangan dan data yang dilaporkan oleh peneliti. Kalau dalam objek penelitian terdapat warna merah, peneliti akan melaporkan warna merah. Kalau dalam objek penelitian para pegawai bekerja dengan keras, peneliti melaporkan bahwa pegawai bekerja dengan keras. Bila peneliti membuat laporan yang tidak sesuai dengan apa yang terjadi pada objek, data tersebut dapat dinyatakan tidak valid.

Pada dasarnya kegunaan data (setelah diolah dan dianalisis) ialah sebagai dasar yang objektif di dalam proses pembuatan keputusan – keputusan / kebijaksanaan – kebijaksanaan dalam rangka untuk memecahkan persoalan oleh pengambil keputusan. Keputusan yang baik hanya bisa diperoleh dari pengambil keputusan yang objektif, dan didasarkan atas data yang baik.

### Validitas
Perhitungan ini dilakukan untuk mengetahui sejauh mana alat ukur yang digunakan, dalam hal ini kuesioner memberikan hasil yang akurat dari data yang diukur. Kuesioner dianggap tidak valid apabila ada satu atau lebih jawaban yang kosong pada kuesioner, ada lebih dari satu jawaban yang diisi dalam satu pertanyaan. Ketentuan suatu kuesioner dikatakan valid apabila: r hitung > r tabel. Dan apabila variabel tidak valid maka variabel tersebut dihilangkan atau dibuang Jonathan Sarwono (2006).

Tahap selanjutnya dilakukan uji reliabilitas, reliabilitas adalah keandalan alat ukur. Dimana untuk mengetahui keandalan kuesioner sebagai alat ukur yang digunakan dalam penelitian ini maka dilakukan uji keandalan alat ukur dengan menggunakan koefesien keandalan Alpha Cronbach.