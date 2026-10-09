# 📦 Product Manager

🖥️ **Aplikasi Manajemen Produk Berbasis PHP dan MySQL**

**Mata Kuliah:** Pemrograman Web\
**Materi:** Integrasi PHP, MySQL, dan UI Styling\
**Pertemuan:** 3\
**Mini Project:** Product Manager

------------------------------------------------------------------------

## 📌 Deskripsi Proyek

Product Manager merupakan aplikasi berbasis web yang digunakan untuk
mengelola data produk menggunakan PHP dan MySQL. Aplikasi ini menerapkan
konsep CRUD (*Create, Read, Update, Delete*) untuk menambah,
menampilkan, mengubah, dan menghapus data produk.

Proyek ini juga menerapkan validasi input, keamanan database menggunakan
PDO dan prepared statement, serta desain antarmuka responsif menggunakan
CSS Box Model dan Flexbox.

## 🎯 Tujuan Proyek

-   Memahami arsitektur client-server dan HTTP request-response.
-   Memahami penggunaan method GET dan POST.
-   Menerapkan validasi data pada sisi server.
-   Menghubungkan PHP dengan database MySQL menggunakan PDO.
-   Mengimplementasikan operasi CRUD.
-   Menerapkan keamanan output untuk mencegah XSS.
-   Menggunakan CSRF token untuk melindungi operasi penghapusan.
-   Membuat tampilan produk yang responsif menggunakan CSS.

## ⚙️ Teknologi yang Digunakan

-   **PHP** --- pemrosesan logika aplikasi.
-   **MySQL** --- penyimpanan data produk.
-   **HTML** --- struktur halaman dan formulir.
-   **CSS** --- styling antarmuka dan layout responsif.
-   **PDO** --- koneksi database dan prepared statement.

## ✨ Fitur Utama

1.  **Create Produk** --- menambahkan produk dengan nama, kategori,
    harga, dan stok.
2.  **Read Produk** --- menampilkan daftar produk dalam bentuk card
    responsif.
3.  **Update Produk** --- mengubah data produk berdasarkan ID.
4.  **Delete Produk** --- menghapus produk melalui method POST dengan
    perlindungan CSRF.
5.  **Validasi Input** --- memastikan nama minimal 3 karakter, harga
    lebih dari 0, dan stok tidak negatif.
6.  **Pencegahan Duplikasi** --- menerapkan pola Post--Redirect--Get
    (PRG) agar pengiriman ulang formulir tidak membuat data ganda.
7.  **Keamanan Database** --- menggunakan prepared statement untuk
    memisahkan query SQL dari input pengguna.
8.  **Keamanan Output** --- menggunakan `htmlspecialchars()` untuk
    membantu mencegah XSS.
9.  **Search dan Filter** --- fitur tambahan untuk mencari produk
    berdasarkan nama atau kategori.

## 🗄️ Struktur Database

Database yang digunakan bernama `store_db` dengan tabel `products`.

  Kolom          Tipe Data       Keterangan
  -------------- --------------- ----------------------------------
  `id`           INT             Primary key dan identitas produk
  `name`         VARCHAR(100)    Nama produk, harus unik
  `category`     VARCHAR(50)     Kategori produk
  `price`        DECIMAL(12,2)   Harga produk
  `stock`        INT             Jumlah stok produk
  `created_at`   TIMESTAMP       Waktu data dibuat

## 📁 Struktur Folder Proyek

``` text
product-manager/
├── config/
│   └── db.php
├── public/
│   ├── index.php
│   ├── create.php
│   ├── edit.php
│   ├── delete.php
│   └── assets/
│       └── style.css
└── database/
    └── store_db.sql
```

## 🔒 Keamanan dan Validasi

Aplikasi menerapkan beberapa mekanisme keamanan dasar:

-   Validasi input pada sisi server menggunakan PHP.
-   Prepared statement untuk query database.
-   `htmlspecialchars()` untuk mengamankan output HTML.
-   CSRF token untuk melindungi proses penghapusan.
-   Konfirmasi antarmuka sebelum menghapus data.
-   Redirect setelah proses penyimpanan menggunakan pola PRG.

## 🚀 Cara Menjalankan Proyek

1.  Siapkan lingkungan PHP dan MySQL, misalnya XAMPP.
2.  Buat database `store_db` dan impor file `database/store_db.sql`.
3.  Sesuaikan konfigurasi koneksi database pada `config/db.php`.
4.  Jalankan server web dan pastikan PHP serta MySQL aktif.
5.  Buka aplikasi melalui browser menggunakan alamat lokal yang sesuai
    dengan konfigurasi server.

## 🧪 Pengujian

Pengujian dilakukan dengan beberapa skenario:

-   Menambahkan produk dengan data valid.
-   Memastikan nama produk kurang dari 3 karakter ditolak.
-   Memastikan harga dan stok negatif ditolak.
-   Memastikan nama produk tidak duplikat.
-   Menguji refresh setelah menambahkan produk.
-   Menguji keamanan tampilan dengan input HTML.
-   Memastikan card produk tetap rapi pada layar berukuran kecil.

## 📚 Kesimpulan

Proyek Product Manager merupakan penerapan materi Pemrograman Web
Pertemuan 3 yang mengintegrasikan PHP, MySQL, HTML, dan CSS. Melalui
proyek ini, mahasiswa mempelajari pengelolaan data produk menggunakan
CRUD, validasi input, keamanan database, serta pembuatan antarmuka web
yang responsif.

------------------------------------------------------------------------

**Materi:** Pemrograman Web --- Pertemuan 3\
**Proyek:** Product Manager
