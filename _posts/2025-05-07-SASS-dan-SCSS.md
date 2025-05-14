---
layout: post
title: "Menggunakan SASS dan SCSS di Jekyll"
date: 2025-02-22
---

# 🎨 Menggunakan SASS dan SCSS di Jekyll

Jekyll secara bawaan mendukung **SASS/SCSS**, yaitu ekstensi dari CSS yang memungkinkan penggunaan variabel, nested rules, mixins, dan banyak lagi. Ini sangat berguna untuk membuat gaya situs yang lebih rapi dan modular.

## 💡 Apa Itu SASS dan SCSS?

- **SASS (Syntactically Awesome Stylesheets)** adalah preprocessor CSS yang memperkenalkan sintaks yang lebih efisien dan fitur tambahan.
- **SCSS** adalah varian dari SASS yang menggunakan sintaks mirip CSS. Ini adalah format yang lebih umum dan mudah diadopsi.

Contoh SCSS:

```scss
$primary-color: #3498db;

body {
  font-family: sans-serif;
  background-color: $primary-color;

  h1 {
    font-size: 2rem;
  }
}
````

## 📁 Struktur File SCSS di Jekyll

Jekyll mengharapkan file SCSS berada di dalam folder bernama `_sass`, dan satu file utama SCSS (biasanya `main.scss`) berada di dalam folder `assets/css/`.

**Contoh struktur:**

```
.
├── _sass/
│   └── _variables.scss
├── assets/
│   └── css/
│       └── main.scss
```

## 📦 Menggunakan SCSS dalam Proyek Jekyll

1. **Buat folder `_sass/`** di root proyek Anda.

2. **Tambahkan file partial SCSS**, misalnya `_variables.scss`:

   ```scss
   $bg-color: #f4f4f4;
   ```

3. **Buat file utama `main.scss` di `assets/css/`**:

   ```scss
   ---
   ---
   @import "variables";

   body {
     background-color: $bg-color;
   }
   ```

   > Baris `---` di atas wajib untuk memberi tahu Jekyll memproses file ini melalui Liquid dan SASS.

4. **Tambahkan ke layout HTML Anda:**

   ```html
   <link rel="stylesheet" href="{{ '/assets/css/main.css' | relative_url }}">
   ```

## ⚙️ Konfigurasi di `_config.yml`

Jika Anda ingin mengatur output CSS dari SCSS, tambahkan ini di `_config.yml`:

```yml
sass:
  style: compressed # atau nested, expanded, compact
```

Nilai `compressed` akan menghasilkan file CSS yang lebih kecil.

## 🧪 Tips Penggunaan

* Gunakan **partial** (file SCSS yang diawali dengan `_`) untuk membagi-bagi style berdasarkan komponen.
* Hindari menaruh CSS di dalam HTML; SCSS lebih terstruktur dan mudah dipelihara.
* Manfaatkan fitur seperti **mixin**, **extend**, dan **functions** untuk membuat style yang reusable.

## ✅ Kesimpulan

* Jekyll mendukung SCSS secara bawaan tanpa konfigurasi tambahan.
* SCSS membantu Anda menulis CSS yang lebih bersih, modular, dan mudah dikelola.
* Manfaatkan struktur file `_sass` dan `assets/css` untuk mengatur style Anda dengan baik.

```
