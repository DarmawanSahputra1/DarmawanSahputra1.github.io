---
layout: post
title: "Mengenal dan Mengatur _config.yml pada Jekyll"
date: 2025-04-24
---

# ⚙️ Mengenal dan Mengatur `_config.yml` pada Jekyll

File `_config.yml` adalah file konfigurasi utama dalam proyek Jekyll. File ini digunakan untuk menyimpan pengaturan global yang akan digunakan di seluruh situs Anda, seperti nama situs, URL, layout default, plugin, dan sebagainya.

Dengan memahami cara kerja dan struktur file ini, Anda bisa mengatur perilaku situs Jekyll Anda dengan lebih mudah dan konsisten.


## 📁 Apa Itu `_config.yml`?

`_config.yml` adalah file dalam format YAML (YAML Ain’t Markup Language) yang digunakan Jekyll untuk:

* Mengatur metadata situs seperti judul, deskripsi, dan URL.
* Mengonfigurasi permalink, koleksi, pagination, dan lain-lain.
* Mengaktifkan plugin atau fitur tambahan.
* Menentukan pengaturan build dan deployment.

Jekyll secara otomatis membaca file ini saat membangun situs Anda.



## 📝 Contoh Struktur Dasar `_config.yml`

```yml
title: "Blog Saya"
description: "Kumpulan tulisan tentang teknologi dan pemrograman"
baseurl: "" # jika situs berada di subfolder, contoh "/blog"
url: "https://namadomain.com" # ganti dengan URL situs Anda

author:
  name: "Nama Anda"
  email: "nama@contoh.com"

theme: minima

permalink: /:categories/:title/

plugins:
  - jekyll-feed
  - jekyll-seo-tag
```


## 🔍 Penjelasan Elemen Konfigurasi

| Kunci         | Fungsi                                                        |
| ------------- | ------------------------------------------------------------- |
| `title`       | Judul situs. Muncul di tag `<title>` dan halaman depan.       |
| `description` | Deskripsi singkat situs Anda. Digunakan oleh plugin SEO.      |
| `baseurl`     | URL basis jika situs Anda berada di subdirektori.             |
| `url`         | URL utama situs Anda.                                         |
| `author`      | Informasi tentang penulis situs.                              |
| `theme`       | Tema Jekyll yang digunakan.                                   |
| `permalink`   | Menentukan format URL untuk halaman/postingan.                |
| `plugins`     | Plugin tambahan yang digunakan untuk memperluas fungsi situs. |



## 🧪 Contoh Lain Konfigurasi Lanjutan

```yml
markdown: kramdown
highlighter: rouge
paginate: 5
paginate_path: "/page:num/"

collections:
  tutorials:
    output: true
    permalink: /tutorials/:path/
```

### Penjelasan Tambahan:

* `markdown`: Menentukan engine Markdown yang digunakan (`kramdown` adalah default).
* `paginate`: Mengaktifkan pagination untuk posting blog.
* `collections`: Menambah koleksi khusus seperti `tutorials`.



## 💡 Tips Penting

* YAML sangat peka terhadap indentasi. Gunakan spasi, **bukan tab**.
* Anda bisa memiliki lebih dari satu file konfigurasi dan menggabungkannya saat build:

```bash
jekyll serve --config _config.yml,_config_dev.yml
```



## ✅ Kesimpulan

* `_config.yml` adalah jantung dari konfigurasi situs Jekyll.
* Anda dapat menyesuaikan banyak aspek situs melalui file ini: dari nama situs hingga perilaku URL.
* Memahami struktur dan cara kerja YAML sangat membantu dalam menghindari kesalahan saat build.


