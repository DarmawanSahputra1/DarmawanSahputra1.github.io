---
layout: posts
title: "Instalasi Ruby dan Jekyll"
date: 2025-02-20
---



# 📘 Instalasi Ruby dan Jekyll

Jekyll adalah salah satu generator situs statis yang sangat populer, dan Ruby adalah bahasa pemrograman yang digunakan oleh Jekyll. Berikut adalah panduan lengkap untuk menginstal Ruby dan Jekyll di sistem Anda.



## 🧑‍💻 Apa Itu Ruby?

**Ruby** adalah bahasa pemrograman dinamis dan berorientasi objek yang digunakan dalam banyak aplikasi, termasuk Jekyll. Ruby memungkinkan Jekyll untuk menjalankan berbagai perintah untuk membangun situs web statis dengan mudah.



## 🧑‍💻 Apa Itu Jekyll?

**Jekyll** adalah static site generator yang dibangun dengan Ruby. Jekyll memungkinkan Anda untuk membuat dan mengelola blog, portfolio, atau situs web sederhana tanpa memerlukan database. Anda cukup menulis konten dalam Markdown atau HTML, dan Jekyll akan menghasilkan situs web statis.



## 📋 Persyaratan Sistem

Sebelum memulai instalasi, pastikan komputer Anda memenuhi persyaratan berikut:

- Sistem Operasi: Linux, macOS, atau Windows
- Ruby: Versi terbaru (atau versi yang didukung oleh Jekyll)
- Bundler: Untuk mengelola dependensi Ruby



## 📦 Langkah 1: Instalasi Ruby

### 🖥️ Untuk macOS

1. **Menggunakan Homebrew (rekomendasi)**

   Jika Anda belum menginstal Homebrew, buka terminal dan jalankan perintah berikut untuk menginstalnya:

   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

   Kemudian, instal Ruby menggunakan Homebrew:

   ```bash
   brew install ruby
   ```

2. **Verifikasi Instalasi Ruby**

   Setelah instalasi selesai, pastikan Ruby telah terinstal dengan benar:

   ```bash
   ruby -v
   ```

   Anda harus melihat versi Ruby yang baru diinstal.

### 🖥️ Untuk Windows

1. **Unduh Ruby Installer**

   Kunjungi halaman [Ruby Installer](https://rubyinstaller.org/) dan unduh versi Ruby yang sesuai dengan sistem operasi Windows Anda.

2. **Instalasi Ruby**

   Jalankan installer dan pilih opsi untuk menambahkan Ruby ke PATH selama instalasi.

3. **Verifikasi Instalasi Ruby**

   Setelah instalasi selesai, buka Command Prompt atau PowerShell dan ketik:

   ```bash
   ruby -v
   ```

   Anda akan melihat versi Ruby yang baru diinstal.



## 📦 Langkah 2: Instalasi Jekyll

Setelah Ruby terinstal dengan benar, Anda dapat melanjutkan untuk menginstal Jekyll dan Bundler.

1. **Instalasi Jekyll dan Bundler**

   Di terminal atau command prompt, jalankan perintah berikut untuk menginstal Jekyll dan Bundler:

   ```bash
   gem install jekyll bundler
   ```

   Perintah ini akan menginstal Jekyll dan Bundler, yang digunakan untuk mengelola dependensi proyek Jekyll.

2. **Verifikasi Instalasi Jekyll**

   Setelah instalasi selesai, pastikan Jekyll telah terinstal dengan benar:

   ```bash
   jekyll -v
   ```

   Anda akan melihat versi Jekyll yang baru diinstal.



## 🏗️ Membuat Situs Jekyll Baru

Setelah Ruby dan Jekyll terinstal, Anda dapat membuat situs Jekyll baru.

1. **Buat Proyek Jekyll Baru**

   Di terminal atau command prompt, jalankan perintah berikut untuk membuat proyek Jekyll baru:

   ```bash
   jekyll new nama_proyek_anda
   ```

   Ini akan membuat folder proyek dengan struktur dasar situs Jekyll.

2. **Masuk ke Direktori Proyek**

   Arahkan ke folder proyek yang baru dibuat:

   ```bash
   cd nama_proyek_anda
   ```

3. **Menjalankan Server Lokal**

   Untuk melihat situs Anda secara lokal, jalankan perintah berikut:

   ```bash
   bundle exec jekyll serve
   ```

   Jekyll akan membangun situs dan menjalankan server lokal di alamat `http://localhost:4000`. Anda dapat membuka browser dan melihat situs baru Anda.



## 🚧 Troubleshooting

### 🛠️ Masalah Umum

- **Masalah Versi Ruby**: Jika Anda mengalami masalah dengan versi Ruby yang terlalu lama, pastikan Anda menggunakan versi yang didukung oleh Jekyll. Anda bisa mengatur versi Ruby menggunakan [rbenv](https://github.com/rbenv/rbenv) atau [RVM](https://rvm.io/).
  
- **Masalah Dependency**: Jika Anda mengalami masalah dengan dependensi, pastikan Anda menjalankan `bundle install` setelah membuat proyek baru untuk menginstal semua gem yang diperlukan.

- **Kesalahan Server**: Jika server lokal tidak berjalan, pastikan Anda menjalankan perintah `bundle exec jekyll serve` dari dalam direktori proyek Anda.



## ✅ Kesimpulan

- **Ruby** adalah bahasa pemrograman yang digunakan oleh Jekyll untuk membangun situs web statis.
- **Jekyll** memungkinkan pembuatan dan pengelolaan situs web statis dengan mudah, menggunakan template dan konten dalam format Markdown.
- Setelah mengikuti langkah-langkah instalasi, Anda dapat membuat dan menjalankan situs web Jekyll di komputer lokal Anda.


