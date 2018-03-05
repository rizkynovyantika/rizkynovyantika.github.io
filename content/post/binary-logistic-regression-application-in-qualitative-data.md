---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.png"
date: 2018-02-26T13:19:28+07:00
title: "Analysis of Factors Affecting Waiting Time Getting Jobs with Binary Logistic Regression Methods Using R"
description: ""
draft: true

categories: []
tags: [stats, math, computer]

linktitle: "Analysis of Factors Affecting Waiting Time Getting Jobs with Binary Logistic Regression Methods Using R"
nomenu: "main"
noweight: 10
image: "img/sampling-2.jpg"
next: ""
prev: ""
---

# Analysis of Factors Affecting Waiting Time Getting Jobs With Binary Logistic Regression Methods Using R

With the same case as before, I write article about "Public Suggest: How to Get Job" and now I want to know what variable that significantly affects waiting time getting a job with Binary Logistic Regression Application Using R.

Dengan kasus yang sama seperti sebelumnya, saya menulis artikel tentang "Public Suggest: How to Get Job" dan sekarang saya ingin mengetahui variabel apa yang secara signifikan mempengaruhi waktu tunggu mendapatkan pekerjaan dengan metode Regresi Logistik Biner Menggunakan R.

Data yang digunakan dalam artikel ini merupakan data primer yang diambil sendiri dengan bantuan google drive. Data yang digunakan dalam artikel ini dapat anda unduh [disini](https://drive.google.com/open?id=1qlc_HK10ZY_W4uqz2DCGCYw1OwpdaJ4t)

Keterangan data :
1 = SS (Sangat Setuju)
2 = S (Setuju)
3 = TS (Tidak Setuju)
4 = STS (Sangat Tidak Setuju)

Lama waktu tunggu mendapatkan pekerjaan :
1 = 0-6 bulan
2 = > 6 bulan

Keterangan X1 sampai X20 merupakan variabel yang digunakan sebagai ukuran untuk mengetahui variabel apa saja yang dapat mempengaruhi waktu tunggu seseorang mendapatkan pekerjaan. Keterngan lebih rinci untuk masing-masing setiap variabel X dapat dilihat pada bagian akhir artikel ini.

## What is Binary Logistic Regression?

> Regresi logistik merupakan model regresi yang digunakan bila variabel responnya bersifat [kualitatif](https://rizkynovyantika.github.io/post/what-is-data/) - Hosmer dan Lemeshow, 1989

> Regresi logistik biner adalah suatu metode analisis data yang digunakan untuk mencari hubungan antara variabel respon (y) yang bersifat biner dengan variabel prediktor (x) 

## Test on Binary Logistic Regression 
Dalam melakukan analisis regresi logistik, dilakukan pengujian sebagai berikut :
1. Menguji Kelayakan Model Regresi
2. Menilai Keseluruhan Model (_Overall Model Fit Test_) 
3. Koefisien Determinasi (R2)
4. Pengujian Simultan (_Omnibus Test of Model Coefficient_)

### Menguji Kelayakan Model Regresi

### Menilai Keseluruhan Model (_Overall Model Fit Test_) 

### Koefisien Determinasi (R2)

### Pengujian Simultan (_Omnibus Test of Model Coefficient_)





#### Keterangan Variabel X
##### Variabel Akademik
X1 : Pernyataan [IPK mempengaruhi dalam mendapatkan pekerjaan]
X2 : Pernyataan [Lama kuliah IPK mempengaruhi dalam mendapatkan pekerjaan]
X3 : Pernyataan [Sering mengikuti kompetisi/lomba bidang akademik mempengaruhi dalam mendapatkan pekerjaan]
X4 : Pernyataan [Tingkat kompetisi/lomba yang diikuti mempengaruhi dalam mendapatkan pekerjaan]
X5 : Pernyataan [Sering mengikuti seminar sesuai dengan jurusan mempengaruhi dalam mendapatkan pekerjaan]

##### Variabel Organisasi
X6 : Pernyataan [Mengikuti organisasi mempengaruhi dalam mendapatkan pekerjaan]
X7 : Pernyataan [Jumlah organisasi yang diikuti selama kuliah mempengaruhi dalam mendapatkan pekerjaan]
X8 : Pernyataan [Jabatan di organisasi mempengaruhi dalam mendapatkan pekerjaan]

##### Variabel Kemampuan Bahasa
X9 : Pernyataan [Penguasaan Bahasa Inggris mempengaruhi dalam mendapatkan pekerjaan]
X10 : Pernyataan [Skor TOEFL mempengaruhi dalam mendapatkan pekerjaan]
X11 : Pernyataan [Penguasaan bahasa asing (selain bahasa inggris) mempengaruhi dalam mendapatkan pekerjaan]

##### Variabel Kemampuan Komputerisasi
X12 : Pernyataan [Penguasaan Microsoft Office mempengaruhi dalam mendapatkan pekerjaan]
X13 : Pernyataan [Penguasaan aplikasi-aplikasi yang sesuai jurusan mempengaruhi dalam mendapatkan pekerjaan]
X14 : Pernyataan [Penguasaan aplikasi-aplikasi diluar jurusan mempengaruhi dalam mendapatkan pekerjaan]
X15 : Pernyataan [Pernah mengikuti training/pelatihan aplikasi mempengaruhi dalam mendapatkan pekerjaan]

##### Variabel Kemampuan Komunikasi
X16 : Pernyataan [Kemampuan public speaking mempengaruhi dalam mendapatkan pekerjaan]
X17 : Pernyataan [Kemampuan berbicara/komunikasi dengan lawan bicara atau team mempengaruhi dalam mendapatkan pekerjaan]
X18 : Pernyataan [Kemampuan presentasi mempengaruhi dalam mendapatkan pekerjaan]

##### Variabel Magang (_Internship_)
X19 : Pernyataan [Pernah menjalani Magang atau PKL (Praktik Kerja Lapangan) mempengaruhi dalam mendapatkan pekerjaan]
X20 : Pernyataan [Penempatan kerja saat Magang atau PKL (Praktik Kerja Lapangan) mempengaruhi dalam mendapatkan pekerjaan]
