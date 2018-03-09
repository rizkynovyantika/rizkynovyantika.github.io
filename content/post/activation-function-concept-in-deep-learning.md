---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.jpg"
date: 2018-02-26T13:19:28+07:00
title: "Simple Convolutional Neural Network Concept"
description: ""
draft: false

categories: [deep learning]
tags: [stats, math, computer]

linktitle: "Simple Convolutional Neural Network Concept"
nomenu: "main"
noweight: 10
image: "img/deep.jpg"
next: ""
prev: ""
---

# Simple Convolutional Neural Network Concept

Convolutional Neural Network merupakan subtipe dari Artificial Neural Network. Munculnya Artificial Neural Network dikarenakan adanya kebutuhan penyelesaian permasalahan pada domain Machine Learning. Permasalahan-permasalahan tersebut dapat diselesaikan dengan berbagai macam algoritma, tergantung permasalahan yang muncul pada Machine Learning yang dibuat.

Algoritma yang digunakan untuk menyelesaikan permasalahan pada domain Machine Learning tersebut semakin berkembang dengan adanya sifat ketidakpuasan manusia. Salah satu algoritma yang berkembang tersebut adalah MLP (Multilayer Perceptron) yang kemudian dikembangkan menjadi Convolutional Neural Network.

Convolutional Neural Network yang merupakan subtipe dari Artificial Neural Network merupakan model yang terinspirasi dari bagaimana neuron manusia bekerja yaitu dengan neuron. Neuron adalah sel saraf yang berfungsi menghantarkan impuls listrik yang terbentuk akibat adanya suatu stimulus atau rangsangan. Dimana setiap neuron tersebut saling terhubung dan informasi mengalir dari setiap neuron. 

[Figure 1](/images/simple-convolutional-neural-network-concept/1.jpg)

Keterangan Neuron  :
* **Dendrites** bertugas untuk menerima dan mengantarkan impuls (rangsangan) ke cell body.
* **Cell Body** bertugas untuk menerima impuls (rangsangan) dari dendrites dan meneruskannya ke axon.
* **Nucleus** merupakan inti sel yang bertugas untuk mengatur kegiatan sel saraf (neuron) dan mengatur sifat keturunan dari sel tersebut.
* **Axon** bertugas untuk menghantarkan impuls (rangsangan) dari cell body menuju efektor, seperti otot dan kelenjar.
* **Synapse** bertugas untuk menghantarkan impuls ke saraf selanjutnya

Secara umum, bagian-bagian Neuron tersebut terhubung bagian satu dengan bagian lainnya. Jika diaplikasikan dalam Artificial Neural Network, tiap neuron menerima input dan melakukan operasi dot dengan sebuah weight, menjumlahkannya (_weighted sum_) dan menambahkan bias. Hasil dari operasi ini akan dijadikan parameter dari _activation function_ yang akan dijadikan output dari neuron tersebut.

## Convolutional Neural Network
### Neural Network Architecture
Untuk mempermudah pemahaman arsitektur neural network, disini saya akan mengaplikasikan bagaimana arsitektur neural network secara umum pada proses pendeteksian tanda nomor kendaraan. 

[Figure 1](/images/simple-convolutional-neural-network-concept/2.jpg)

Pada arsitektur tersebut terdapat beberapa 3 layer secara umum yaitu input layer, hidden layer dan output layer. Berikut ini adalah penjelasan dari masing-masing layer tersebut :
1. **Input layer** merupakan seluruh data yang diperoleh dari gambar pada **image for detection**. Input layer merupakan seluruh node pixel gambar. Pada gambar tersebut terbagi menjadi 300x300 pixel, sehingga node yang terdapat pada input layer sebanyak 90.000 node, akan tetapi keterangan pada arsitektur tersebut adalah 270.000.000 yang diperoleh dari 90.000 node dari pixel asli yang dikalikan dengan 3 channel warna RGB (_Red, Green, Blue_) sehingga menghasilkan node sebanyak 270.000.000.

2. **Hidden layer** merupakan bagian pada neural network yang tidak ditampilkan, sehingga dinamakan sebagai hidden layer. Pada hidden layer ini dilakukan proses perhitungan. Dalam hal ini perhitungan dilakukan untuk melakukan deteksi tanda nomor kendaraan. Pada hidden layer ini sebenarnya terdapat tiga proses untuk mendapatkan hasil deteksi tanda nomor kendaraan. Tiga proses tersebut adalah proses _convolution_, proses _activation_ dan proses _pooling_ layer.

3. **Output layer** merupakan hasil dari proses dari input layer dan hidden layer yang berupa _fully connected layer_ atau dengan kata lain adalah menggabungkan semua layer yang diperkirakan sebagai tanda nomor kendaraan.

