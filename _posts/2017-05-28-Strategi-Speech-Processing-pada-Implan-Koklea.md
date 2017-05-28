---
layout: post
title: "Strategi Speech Processing pada Implan Koklea"
date: 2017-05-28
excerpt: "Implan Koklea (Cochlear Implant) adalah alat yang menyediakan pendengaran parsial untuk orang-orang tunarungu yang tidak dapat menggunakan alat bantu dengar konvensional. Hal tersebut disebabkan oleh hilangnya sel rambut di telinga bagian dalam. Dalam kejadian seperti itu, stimulasi langsung serabut saraf memberikan sarana untuk mengembalikan pendengaran pasien."
tags: [implan, koklea, speech processing]
comments: true
---

Implan Koklea (Cochlear Implant) adalah alat yang menyediakan pendengaran parsial untuk orang-orang tunarungu yang tidak dapat menggunakan alat bantu dengar konvensional. Hal tersebut disebabkan oleh hilangnya sel rambut di telinga bagian dalam. Dalam kejadian seperti itu, stimulasi langsung serabut saraf memberikan sarana untuk mengembalikan pendengaran pasien. Implan koklea  beroperasi dengan menstimulasi secara elektrik saraf pendengaran secara langsung sehingga melewati mekanisme pendengaran normal.

<figure>
	<a href="assets/img/fig0.png"><img src="assets/img/fig0.png"></a>
</figure>

Berbagai perangkat implan koklea telah dikembangkan selama ini. Semua perangkat implan memiliki fitur dasar yang sama: mikrofon yang mengambil suara, prosesor sinyal yang mengubah suara menjadi sinyal listrik, sistem transmisi yang mentransmisikan sinyal listrik ke elektroda implan dan elektroda atau rangkaian elektroda (terdiri dari beberapa elektroda) yang dimasukkan ke dalam koklea oleh ahli bedah.

<figure>
	<a href="assets/img/fig1.png"><img src="assets/img/fig1.png"></a>
</figure>

Dalam implan saluran tunggal hanya satu elektroda yang digunakan. Pada implan koklea multichannel, susunan elektroda dimasukkan ke dalam koklea sehingga serabut saraf pendengaran yang berbeda dapat distimulasi di tempat yang berbeda dalam koklea, sehingga memanfaatkan mekanisme tempat untuk frekuensi pengkodean. Elektroda yang berbeda distimulasi tergantung pada frekuensi sinyal. Elektroda di dekat dasar koklea distimulasi dengan sinyal frekuensi tinggi, sedangkan elektroda dekat apeks dirangsang dengan sinyal frekuensi rendah. Prosesor sinyal bertanggung jawab untuk memecah sinyal input menjadi pita frekuensi atau saluran yang berbeda dan mengirimkan sinyal yang disaring ke elektroda yang sesuai.

## Strategi bentuk gelombang

### Pendekatan Compressed-Analog (CA)

Pendekatan kompresi-analog (CA) pada awalnya digunakan pada perangkat Ineraid yang diproduksi oleh Symbion, Inc., Utah. Sinyal dikompres dengan menggunakan control gain otomatis dan kemudian disaring menjadi empat pita frekuensi bersebelahan, dengan frekuensi tengah pada 0,5, 1, 2 dan 3,4 kHz. Bentuk gelombang yang disaring melalui kontrol gain yang dapat disesuaikan dan kemudian dikirim secara langsung melalui koneksi perkutan ke empat elektroda intracochlear. Bentuk gelombang yang disaring dikirim bersamaan ke empat elektroda dalam bentuk analog. Pendekatan CA, yang digunakan pada perangkat Ineraid, sangat berhasil karena memungkinkan banyak pasien untuk mendapatkan pemahaman berbagai suara. 

### Continuous Interleaved Sampling (CIS)

Pendekatan CA menggunakan stimulasi analog yang menghasilkan empat bentuk gelombang analog kontinu hingga empat elektroda secara bersamaan. Perhatian utama yang terkait dengan stimulasi simultan adalah interaksi antara saluran yang disebabkan oleh penjumlahan medan listrik dari elektroda individu. Interaksi ini dapat mendistorsi informasi spektrum bicara dan karena itu menurunkan pemahaman wicara. Peneliti di Research Triangle Institute (RTI) mengembangkan pendekatan Continuous Interleaved Sampling (CIS) [4] yang membahas masalah interaksi saluran dengan menggunakan sinyal non simultan. Kumpulan dari biphasic pulses dikirim ke elektroda dengan cara yang tidak saling tumpang tindih (non-simultan), yaitu dengan cara sedemikian rupa sehingga hanya satu elektroda yang dirangsang pada satu waktu. Amplitudo pulsa diperoleh dengan mengekstraksi amplop bentuk gelombang yang dilambangkan. Sinyal pertama kali ditekankan terlebih dahulu dan melewati bank bandpass filter.

<figure>
	<a href="assets/img/fig2.png"><img src="assets/img/fig2.png"></a>
</figure>

