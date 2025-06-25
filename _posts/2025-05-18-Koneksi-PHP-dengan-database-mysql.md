---
layout: post
title: "Koneksi PHP dengan database mysql"
date: 2025-05-18
---

# Materi Lengkap Koneksi PHP dengan Database MySQL

## 1. Pengantar

Koneksi antara PHP dan MySQL diperlukan agar aplikasi web dapat menyimpan dan mengambil data dari database.


## 2. Persiapan

* Pastikan server web (Apache) dan MySQL berjalan (gunakan XAMPP, Laragon, atau lainnya)
* Buat database terlebih dahulu (misalnya: `db_sekolah`)

Contoh pembuatan database via PHPMyAdmin:

```sql
CREATE DATABASE db_sekolah;
```

## 3. Membuat File Koneksi

### a. Menggunakan MySQLi (prosedural)

```php
<?php
$host = "localhost";
$user = "root";
$pass = "";
$db   = "db_sekolah";

$koneksi = mysqli_connect($host, $user, $pass, $db);

if (!$koneksi) {
  die("Koneksi gagal: " . mysqli_connect_error());
} else {
  echo "Koneksi berhasil.";
}
?>
```

### b. Menggunakan MySQLi (OOP)

```php
<?php
$koneksi = new mysqli("localhost", "root", "", "db_sekolah");

if ($koneksi->connect_error) {
  die("Koneksi gagal: " . $koneksi->connect_error);
} else {
  echo "Koneksi berhasil.";
}
?>
```

### c. Menggunakan PDO

```php
<?php
try {
  $koneksi = new PDO("mysql:host=localhost;dbname=db_sekolah", "root", "");
  $koneksi->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
  echo "Koneksi berhasil";
} catch(PDOException $e) {
  echo "Koneksi gagal: " . $e->getMessage();
}
?>
```


## 4. Contoh Penggunaan Koneksi

Menampilkan data dari tabel `siswa`:

```php
<?php
include 'koneksi.php';

$data = mysqli_query($koneksi, "SELECT * FROM siswa");
while($row = mysqli_fetch_assoc($data)) {
  echo $row['nama'] . "<br>";
}
?>
```


## 5. Menutup Koneksi

```php
mysqli_close($koneksi); // untuk MySQLi
$koneksi = null;         // untuk PDO
```


## 6. Tips

* Gunakan prepared statement untuk keamanan (hindari SQL Injection)
* Simpan file koneksi di luar folder publik (htdocs)
* Pisahkan file koneksi dari file utama untuk efisiensi

## 7. Referensi

* [PHP Manual - mysqli](https://www.php.net/manual/en/book.mysqli.php)
* [W3Schools PHP MySQL Connect](https://www.w3schools.com/php/php_mysql_connect.asp)
