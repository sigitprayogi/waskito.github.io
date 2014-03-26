---
layout: post
title: "TechTalk: Membuat Server Digital Ocean Jadi Seperti Heroku"
description: "Membuat Heroku mini di vps kita sendiri di Digital
Ocean."
tags: [server, techtalk]
comments: true
share: true
---

Anda tahu Heroku? Bagi para developer (terutama developer Ruby,
Node.js, Python) tentu mengenal heroku. Platform as a Service (PaaS)
yang terkenal dengan “autodeploy” yang memudahkan dan
mempercepat developer dalam mendeploy aplikasi. Apalagi dengan fitur
gratis sampai skala tertentu, namun tentu ada limit dan performa
yang terbatas.

Selain Heroku, setahun belakangan ini dunia server dan cloud computing
diramaikan oleh kemunculan Digital Ocean. Startup dari New York yang
menawarkan 20GB SSD/ 1TB Bandwidth server seharga $5 . Digital Ocean
juga menjadi rujukan oleh para developer dan para pemula di bidang
server karena dokumentasinya yang lengkap dan banyak tutorial yang
diberikan.

Nah, TechTalk kali ini akan membahas bagaimana membuat
autodeploy seperti Heroku, namun di server yang kita miliki di Digital
Ocean. Daripada harus mengupgrade paket Heroku yang lumayan mahal,
mending kita bikin VPS Digital Ocean seharga $5/Bulan menjadi layaknya
Heroku.
