---
layout: post
title: "Responsive Web Desain"
date: 2025-05-18
---

# Materi Lengkap Responsive Web Design

## 1. Pengertian

Responsive Web Design (RWD) adalah pendekatan desain web agar tampilan dan layout website menyesuaikan ukuran layar pengguna, seperti desktop, tablet, dan smartphone.


## 2. Tujuan Responsive Design

* Memberikan pengalaman pengguna (UX) yang konsisten di semua perangkat
* Mengurangi kebutuhan membuat versi terpisah untuk mobile
* Meningkatkan SEO karena Google mengutamakan situs yang mobile-friendly


## 3. Teknik Utama

### a. Viewport Meta Tag

Menentukan bagaimana halaman ditampilkan di perangkat mobile.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### b. Media Queries

Menentukan aturan CSS berdasarkan lebar layar.

```css
@media (max-width: 768px) {
  body {
    background-color: lightgray;
  }
}
```

### c. Layout Fleksibel

Gunakan `width` dalam persentase daripada satuan tetap (px).

```css
.container {
  width: 100%;
  padding: 5%;
}
```

### d. Gambar Responsif

```css
img {
  max-width: 100%;
  height: auto;
}
```

### e. Framework CSS (Contoh: Bootstrap)

Menggunakan grid system dan utility classes seperti `col-md-6`, `d-none`, `d-lg-block`.


## 4. Tools untuk Testing Responsif

* Chrome DevTools (toggle device toolbar)
* Responsively App
* BrowserStack / LambdaTest


## 5. Contoh Layout Responsive Sederhana

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: flex;
      flex-wrap: wrap;
    }
    .box {
      flex: 1 1 300px;
      padding: 20px;
      background: lightblue;
      margin: 10px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">Konten 1</div>
    <div class="box">Konten 2</div>
    <div class="box">Konten 3</div>
  </div>
</body>
</html>
```


## 6. Tips Tambahan

* Rancang dari mobile ke desktop (mobile-first design)
* Hindari ukuran tetap (fixed width)
* Gunakan rem/em untuk ukuran font


## 7. Referensi

* [MDN Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)
* [W3Schools Responsive Web](https://www.w3schools.com/html/html_responsive.asp)
