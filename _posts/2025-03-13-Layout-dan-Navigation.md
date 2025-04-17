---
layout: post
title: "HTML: Layout dan Navigation"
date: 2025-03-13
---

# 📘 HTML: Layout dan Navigasi

Pelajari cara menyusun tata letak halaman web (layout) dan membuat sistem navigasi menggunakan elemen-elemen dasar HTML.



## 🧱 Apa Itu Layout dalam HTML?

**Layout** adalah struktur atau kerangka utama dari sebuah halaman web. Layout menentukan bagaimana elemen-elemen seperti header, konten, sidebar, dan footer ditampilkan dan diatur di dalam halaman.

### 📌 Elemen-Elemen Layout Umum

| Elemen | Fungsi |
|--------|--------|
| `<header>` | Bagian atas halaman (judul, logo, dll.) |
| `<nav>` | Menu navigasi |
| `<main>` | Konten utama halaman |
| `<section>` | Seksi konten (bab/subbab) |
| `<article>` | Konten independen seperti post atau berita |
| `<aside>` | Konten tambahan (sidebar, iklan) |
| `<footer>` | Bagian bawah halaman (hak cipta, kontak) |
| `<div>` | Pembungkus (container) umum |



### ✅ Contoh Layout Sederhana

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Contoh Layout</title>
</head>
<body>
  <header>
    <h1>Website Saya</h1>
  </header>

  <nav>
    <ul>
      <li><a href="index.html">Beranda</a></li>
      <li><a href="about.html">Tentang saya</a></li>
      <li><a href="kontak.html">Kontak</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <h2>Selamat Datang</h2>
      <p>Ini adalah halaman utama.</p>
    </section>
  </main>

  <aside>
    <h3>Berita Terkini</h3>
    <p>Informasi tambahan atau iklan di sini.</p>
  </aside>

  <footer>
    <p>&copy; 2025 Website Saya</p>
  </footer>
</body>
</html>
```



## 🧭 Apa Itu Navigasi dalam HTML?

**Navigasi (navigation)** adalah bagian dari halaman web yang memungkinkan pengguna berpindah antarhalaman atau antarbagian dalam halaman.

### 🏷️ Elemen untuk Navigasi

- `<nav>` digunakan untuk membungkus menu navigasi utama.
- `<a>` digunakan untuk membuat link ke halaman atau bagian tertentu.



### ✅ Contoh Menu Navigasi

```html
<nav>
  <ul>
    <li><a href="index.html">Beranda</a></li>
    <li><a href="layanan.html">Layanan</a></li>
    <li><a href="kontak.html">Kontak</a></li>
  </ul>
</nav>
```



### ✅ Navigasi ke Bagian Halaman (Scroll Internal)

```html
<ul>
  <li><a href="#profil">Profil</a></li>
  <li><a href="#layanan">Layanan</a></li>
  <li><a href="#kontak">Kontak</a></li>
</ul>

<section id="profil">
  <h2>Profil</h2>
  <p>Deskripsi tentang kami...</p>
</section>

<section id="layanan">
  <h2>Layanan</h2>
  <p>Layanan kami meliputi...</p>
</section>

<section id="kontak">
  <h2>Kontak</h2>
  <p>Hubungi kami di...</p>
</section>
```


## 🎯 Tips Praktis

- Gunakan **elemen semantik** seperti `<header>`, `<nav>`, `<main>` untuk membantu struktur dan SEO.
- Gunakan CSS (di luar HTML) untuk mengatur **layout grid/flexbox** dan membuat tampilan responsive.
- Pastikan setiap navigasi menggunakan teks yang jelas dan mudah dimengerti.
- Gunakan `aria-label` pada elemen navigasi jika perlu untuk aksesibilitas.


## ✅ Kesimpulan

- **Layout HTML** membantu menyusun kerangka halaman agar rapi dan konsisten.
- **Navigasi HTML** memungkinkan pengguna berpindah dari satu halaman ke halaman lain atau bagian tertentu dalam halaman.
- Elemen semantik HTML mempermudah pengembangan dan meningkatkan pengalaman pengguna serta SEO.