### Convolution Layer
Konvolusi merupakan cara untuk mengkombinasikan dua buah deret angka yang menghasilkan deret angka yang ketiga. Dalam penelitian ini, dua buah deret angka tersebut terdapat dalam input dan kernel atau filter sedangkan deret angka yang ketiganya adalah output. Input dan kernel atau filter keduanya memiliki deret angka berupa matriks. Pada input deret angka diperoleh berdasarkan tingkat warna yang ada pada masing-masing piksel sedangkan pada kernel atau filter deret angka disesuaikan oleh kebutuhan peneliti. Terdapat beberapa jenis kernel atau filter yang biasa digunakan, diantaranya pada operasi identity, edge detection, sharpen, box blur, Gaussian blur dan lain sebagainya.
Lapisan konvolusi dibentuk dengan menjalankan filter di atasnya. Filter merupakan blok lain atau kubus dengan tinggi dan lebar yang lebih kecil namun kedalaman yang sama yang tersapu di atas gambar dasar atau gambar asli. Filter digunakan untuk menentukan pola apa yang akan dideteksi yang selanjutnya dikonvolusi atau dikalikan dengan nilai pada matriks input, nilai pada masing-masing kolom dan baris pada matriks sangat bergantung pada jenis pola yang akan dideteksi 
Untuk dapat lebih memahami cara kerja dari proses konvolusi, peneliti akan menggunakan sampel deret angka pada input dikarenakan keterbatasan penulisan dengan ukuran 300x300 maka peneliti menggunakan sampel deret angka pada input dengan ukuran 6x6 dan menggunakan kernel atau filter untuk operasi _vertical edge detection_ dengan ukuran 3x3. 
[Figure 1](/images/simple-convolutional-neural-network-concept/3.jpg)

Degan menggunakan filter 3x3 dengan strided atau langkah yang digunakan dalam perhitungan konvolusi tersebut adalah 1 maka proses perhitungan konvolusi tersebut dapat divisualisasikan seperti gambar dibawah ini :
[Figure 1](/images/simple-convolutional-neural-network-concept/4.jpg)

Perhitungan pada proses konvolusi dengan ukuran filter 3x3 ini dimulai dari sudut kiri atas kemudian dilakukan _sliding window_ sampai pojok kiri bawah. 

#### Activation Layer
Tahap ini adalah perhitungan nilai dengan _Activation Function_ yang digunakan untuk mencari nilai non-linier pada nilai hasil konvolusi. Secara umum, _Activation function_ dapat dibagi menjadi 2 tipe yaitu fungsi aktivasi linier dan fungsi aktivasi non linier. Penjelasan Activation Function dapat dilihat [disini]()

Activation Function yang digunakan dalam artikel ini menggunakan ReLu. Untuk lebih memahami ReLU dapat diilustrasikan dengan gambar dibawah ini :
[Figure 1](/images/simple-convolutional-neural-network-concept/5.jpg)

Kernel pertama (3 x 1) + (0 x 0) + (1 x (-1)) + (1 x 1) + (0 x 5) + (8 x (-1)) + (2 x 1) + (7 x 0) + (2 x (-1)) = -5, pada kernel kedua (3 x 0) + (0 x 0) + (1 x 0) + (1 x 0) + (5 x 1) + (8 x 0) + (2 x 0) + (7 x 0) + (2 x 0) = 5 dan pada kernel ketiga (3 x 0) + (0 x (-1)) + (1 x 0) + (1 x (-1)) + (5 x 5) + (8 x (-1)) + (2 x 0) + (7 x (-1)) + (2 x 0) = 9. Karena nilai tertinggi yang diperoleh menggunakan ketiga kernel tersebut, maka yang digunakan adalah angka 9 pada output selanjutnya, begitupun dengan kolom dan baris lainnya.

#### Pooling Layer
[Figure 1](/images/simple-convolutional-neural-network-concept/6.jpg)

Pooling layer pada Gambar diatas merupakan pooling layer dengan menggunakan metode Max Pooling. Pooling layer sendiri berguna untuk mengurangi ukuran gambar. Pada Gambar diatas terdapat lapisan dengan ukuran 6×6, apabila peneliti menggunakan filter 3x3 dengan stride 1 maka diperoleh hasil Max pooling dengan ukuran 4x4. 

#### Fully Connected Layer
[Figure 1](/images/simple-convolutional-neural-network-concept/7.jpg)

Menggunakan lapisan yang terhubung sepenuhnya di mana setiap piksel dianggap sebagai neuron terpisah seperti jaringan saraf biasa. Lapisan terakhir yang terhubung sepenuhnya akan mengandung banyak neuron sebagai jumlah kelas yang harus diprediksi. Pada proses fully connected layer ini penyatuan setiap piksel yang dianggap sebagai Tanda Nomor Kendaraan yang kemudian akan menjadi sebuah output yang terdiri dari satu label kelas yaitu Tanda Nomor Kendaraan Bermotor sehingga lapisan yang terhubung terakhir hanya memiliki 1 neuron.