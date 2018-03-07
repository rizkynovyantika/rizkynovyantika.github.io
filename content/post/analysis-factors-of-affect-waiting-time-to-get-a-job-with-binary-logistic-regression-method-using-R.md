---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.png"
date: 2018-02-26T13:19:28+07:00
title: "Analysis Factors of Affect Waiting Time to Get a Job with Binary Logistic Regression Method Using R"

description: ""
draft: true

categories: []
tags: [stats, math, computer]

linktitle: "Analysis Factors of Affect Waiting Time to Get a Job with Binary Logistic Regression Method Using R"
nomenu: "main"
noweight: 10
image: "img/sampling-2.jpg"
next: ""
prev: ""
---

# Analysis Factors of Affect Waiting Time to Get a Job with Binary Logistic Regression Method Using R

With the same case as before, I write article about "Public Suggest: How to Get Job" and now I want to know what variable that significantly affects waiting time getting a job with Binary Logistic Regression Method Using R.

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

Keterangan X1 sampai X20 merupakan variabel yang digunakan sebagai ukuran untuk mengetahui variabel apa saja yang dapat mempengaruhi waktu tunggu seseorang mendapatkan pekerjaan. Keterangan lebih rinci untuk masing-masing setiap variabel X dapat dilihat [disini](variabel-explanation-of-waiting-time-to-get-job-research).

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