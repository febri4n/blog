---
layout: single
title: "Berkenalan dengan Gitlab"
date: 2023-08-26 06:00:00 +0700
permalink: /:title
description: "Menjelaskan beberapa hal terkait dengan Gitlah dan hubungannya dengan DevOps."
excerpt: "Menjelaskan beberapa hal terkait dengan Gitlah dan hubungannya dengan DevOps."
header:
  overlay_color: "#333"
#  image: /assets/images/tutorial-install-nodejs.png
#  caption: "Tutorial Install Node.js di Linux Ubuntu"
toc: true
toc_label: "Daftar Isi"
toc_icon: "cog"
toc_sticky: true
categories:
  - info
tags:
  - linux
  - git
  - git-scm
  - github
  - version control
---

### Apa itu Gitlab ?

GitLab adalah pengelola repositori Git berbasis web yang menyediakan repositori gratis terbuka dan pribadi, wiki, pelacakan isu, dan fitur pipa CI/CD, menggunakan lisensi sumber terbuka (lisensi MIT), yang dikembangkan oleh GitLab Inc. Perangkat lunak ini diciptakan oleh Dmitriy Zaporozhets dan Valery Sizov.

GitLab mirip dengan Github. Anda dapat mengakses GitLab di mana saja dan kapan saja secara gratis. Di GitLab, Anda dapat menyimpan kode, berkolaborasi dalam kode dengan tim Anda, melakukan pekerjaan devops, dan lainnya.

### Kenapa Gitlab ?

Ada beberapa alasan mengapa kita menggunakan GitLab:

1. GitLab adalah Platform DevOps Lengkap Di GitLab, Anda dapat melakukan pekerjaan DevOps mulai dari perencanaan hingga pemantauan dan keamanan. Di GitLab, kita dapat bekerja sama dengan lebih baik.

2. GitLab adalah Sumber Terbuka GitLab adalah platform pengembangan perangkat lunak ujung-ke-ujung sumber terbuka dengan kontrol versi bawaan, pelacakan isu, tinjauan kode, CI/CD, dan banyak lagi.

3. Mudah untuk Melaksanakan CI/CD Di GitLab, Anda dapat melaksanakan CI/CD untuk pengembangan perangkat lunak seperti membangun, menguji, mendeploy, dan memantau aplikasi. Anda dapat menggunakan alat ini secara gratis.

#### Perbedaan Gitlab CE & Gitlab EE

Perbedaan antara GitLab Community Edition (CE) dan GitLab Enterprise Edition (EE) terutama berkaitan dengan fitur dan dukungan yang disediakan oleh masing-masing versi. Berikut adalah beberapa perbedaan utama antara keduanya:

1. **Fitur Tambahan**:

   - GitLab CE: Versi CE menyediakan sejumlah fitur inti GitLab seperti kontrol versi, pelacakan masalah, kolaborasi, CI/CD dasar, dll. Namun, beberapa fitur canggih mungkin tidak tersedia di versi ini.
   - GitLab EE: Versi EE memiliki semua fitur yang ada di CE dan juga menyertakan sejumlah fitur lanjutan seperti analisis siklus hidup aplikasi, keamanan yang ditingkatkan, manajemen portofolio, alat pengawasan lebih canggih, dan lainnya.

2. **Keamanan dan Kepatuhan**:

   - GitLab CE: Fitur keamanan dan kepatuhan mungkin lebih terbatas atau tidak ada dalam versi CE.
   - GitLab EE: Versi EE sering kali memiliki fitur keamanan dan kepatuhan yang lebih lengkap dan ditingkatkan untuk memenuhi kebutuhan perusahaan dan organisasi besar.

3. **Dukungan Prioritas**:

   - GitLab CE: Tidak ada dukungan resmi yang disediakan untuk versi CE. Dukungan datang melalui komunitas GitLab.
   - GitLab EE: Versi EE umumnya menyertakan dukungan resmi dari tim GitLab. Ini berarti pelanggan EE mendapatkan dukungan prioritas dan akses ke sumber daya bantuan.

4. **Lisensi dan Biaya**:

   - GitLab CE: Versi CE adalah perangkat lunak sumber terbuka dan dapat digunakan secara gratis.
   - GitLab EE: Versi EE adalah produk berlisensi yang memerlukan pembayaran berlangganan. Biaya berlangganan bisa bervariasi berdasarkan jumlah pengguna dan fitur yang diinginkan.

5. **Skalabilitas dan Integrasi**:
   - GitLab EE: Kadang-kadang versi EE memiliki fitur yang mendukung skalabilitas dan integrasi lebih baik untuk memenuhi kebutuhan perusahaan besar atau proyek yang kompleks.

Pilihan antara GitLab CE dan GitLab EE tergantung pada kebutuhan dan anggaran perusahaan atau proyek Anda. Jika Anda hanya membutuhkan fitur dasar kontrol versi dan kolaborasi, GitLab CE mungkin sudah memadai. Namun, jika Anda memerlukan fitur-fitur lanjutan, dukungan resmi, keamanan yang ditingkatkan, dan skala yang lebih besar, GitLab EE mungkin menjadi pilihan yang lebih baik.

### Gitlab Runner, apakah itu ?

GitLab Runner adalah aplikasi yang bekerja dengan GitLab CI/CD untuk menjalankan pekerjaan dalam sebuah pipeline. Ketika kita memiliki pekerjaan CI/CD, kita dapat menggunakan GitLab Runner ini untuk menjalankan pekerjaan kita. Jadi nantinya, GitLab Runner akan menjalankan perintah untuk menjalankan pekerjaan CI/CD tersebut.

GitLab Runner bersifat sumber terbuka dan ditulis dalam bahasa Go. Ia dapat dijalankan sebagai satu berkas biner tunggal, tanpa memerlukan persyaratan tertentu terhadap bahasa pemrograman.

Anda dapat menginstal GitLab Runner pada beberapa sistem operasi yang didukung. Sistem operasi lain mungkin juga dapat digunakan, selama Anda dapat mengkompilasi berkas biner Go di dalamnya.

GitLab Runner juga dapat berjalan di dalam wadah Docker atau dideploy dalam sebuah kluster Kubernetes.

Untuk menggunakan GitLab Runner, ada beberapa hal yang perlu kita siapkan.

Buat dan tambahkan berkas .gitlab-ci.yml ke direktori utama repositori Anda.
Konfigurasikan Runner.

### Gitlab CI/CD

GitLab CI/CD adalah layanan di GitLab yang digunakan untuk menerapkan praktik CI/CD. Jadi, semua yang Anda pelajari pada modul sebelumnya seperti GitLab Runner dan GitLab Executor merupakan bagian dari layanan GitLab CI/CD.

Apa manfaatnya ketika kita menggunakan GitLab CI/CD untuk menerapkan CI/CD?

1. Mudah dipelajari, digunakan, dan dapat diskalakan.
2. Ini adalah sistem yang lebih cepat yang dapat digunakan untuk penyebaran dan pengembangan kode.
3. Anda dapat menjalankan pekerjaan lebih cepat dengan mengatur runner Anda sendiri (ini adalah aplikasi yang memproses pembangunan) dengan semua dependensi telah terpasang sebelumnya.
4. Ini memungkinkan anggota tim proyek untuk mengintegrasikan pekerjaan mereka secara harian, sehingga kesalahan integrasi dapat diidentifikasi dengan mudah melalui pembangunan otomatis.
