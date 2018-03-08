---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.jpg"
date: 2018-02-26T13:19:28+07:00
title: "Convolutional Neural Network Glossary"
description: ""
draft: false

categories: [deep learning]
tags: [stats, math, computer]

linktitle: "Convolutional Neural Network Glossary"
nomenu: "main"
noweight: 10
image: "img/deep.jpg"
next: ""
prev: ""
---

# Convolutional Neural Network Glossary

This glossary is work in progress and I am planning to continuously update it. If you find a mistake or think an important term is missing, please let me know via [email](https://rizkynovyantika.github.io/about/).

Deep Learning terminology can be quite overwhelming to newcomers. This glossary tries to define commonly used terms and link to original references and additional resources to help readers dive deeper into a specific topic.

### Class/Label
_Class_ atau _label_ merupakan variabel atau atribut yang digunakan dalam penelitian

### Gradient Descent
_Gradient descent_ merupakan algoritma yang digunakan untuk mengoptimalkan prosesiterasi yang digunakan pada Machine Learning untuk menemukan hasil yang terbaik

### Learning Rate
_Learning rate_ adalah Parameter dari _Gradient Descent_ 

### Loss Function 
Loss function merupakan nilai kerugian yang diperoleh dari proses training

### Epoch
_Epoch_ merupakan proses ketika seluruh dataset sudah melalui proses pelatihan pada Neural Network sampai dikembalikan ke awal untuk sekali putaran

### Batch Size
_Batch size_ merupakan jumlah sampel data yang disebarkan ke Neural Network atau ukuran dari satuan kecil _Epoch_ yang dimasukkan (feeding) kedalam komputer 

### Iterations
_Iteration_ merupakan jumlah batch yang diperlukan untuk menyelesaikan satu _Epoch_

### Feed Dictionary
_Feed Dictionary_ merupakan proses menyediakan data dengan TensorFlow Record (TFRecord) pada API Tensorflow

### Stride
_Stride_ merupakan parameter yang menentukan berapa jumlah pergeseran filter/kernel

### Padding
_Padding_ merupakan Parameter yang menentukan jumlah piksel yang berisi nilai nol yang akan ditambahkan disetiap sisi input.

### Dropout
_Dropout_ merupakan teknik regulasi jaringan saraf dimana beberapa neuron akan dipilih secara acak dan tidak dipakai selama proses pelatihan

### Step 
_Step_ merupakan sejumlah langkah yang didefinisikan pada konfigurasi pipeline untuk proses pelatihan yang menentukan tingkat keberhasilan pelatihan Neural Network 

### Filter/Kernel
Filter atau kernel adalah matriks untuk menghitung dan mendeteki suatu pola atau ciri yang digunakan untuk perhitungan konvolusi

### Checkpoint
_Checkpoint_ merupakan berkas yang dihasilkan dari proses pelatihan yang disimpan dalam format _.chkp_

### Prediction Confidence
_Prediction Confidence_ merupakan angka keberhasilan atau skor suatu pendeteksian berupa persentase 0-100%

### Model
Model adalah berkas hasil akhir yang siap didistribusikan untuk keperluan deteksi.