Amplop dari bentuk gelombang yang disaring kemudian diekstraksi dengan rektifikasi gelombang penuh dan penyaringan low-pass (biasanya dengan frekuensi cutoff 200 atau 400 Hz). Keluaran amplop akhirnya dikompres dan kemudian digunakan untuk memodulasi biphasic pulses. Fungsi kompresi non linier (misalnya logaritmik) digunakan untuk memastikan bahwa keluaran amplop sesuai dengan rentang dinamis pasien yang didengar secara elektrik. Deretan biphasic pulses seimbang, dengan amplitudo sebanding dengan amplop, dikirim ke enam elektroda dengan kecepatan konstan dalam mode nonoverlapping. Tingkat di mana pulsa dikirim ke elektroda telah ditemukan memiliki dampak besar pada pengenalan suara. Rangsangan denyut nadi yang tinggi biasanya menghasilkan kinerja yang lebih baik daripada stimulasi denyut nadi rendah. Perbandingan antara pendekatan CA dan CIS menunjukkan tingkat pengenalan ucapan yang lebih tinggi dengan pendekatan CIS.

### Teknik ekstraksi fitur

Teknik ini didasarkan pada penggalian informasi spektral dari sinyal masukan dan menggunakan informasi ini untuk menghasilkan rangsangan pada elektroda. Untuk persepsi ujaran yang tepat, penting untuk menyajikan frekuensi pemancar (F1-F3). Frekuensi gelombang periodik ini disebut frekuensi dasar (F0). Tiga puncak berikut frekuensi disebut F1, F2 dan F3 dan dikenal sebagai pembentuk. Implan nukleus yang diproduksi oleh Cochlear Corporation dan dikembangkan di University of Melbourne menggunakan teknik ini. Beberapa teknik yang digunakan pada perangkat ini dibahas pada bagian berikut. Alat implan koklea nukleus terdiri dari 22 elektroda.

### F0 / F2

Dalam skema ini F0 diperkirakan menggunakan detektor zero-crossing pada keluaran filter lowpass 270Hz. F2 diperkirakan menggunakan detektor zero-crossing pada keluaran filter bandpass 1000-4000 Hz. Amplitudo formant F2 diperoleh setelah rektifikasi dan lowpass penyaringan dari keluaran filter bandpass. Elektroda yang tepat (di antara 22 elektroda) dirangsang pada laju pulsa F0. Untuk suara yang tak terdengar, elektroda dirangsang pada tingkat rata-rata 100 pulsa.

### F0 / F1 / F2

Strategi ini merupakan perbaikan teknik F0 / F2 sebelumnya karena ia juga termasuk F1 formant pertama. Detektor zero-crossing digunakan pada output filter bandpass 280-1000 Hz. Dua set elektroda sekarang distimulasi, satu dengan informasi formant F1 dan yang lainnya dengan informasi formant F2. Informasi F1 digunakan untuk merangsang elektroda apikal dan informasi F2 untuk elektroda basal. 200 μ detik pulsa digunakan dengan pemisahan 800 μ detik untuk menghindari interaksi saluran. Amplitudo pulsa sebanding dengan amplitudo pembentuk F1 dan F2 dan laju stimulasi masih pulsa F0 detik-1. Karena informasi tambahan pada perangkat F0 / F1 / F2, kinerjanya meningkat dibandingkan dengan perangkat F0 / F2 sebelumnya. Konsep penggunaan informasi forma bekerja dengan baik untuk sinyal frekuensi rendah, namun dengan frekuensi yang lebih tinggi seperti konsonan, strategi yang berbeda harus digunakan.

### MPEAK

Perbaikan lebih lanjut atas skema F0 / F1 / F2 adalah MPEAK (atau MULTIPEAK) yang mengekstrak dan menggunakan informasi frekuensi tinggi dari sinyal input untuk merangsang elektroda. Filter bandpass 800-4000 Hz digunakan untuk menentukan F2. Selanjutnya tiga filter bandpass tambahan (2000-2800 Hz, 2800-4000 Hz, 4000-6000 Hz) digunakan untuk mengekstrak informasi frekuensi tinggi. Jadi, empat elektroda dirangsang pada pulsa F0 untuk pidato bersuara dan rata-rata 250 pulsa untuk pidato tak bersuara. Karena tersedianya informasi frekuensi tinggi kinerja pasien membaik dengan skema ini terutama untuk konsonan. Kerugian utama dari skema ekstraksi fitur adalah bahwa mereka mengenalkan kesalahan dalam penentuan frekuensi forman. Dengan demikian penelitian lebih lanjut berusaha melihat teknik lain untuk mewakili ucapan dalam implan koklea.

### Spectral maxima sound processor (SMSP)

Alih-alih melakukan ekstraksi fitur, SMSP menganalisis pidato oleh bank dengan 16 filter bandpass mulai dari 250-5400 Hz. Keluaran dari filter bandpass diperbaiki dan lowpass disaring (200 Hz) dan enam keluaran terbesar dipilih dari antara 16. Hanya enam elektroda yang sesuai dengan amplitudo maksimum yang dirangsang pada setiap siklus pada tingkat 250 pps.


<iframe width="560" height="315" src="https://www.youtube.com/watch?v=zeg4qTnYOpw" frameborder="0"> </iframe>


#### Referensi:

https://en.wikipedia.org/wiki/Speech_processing

Kouachi Rouiha, Djedou Bachir, Bouchaala Ali. 2008. Analysis of Speech Processing Strategies in Cochlear Implants. Algeria: Science Publications.

