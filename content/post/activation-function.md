---
author: "Rizky D. Novyantika"
authorAvatar: "/img/avatar.jpg"
date: 2018-02-26T13:19:28+07:00
title: "Activation Function Concept in Deep Learning"
description: ""
draft: false

categories: [deep learning]
tags: [stats, math, computer]

linktitle: "Activation Function Concept in Deep Learning"
nomenu: "main"
noweight: 10
image: "img/deep.jpg"
next: ""
prev: ""
---

# Activation Function Concept in Deep Learning

Activation function merupakan sebuah node yang ditambahkan ke akhir output dari setiap jaringan syaraf. Hal ini juga dikenal sebagai Transfer Function. Hal ini juga dapat dilampirkan di antara dua Neural Networks.  Activation function digunakan untuk menentukan output jaringan syaraf tiruan. Activation function memetakan nilai yang dihasilkan di antara 0 sampai 1 atau -1 sampai 1 dan lain-lain (tergantung pada fungsinya). Activation function pada dasarnya dapat dibagi menjadi 2 tipe yaitu fungsi aktivasi linier dan fungsi aktivasi non linier. (Sharma, 2017)

## Fungsi Aktivasi Linear
Seperti yang dapat dlihat fungsinya adalah garis atau linier. Oleh karena itu, output dari fungsi tidak akan dibatasi antara suatu rentang.

![Figure 1](/images/activation-function-concept-in-deep-learning/1.png)

Fungsi aktivasi pada linear function memiliki persamaan : f(x) = x dan Rentang : -tak hingga sampai tak hingga. Fungsi aktivasi linier ini tidak membantu dengan kompleksitas atau berbagai parameter data biasa yang diumpankan ke jaringan syaraf tiruan. (Sharma, 2017)

## Fungsi Aktivasi Non-Linear
Fungsi Aktivasi Nonlinear adalah fungsi aktivasi yang paling banyak digunakan. Nonlinier membantu membuat grafik terlihat seperti gambar dibawah ini :

![Figure 1](/images/activation-function-concept-in-deep-learning/2.png)

Fungsi aktivasi non linier memudahkan model untuk mengeneralisasi atau menyesuaikan dengan berbagai data dan untuk membedakan antara output. Terminologi utama yang perlu dipahami untuk fungsi nonlinier adalah Derivatif atau Diferensial dan Monotonik. Fungsi Derivatif atau Diferensial: Perubahan sumbu y w.r.t. Perubahan x-axis. Hal ini juga dikenal sebagai kemiringan dan fungsi Monotonik merupakan sebuah fungsi yang bervariasi sedemikian rupa sehingga tidak pernah berkurang atau tidak pernah meningkat. Berikut ini adalah fungsi Aktivasi Nonlinier berdasarkan rentang atau kurva (Sharma, 2017) :

1. **Sigmoid Activation Function**
	
	Sigmoid Activation Function disebut juga sebagai Logistic activation function. Kurva Fungsi Sigmoid terlihat seperti bentuk S. 

![Figure 1](/images/activation-function-concept-in-deep-learning/3.png)
	
	Alasan utama mengapa kita menggunakan fungsi sigmoid adalah karena ada antara (0 sampai 1). Oleh karena itu, ini terutama digunakan untuk model dimana kita harus memprediksi probabilitas sebagai keluaran. Karena probabilitas dari sesuatu yang ada hanya antara kisaran 0 dan 1, sigmoid adalah pilihan tepat. Fungsi itu bisa dibedakan. Artinya, kita bisa menemukan kemiringan kurva sigmoid pada dua titik yaitu fungsi monotonik tapi turunan fungsi tidak. Fungsi sigmoid logistik dapat menyebabkan jaringan saraf terjebak pada waktu pelatihan.Fungsi softmax adalah fungsi aktivasi logistik yang lebih umum yang digunakan untuk klasifikasi multiklass.

2. Tanh Activation function
	
	Tanh Activation function disebut juga sebagai hyperbolic tangent. Tanh juga seperti sigmoid logistik tapi lebih baik. Kisaran fungsi tanh adalah dari (-1 sampai 1). tanh juga sigmoidal (berbentuk s).

![Figure 1](/images/activation-function-concept-in-deep-learning/4.png)

	Keuntungannya adalah input negatif akan dipetakan sangat negatif dan input nol akan dipetakan mendekati nol pada grafik tanh. Fungsi ini bisa dibedakan. Fungsinya monoton sementara turunannya tidak. Fungsi tanh terutama digunakan klasifikasi antara dua kelas. Fungsi aktivasi sigmoid tanh dan logistic digunakan pada jaring umpan maju.


3. ReLU (Rectified Linear Unit) Activation Function
	
	ReLU adalah fungsi aktivasi yang paling banyak digunakan di dunia saat ini. Karena, ini digunakan di hampir semua jaringan saraf konvolusi atau pembelajaran yang dalam. 

![Figure 1](/images/activation-function-concept-in-deep-learning/5.png)

	Seperti yang dapat Anda lihat, ReLU setengah diperbaiki (dari bawah). Ini adalah f (s) adalah nol bila z kurang dari nol dan f (z) sama dengan z bila z di atas atau sama dengan nol. Rentang: [0 sampai tak terbatas) Fungsi dan turunannya keduanya bersifat monoton. Tapi masalahnya adalah semua nilai negatif menjadi nol segera yang menurunkan kemampuan model agar sesuai atau melatih dari data dengan benar. Itu berarti setiap masukan negatif yang diberikan pada fungsi aktivasi ReLU mengubah nilainya menjadi nol segera dalam grafik, yang pada gilirannya mempengaruhi grafik yang dihasilkan dengan tidak memetakan nilai negatif secara tepat..

4. Leaky ReLU
	Leaky ReLU adalah usaha untuk memecahkan masalah ReLU yang sekarat. Berikut gambar perbedaan ReLU dan Leaky ReLU :

![Figure 1](/images/activation-function-concept-in-deep-learning/6.png)
	
	Kebocoran membantu meningkatkan jangkauan fungsi ReLU. Biasanya, nilai a adalah 0,01 atau lebih. Bila tidak ada 0,01 maka disebut Randomized ReLU. Oleh karena itu rentang Leaky ReLU adalah (-infinity to infinity). Fungsi Leaky dan Randomized ReLU bersifat monoton. Selain itu, turunannya juga bersifat monoton.