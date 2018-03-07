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

Sebelum masuk kedalam tahap analisis logistik regresi biner, sebaiknya data kuisioner dilakukan uji validitas dan reabilitas. Hasil pengujian validitas dan reabilitas pada data yang digunakan dalam artikel ini telah dibahas pada artikel sebelumnya. Anda dapat melihatnya [disini](https://rizkynovyantika.github.io/post/validity-and-reability-test-using-excel/)


## What is Binary Logistic Regression?

> Regresi logistik merupakan model regresi yang digunakan bila variabel responnya bersifat [kualitatif](https://rizkynovyantika.github.io/post/what-is-data/) - Hosmer dan Lemeshow, 1989

> Regresi logistik biner adalah suatu metode analisis data yang digunakan untuk mencari hubungan antara variabel respon (y) yang bersifat biner dengan variabel prediktor (x) 

## Binary Logistic Regression 
Sebelum masuk kedalam tahap analisis, hal yang pertama dilakukan adalah menginputkan data. Penginputan data dapat dilakukan dengan menggunakan syntax seperti dibawah ini :

```R
data=read.delim("clipboard")
View(data)
data$akademik<-factor(data$akademik)
data$organisasi<-factor(data$organisasi)
data$bahasa<-factor(data$bahasa)
data$komputer<-factor(data$komputer)
data$komunikasi<-factor(data$komunikasi)
data$magang<-factor(data$magang)

data$cakademik <-data$akademik-mean(data$akademik)
data$corganisasi <-data$organisasi-mean(data$organisasi)
data$cbahasa <-data$bahasa-mean(data$bahasa)
data$ckomputer <-data$komputer-mean(data$komputer)
data$ckomunikasi <-data$komunikasi-mean(data$komunikasi)
```

Kemudian memanggil beberapa package yang digunakan dalam proses analisis. Pda analisis regresi logistik biner menggunakan tiga package yaitu LOGIT, MASS dan rms. Berikut ini adalah syntax yang digunakan untuk memanggil package yang akan digunakan :

```R
library(LOGIT)
library(MASS)
library(rms)
```

### Estimasi Parameter
Estimasi parameter regresi logistik dengan menggunakan MLE (_Maximum Likelihood Estimator_). Taraf signifikansi yang digunakan adalah 5%. Variabel dapat dikatakan signifikan apabila nilai p-value lebih dari α (0.05). 
Berikut ini adalah syntax yang digunakan untuk menghitung estimasi parameter menggunakan sofware R :

Berikut ini adalah output dari syntax estimasi parameter

gambar

Dari gambar diatas, didapatkan bahwa variabel akademik, organisasi, kemampuan berbahasa, kemampuan komputerisasi, dan kemampuan komunikasi masing-masing memiliki nilai p-value > α (0.05), yang berarti variabel-variabel tersebut tidak signifikan untuk masuk kedalam model. Sedangkan variabel pengalaman magang memiliki p-value < α (0.05), yang berarti variabel tersebut signifikan untuk masuk kedalam model. 
Dikarenakan banyak variabel yang tidak signifikan, dilakukan pengujian variabel dependen dengan settiap variabel independen. Namun, didapatkan bahwa kelima variabel tetap tidak signifikan untuk dimasukkan kedalam model.

### Signifikansi Parameter

Pengujian signifikansi parameter untuk mengetahui variabel-variabel independen apa saja yang memiliki pengaruh signifikan terhadap lama waktu tunggu seorang alumni universitas dalam mendapatkan pekerjaan. Pengujian akan dilakukan secara overall dan parsial. 
Pengujian overall dengan menggunakan distribusi chi-square dan uji parsial dengan menggunakan uji wald. Pada uji overall, variabel independen dikatakan berpengaruh terhadap variabel dependen apabila nilai p-value lebih kecil dari α (0.05). Pada uji parsial, variabel independen dikatakan berpengaruh terhadap variabel dependen apabila .

gambar

Gambar diatas merupakan hasil untuk analisis overall. Dari gambar diatas, didapatkan nilai p-value sebesar 0.0020. Nilai p-value < α (0.05), sehingga keputusannya tolak  , yang berarti minimal ada satu variabel independen berpengaruh terhadap variabel dependen. 

gambar


Gambar diatas merupakan hasil untuk analisis parsial. Dari gambar diatas, didapatkan nilai W sebesar 2.87. Nilai W >., sehingga keputusannya tolak , yang berarti variabel independen (magang) berpengaruh terhadap variabel dependen (lama waktu tunggu).

### Model Regresi Logistik
Model regresi digunakan untuk mengetahui sebarapa besar pengaruh variabel independen terhadap variabel dependen. Model yang didapatkan adalah


### Uji Kesesuaian Model

Gambar diatas merupakan uji goodness of fit yang diguanakan untuk mengetahui apakah model telah sesuai. Model dikatakan sesuai apabila nilai p-value lebih besar dari . Dari gambar diatas didapatkan nilai p-value sebesar 0.08953, yang berarti model sesuai (tidak terdapat perbedaan yang signifikan antara hasil pengamatan dengan kemungkinan hasil prediksi model.



#------------------------------------------------------------------------------

## Test on Binary Logistic Regression 
Dalam melakukan analisis regresi logistik, dilakukan pengujian sebagai berikut :
1. Menguji Kelayakan Model Regresi
2. Menilai Keseluruhan Model (_Overall Model Fit Test_) 
3. Koefisien Determinasi (R2)
4. Pengujian Simultan (_Omnibus Test of Model Coefficient_)

### Menguji Kelayakan Model Regresi
Pengujian kelayakan model regresi logistik dinilai dengan menggunakan Hosmer and Lemeshow’s Goodness of Fit Test Goodness yang diukur dengan nilai Chi-square. Hosmer and Lemeshow’s Goodness of Fit Test Goodness menguji hipotesis nol bahwa data empiris cocok atau sesuai dengan model (tidak ada perbedaan antara model dengan data sehingga model dapat dikatakan fit). Jika nilai statistik Hosmer and Lemeshow’s Goodness of Fit Test sama dengan atau kurang dari 0.05, maka hipotesis nol ditolak yang berarti ada perbedaan signifikan antara model dengan nilai observasinya sehingga Goodness of Fit Test tidak baik karena model tidak dapat memprediksi nilai observasinya. Jika nilai statistik Hosmer and Lemeshow’s Goodness of Fit Test lebih besar dari 0.05, maka hipotesis nol diterima dan berarti model mampu memprediksi nilai observasinya atau dapat dikatakan model dapat diterima karena cocok dengan data observasinya.


Gambar diatas merupakan uji goodness of fit yang diguanakan untuk mengetahui apakah model telah sesuai. Model dikatakan sesuai apabila nilai p-value lebih besar dari . Dari gambar diatas didapatkan nilai p-value sebesar 0.08953, yang berarti model sesuai (tidak terdapat perbedaan yang signifikan antara hasil pengamatan dengan kemungkinan hasil prediksi model.

### Menilai Keseluruhan Model (_Overall Model Fit Test_) 
Uji ini digunakan untuk menilai model yang telah dihipotesiskan telah fit atau tidak dengan data. Pengujian dilakukan dengan membandingkan nilai antara -2 log likelihood pada awal (block number = 0) dengan nilai -2 log likelihood pada akhir (block number = 1). Adanya pengurangan nilai antara -2LL awal (initial -2LL function) dengan nilai -2LL pada langkah berikutnya (-2LL akhir) menunjukkan bahwa model yang dihipotesiskan fit dengan data.

### Koefisien Determinasi (R2)
Pegujian koefisien determinasi pada regresi logistik dengan menggunakan Nagelkerke’s R square. Tujuan dari pengujian ini adalah untuk mengetahui seberapa besar kombinasi variabel independen yaitu kompetensi aparatur dan kepemimpinan mampu menjelaskan variasi variabel dependen yaitu ketepatan waktu penyampaian pelaporan keuangan.

### Pengujian Simultan (_Omnibus Test of Model Coefficient_)
Pengujian ini dilakukan untuk menguji apakah variabel-variabel independen yang terdiri dari kompetensi aparatur dan kepemimpinan secara simultan berpengaruh terhadap variabel dependen yaitu ketepatan waktu penyampaian pelaporan keuangan.
Pengujian hipotesis dilakukan dengan cara membandingkan antara nilai probabilitas (sig) dengan tingkat signifikansi (α). Untuk menentukan penerimaan atau penolakan H0 didasarkan pada tingkat signifikansi (α) 5% dengan kriteria :

1. H0 tidak akan ditolak apabila statistik Wald hitung < Chi- square tabel, dan nilai probabilitas (sig) > tingkat signifikansi (α). Hal ini berarti H alternatif ditolak atau hipotesis yang menyatakan veriabel bebas berpengaruh terhadap variabel terikat ditolak.
2. H0 ditolak apabila statistik Wald hitung > Chi-square tabel, dan nilai probabilitas (sig) < tingkat signifikansi (α). Hal ini berarti H alternatif diterima atau hipotesis yang menyatakan variabel bebas berpengaruh terhadap variabel terikat diterima.