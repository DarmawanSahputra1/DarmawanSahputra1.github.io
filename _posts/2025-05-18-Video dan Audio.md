---
layout: post
title: "Video dan Audio"
date: 2025-05-18
---

# Materi Lengkap HTML Audio dan Video

## 1. Pengantar

HTML5 menyediakan tag khusus untuk menampilkan media audio dan video secara langsung di halaman web tanpa plugin tambahan seperti Flash.

---

## 2. Tag `<audio>`

Digunakan untuk menyisipkan file audio.

### Contoh:

```html
<audio controls>
  <source src="audio/musik.mp3" type="audio/mpeg">
  Browser Anda tidak mendukung tag audio.
</audio>
```

### Atribut:

* `controls`: Menampilkan kontrol pemutar
* `autoplay`: Memutar otomatis saat halaman dimuat
* `loop`: Memutar ulang secara terus-menerus
* `muted`: Memulai dalam keadaan senyap
* `preload`: Petunjuk pemuatan (auto, metadata, none)

### Format Umum:

* MP3 (`audio/mpeg`)
* OGG (`audio/ogg`)
* WAV (`audio/wav`)


## 3. Tag `<video>`

Digunakan untuk menyisipkan file video.

### Contoh:

```html
<video width="320" height="240" controls>
  <source src="video/film.mp4" type="video/mp4">
  Browser Anda tidak mendukung tag video.
</video>
```

### Atribut:

* `controls`: Menampilkan kontrol
* `autoplay`, `loop`, `muted`
* `poster`: Gambar awal sebelum video diputar
* `width`, `height`: Ukuran tampilan video

### Format Umum:

* MP4 (`video/mp4`)
* WebM (`video/webm`)
* OGV (`video/ogg`)


## 4. Multi-Format dan Fallback

Gunakan beberapa tag `<source>` agar mendukung berbagai browser:

```html
<video controls>
  <source src="video/video.mp4" type="video/mp4">
  <source src="video/video.webm" type="video/webm">
  Browser Anda tidak mendukung pemutaran video.
</video>
```


## 5. Menyematkan YouTube

Selain file lokal, video dari YouTube bisa disisipkan:

```html
<iframe width="560" height="315" src="https://www.youtube.com/embed/ID_VIDEO" frameborder="0" allowfullscreen></iframe>
```


## 6. Tips

* Simpan file di folder `audio/` atau `video/`
* Kompres ukuran file agar tidak berat saat dimuat
* Pastikan format didukung oleh semua browser target


## 7. Referensi

* [MDN Web Docs - Audio](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio)
* [MDN Web Docs - Video](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video)
