---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.jpg"
date: 2018-02-26T13:19:28+07:00
title: "Research Step for Object Detection Using Tensoflow"
description: ""
draft: false

categories: [deep learning]
tags: [stats, math, computer]

linktitle: "Research Step for Object Detection Using Tensoflow"
nomenu: "main"
noweight: 10
image: "img/plate.png"
next: ""
prev: ""
---

# Research Step for Object Detection Using Tensoflow

Salah satu yang mengalami perkembangan pesat pada bidang komputerisasi adalah _computer vision_. Dalam _computer vision_ terdapat beberapa permasalahan diantaranya adalah _Image classification_, _object detection_, dan _neural style transfer_. _Object detection_ dengan jaringan saraf tiruan ini masih berkembang sebagai teknologi untuk menduplikasi kemampuan manusia dalam memahami informasi dari sebuah gambar agar komputer dapat mengenali objek pada gambar selayaknya manusia. Lalu, bagaimana cara untuk membuat _object detection_ menggunakan Tensorflow?

![Figure 1](/images/research-step-for-object-detection-using-tensorflow/1.png)

Langkah-langkah yang digunakan untuk membuat deteksi objek menggunakan Tensorflow adalah sebagai berikut :

1. Tahap awal dimulai dengan mengumpulkan data gambar, pengumpulan data gambar dapat dilakukan dengan menggunakan aplikasi [Fatkun Batch Download Image](https://chrome.google.com/webstore/detail/fatkun-batch-download-ima/nnjjahlikiabnchcpehcpkdeckfgnohf) pada Chrome, [Image Downloader](https://id.wikihow.com/Mengunduh-Semua-Gambar-di-Halaman-Web) pada Chrome [DownThemAll](https://id.wikihow.com/Mengunduh-Semua-Gambar-di-Halaman-Web) atau pada Firefox.
Dalam hal ini saya merekomendasikan menggunakan Fatkun Batch Download Image karena penggunaannya lebih mudah khususnya dalam hal penentuan halaman yang akan di download gambarnya. Langkah-langkah untuk mengambil gambar menggunakan Fatkun Batch Download Image dapat dilihat [disini]()


2. Langkah selanjutnya adalah dilakukan pelabelan gambar atau _tracking costum object_, tahap ini dilakukan untuk mempermudah penentuan letak objek yang akan dideteksi. Pelabelan gambar dapat dilakukan menggunakan 




3. Setelah proses pelabelan perlu adanya konversi berkas dari XML ke CSV untuk tujuan konversi dataset ke berkas TFRecord 
4. Setelah proses konversi berkas XML dengan output berupa file CSV perlu adanya konversi ke TensorFlow Record file yang digunakan untuk feeding data pada proses pelatihan 
5. Kemudian dilakukan pembuatan label Map dan dataset (file TFRecord) yang sesuai dengan proses pelabelan data.
6. Sebelum dilakukan konfigurasi pipeline, terlebih dahulu dilakukan  
7. Kemudian langkah selanjutnya adalah konfigurasi object detection training pipeline untuk mengkonfigurasi proses pelatihan dan evaluasi yang dilakukan menggunakan berkas protobuf. Sebelum tahapan ini d

Sebelum tahap ini dilakukan terlebih dahulu dilakukan install dependencies,  Beberapa dependencies tersebut dapat dilihat [disini]()

7. Langkah selanjutnya adalah dilakukan proses training. 
	
	* Tahap awal pada proses pelatihan dimulai dengan Feeding data pelatihan atau memasukan data pelatihan ke dalam TensorFlow
	* Langkah selanjutnya yaitu dilakukan proses pelatihan data gambar untuk menghasilkan sistem pendeteksi objek Tanda Nomor Kendaraan Bermotor (TNKB) dengan menggunakan algoritma Convolutional Neural Network
	* Langkah selanjutnya adalah Pooling Layer yang digunakan untuk mengurangi dimensi dari downsampling, sehingga mempercepat komputasi karena parameter yang harus diupdate semakin sedikit dan mengatasi overfitting.
	* Kemudian dilakukan aktivasi menggunakan ReLU (Rectrified Linear Units) kemudian langkah untuk proses pelatihan
	* Setelah dilakukan aktivasi, kemudian akan menghasilkan output prediksi kelas yang berupa gambar hasil deteksi Tanda Nomor Kendaraan Bermotor (TNKB)

8. Ketika output dari hasil pelatihan menghasilkan tingkat akurasi yang rendah maka akan dilakukan proses pelatihan kembali, akan tetapi apabila output menghasilkan akurasi yang tinggi akan dilanjutkan dengan langkah selanjutnya.
9. Pada saat proses pelatihan maka akan menghasilkan checkpoint yang dibuat secara otomatis oleh TensorFlow berbentuk graph tensor yang bertujuan untuk menyimpan informasi proses pelatihan yang dilakukan, jika proses pelatihan selesai maka selanjutnya adalah mengeskpor graph tensor dan dijadikan model yang siap dipakai
10. Setelah proses pelatihan dilakukan maka akan menghasilkan model yang siap dipakai. 
11. Selanjutnya adalah pengujian data dengan program yang digunakan saat dilakukan pelatihan tetapi dengan jumlah data yang lebih sedikit. 
Kemudian dengan langkah yang sama, proses pengujian juga dilakukan dimulai dengan langkah Convolution dan diakhiri dengan output prediksi kelas yang berupa gambar hasil deteksi Tanda Nomor Kendaraan Bermotor (TNKB)
12. Setelah mendapatkan model yang sesuai dengan tingkat akurasi yang tinggi maka dilakukan interpretasi hasil dan pembahasan
13. Kesimpulan