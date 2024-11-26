---
layout: post
title: Mencoba membangun blog dengan Jekyll, Github Repo dan Visual Studio Code
date: 2024-11-24
categories: blogging
tags: [jekyll, blog]
description: 'ngeblog gratis dengan Github Page'
---

Membangun blog menggunakan Jekyll, GitHub Repo, dan Visual Studio Code adalah salah satu cara yang efisien dan modern untuk mengelola konten Anda. Jekyll adalah generator situs statis yang dirancang untuk GitHub Pages. Artikel ini akan memandu Anda langkah demi langkah untuk membangun blog Anda sendiri dengan menggunakan ketiga alat tersebut. 

## Mengapa Memilih Jekyll?

Jekyll adalah alat yang sangat populer di kalangan pengembang karena kemudahannya dalam membuat situs statis yang cepat dan aman. Tidak memerlukan basis data, sehingga lebih ringan dan mudah dikelola. Dengan Jekyll, Anda bisa fokus pada penulisan konten dalam format markdown dan membiarkan Jekyll mengurus sisanya. 

## Persiapan Lingkungan Pengembangan

Langkah pertama adalah menyiapkan lingkungan pengembangan. Pastikan Anda telah menginstal Git, Ruby, dan Jekyll di komputer Anda.

Berikut adalah langkah-langkah untuk menginstal Jekyll: 

### 1. Instal Ruby
Unduh dan instal Ruby dari [situs resmi Ruby](https://www.ruby-lang.org/en/). Pastikan untuk memilih versi yang sesuai dengan sistem operasi Anda. 
### 2. Instal Jekyll
Buka terminal atau command prompt dan jalankan perintah berikut untuk menginstal Jekyll dan bundler: 

`sh gem install jekyll bundler`

### 3. Membuat Proyek Jekyll Baru
Setelah Jekyll terinstal, buat proyek Jekyll baru dengan perintah berikut:

`jekyll new nama-blog-anda`

Perintah ini akan membuat folder baru dengan struktur proyek Jekyll dasar. Masuk ke folder proyek Anda:

`cd nama-blog-anda`

Untuk melihat blog Anda dalam mode pengembangan, jalankan perintah berikut:

`bundle exec jekyll serve`

Buka browser dan akses http://localhost:4000 untuk melihat blog Anda.

## Mengelola Kode dengan GitHub
Berikutnya, kita akan mengelola kode proyek kita menggunakan GitHub. Buat repositori baru di GitHub dan ikuti langkah-langkah berikut untuk menambahkan proyek Anda ke repositori:

### 1. Inisialisasi Git
Inisialisasi Git di folder proyek Anda dengan perintah:

`git init`

### 2. Tambahkan Remote Origin
Tambahkan URL repositori GitHub sebagai remote origin:

`git remote add origin https://github.com/username/nama-repo.git`

### 3. Commit dan Push
Commit dan push perubahan ke GitHub:

`git add .`
`git commit -m "Initial commit"`
`git push -u origin master`

## Mengedit Kode dengan Visual Studio Code
Visual Studio Code adalah editor kode yang sangat populer dan kaya fitur. Anda bisa menggunakannya untuk mengedit dan mengelola proyek Jekyll Anda. Berikut adalah beberapa langkah dasar untuk menggunakan Visual Studio Code dengan proyek Jekyll Anda:

1. Buka Proyek: Buka Visual Studio Code dan buka folder proyek Jekyll Anda.
2. Instal Ekstensi: Instal ekstensi yang membantu dalam pengembangan Jekyll, seperti "Jekyll Syntax Support" dan "Markdown All in One".
3. Edit Konten: Mulai mengedit file markdown di folder `_posts` untuk menambahkan artikel baru atau mengedit yang sudah ada. Setiap perubahan yang Anda buat dapat langsung dilihat dengan menjalankan `bundle exec jekyll serve` dan membuka `http://localhost:4000` di browser.

Menerapkan ke GitHub Pages
Setelah Anda puas dengan blog Anda, saatnya untuk menerapkannya ke GitHub Pages agar bisa diakses oleh publik. Berikut langkah-langkahnya:

1. Aktifkan GitHub Pages: Masuk ke pengaturan repositori GitHub Anda, gulir ke bawah ke bagian GitHub Pages, dan pilih sumber dari cabang master atau main.
2. Deploy: GitHub akan secara otomatis membangun dan menerapkan situs Jekyll Anda. Anda dapat mengakses blog Anda di https://username.github.io/nama-repo.

## Kesimpulan
Membangun blog dengan Jekyll, GitHub Repo, dan Visual Studio Code adalah proses yang menyenangkan dan memberi Anda kontrol penuh atas konten dan desain blog Anda. Dengan mengikuti langkah-langkah ini, Anda dapat membuat blog yang cepat, aman, dan mudah dikelola. Selamat mencoba!

Apakah Anda pernah mencoba menggunakan Jekyll untuk membangun blog? Bagikan pengalaman Anda di kolom komentar!

Semoga artikel ini membantu Anda dalam memulai perjalanan membangun blog dengan Jekyll, GitHub Repo, dan Visual Studio Code. Jika ada pertanyaan atau permintaan lebih lanjut, jangan ragu untuk menghubungi saya! 😊