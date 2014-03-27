---
layout: post
title: "TechTalk: Membuat Mini Heroku di Digital Ocean"
description: "Membuat Heroku mini di vps kita sendiri di Digital
Ocean."
tags: [server, techtalk]
image:
  feature: abstract-6.jpg
  credit: dargadgetz
  creditlink: 
comments: true
share: true
---

Anda tahu Heroku? Platform as a Service (PaaS)
yang terkenal dengan “autodeploy” yang memudahkan dan
mempercepat developer dalam mendeploy aplikasi. Apalagi dengan fitur
gratis sampai limit tertentu.

Jika kita mendeploy aplikasi kita di heroku, mungkin akan terasa murah saat menggunakan versi gratis, namun saat sudah melampaui limit, maka biaya yang harus kita bayarkan akan mahal, mulai dari `USD 9` ke atas. Solusinya kita bisa membeli vps dengan harga yang relative murah di [Digital Ocean](http://bit.ly/toOcean).

Selain Heroku, setahun belakangan ini dunia server dan cloud computing
diramaikan oleh kemunculan [Digital Ocean](http://bit.ly/toOcean). Startup dari New York yang
menawarkan 20GB SSD/ 1TB Bandwidth server seharga $5 . [Digital Ocean](http://bit.ly/toOcean)
juga menjadi rujukan oleh para developer dan para pemula di bidang
server karena dokumentasinya yang lengkap dan banyak tutorial yang
diberikan.

Nah, TechTalk kali ini akan membahas bagaimana membuat
autodeploy seperti Heroku, namun di server yang kita miliki di Digital
Ocean. Daripada harus mengupgrade paket Heroku yang lumayan mahal,
mending kita bikin VPS Digital Ocean seharga $5/Bulan menjadi layaknya
Heroku.

### Dokku
> [Dokku](https://github.com/progrium/dokku) adalah solusi Platform as a Service yang memungkinkan kita untuk mendeploy aplikasi yang kita miliki dengan cepat di server kita sendiri.

Berikut langkah - langkah membuat heroku-mini versi digital ocean:

### Langkah #1:  Membuat Droplet
Yang pertama kita buat adalah droplet yang ada instalasi dokku didalamnya.

Klik tombol hijau `Create` di kiri atau tombol biru `Create Droplet` di kanan atas untuk membuat droplet baru:
<figure>
  <img src="/images/techtalk-do-heroku/create_droplet.png" />
</figure>

**Droplet Hostname :** Beri nama droplet sesuai keinginan kita, yang jelas dalam satu kata, contoh dibawah ini dengan `trydokku`

<figure>
	<img src="/images/techtalk-do-heroku/config_1.png" />
</figure>

**Select Size :** Pilih paket yang ingin kita beli. Ini tergantung kebutuhan aplikasi yang akan kita jalankan nanti. Semakin besar komputasi dan resource yang akan kita gunakan berarti kita membutuhkan kapasitas server yang semakin besar.

<figure>
	<img src="/images/techtalk-do-heroku/config_2.png" />
</figure>

**Select Region :** Memilih posisi datacenter. Pilih posisi datacenter yang terdekat dari negara kita karena kemungkinan besar akan berpengaruh pada kecepatan akses kita terhadap server yang kita miliki. Karena posisi saya di Indonesia, jadi saya memilih `Singapore`. Kalau bertanya kenapa lebih cepat, karena `route` yang kita ambil lebih dekat daripada jika kita mengambil datacenter yang ada di US misalnya. Dan karena rutenya lebih dekat, `latency`-nya lebih kecil.
 
<figure>
	<img src="/images/techtalk-do-heroku/config_3.png" />
</figure>

**Select Image:** Setelah itu scroll ke bawah kita akan diberi pilihan OS maupun aplikasi yang bisa kita pilih dan akan diinstallkan langsung oleh Digital Ocean. Pilih tab `Applications` dan pilih tombol `Dokku on Ubuntu 13.04` untuk memilih OS yang sudah terinstall dokku.

<figure>
	<img src="/images/techtalk-do-heroku/config_4.png" />
</figure>



