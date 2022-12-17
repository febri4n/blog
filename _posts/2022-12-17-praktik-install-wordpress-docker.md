---
layout: single
title:  "Praktik: Install WordPress MariaDB di Docker dengan Spesifikasi Terbatas."
date: 2022-12-17 00:00:00 +0700
permalink: /:title
description: "Praktik: Install WordPress di Docker dengan Spesifikasi Terbatas."
excerpt: "Menjelaskan Bagaimana Cara Install WordPress MariaDB di Docker dengan Spesifikasi Terbatas."
header:
    overlay_color: "#333"
#  image: /assets/images/tutorial-install-nodejs.png
#  caption: "Tutorial Install Node.js di Linux Ubuntu"
# toc: true
# toc_label: "Daftar Isi"
# toc_icon: "cog"
# toc_sticky: true
categories: 
    - praktik
tags : 
    - docker
    - linux
    - wordpress
    - mariadb
classes: wide
---
Untuk membuat container WordPress dan menghubungkannya ke database MariaDB dengan spesifikasi terbatas, Anda dapat mengikuti langkah-langkah berikut:

1. Instal Docker pada sistem Anda.

2. Jalankan perintah berikut untuk membuat container MariaDB dengan sumber daya terbatas:
```bash
docker run --name mariadb -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=wordpress -e MYSQL_USER=wordpress -e MYSQL_PASSWORD=password -p 3306:3306 --memory="256m" --memory-swap="512m" --cpu-shares=512 --cpus=1 -d mariadb:latest
```
Ini akan membuat container MariaDB dengan nama `mariadb`, kata sandi root `password`, dan database bernama `wordpress` dengan pengguna bernama `wordpress` dan kata sandi `password`. Ini juga akan membatasi container hingga 256 MB RAM dan 1 CPU core.

3. Jalankan perintah berikut untuk membuat container WordPress dan menghubungkannya ke container MariaDB:
```bash
docker run --name wordpress --link mariadb:mysql -p 80:80 -e WORDPRESS_DB_HOST=mysql:3306 -e WORDPRESS_DB_USER=wordpress -e WORDPRESS_DB_PASSWORD=password -e WORDPRESS_DB_NAME=wordpress --memory="256m" --memory-swap="512m" --cpu-shares=512 --cpus=1 -d wordpress:latest
```
Ini akan membuat container WordPress dengan nama `wordpress` dan menghubungkannya ke container MariaDB menggunakan flag tautan. Ini juga akan mengatur host database, pengguna, kata sandi, dan nama dalam variabel lingkungan WordPress dan membatasi kontainer hingga 256 MB RAM dan 1 CPU core.

4. Akses situs web WordPress dengan mengunjungi http://localhost di browser web Anda untuk menyelesaikan proses instalasi WordPress.