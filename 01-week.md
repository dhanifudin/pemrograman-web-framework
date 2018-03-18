# Pengantar dan Pengenalan Web Framework

## Persiapan

### Perangkat Lunak

* Xampp / Wamp / (PHP + Apache + MySql)
* Text Editor/IDE
* Git (Referensi: [Try Github](http://try.github.com))

### Editor

> Your editor is your Katana

Perkuliahan ini tidak mewajibkan anda untuk menggunakan suatu text editor/IDE
tertentu (gunakan sesuai preferensi anda).

Beberapa text editor/IDE yang umum digunakan antara lain:

* Sublime Text 3
* Visual Studio Code
* Atom
* Notepad++
* Webstorm
* Emacs
* Vim

Recommended Settings & Plugins

* Linter
  * [Sublime Text 3](https://github.com/SublimeLinter/SublimeLinter-php)
  * [VS Code](https://code.visualstudio.com/docs/languages/php#_linting)
* [Emmet](https://emmet.io/download/)
* CodeIgniter 3 Snippet
* Bootstrap 3 Snippet
* Bootstrap 3 Autocomplete

## Instalasi CodeIgniter

{{'https://www.youtube.com/watch?v=4gIm35pDNSo'|video}}
Unduh paket CodeIgniter 3 pada halaman [CodeIgniter
Download](https://codeigniter.com/download). Pastikan versi yang diunduh adalah
versi 3.x (versi saat modul ini ditulis adalah 3.1.7).

Panduan lebih lengkap dapat dilihat di [Docs CodeIgniter
3](https://www.codeigniter.com/userguide3/installation/index.html)

## Konfigurasi CodeIgniter

File-file yang berkaitan dengan konfigurasi CodeIgniter, antara lain:

* `application/config/config.php`
* `application/config/database.php`
* `application/config/routes.php`

## Instalasi Twitter Bootstrap

Untuk menginstall Twitter Bootstrap, unduh pada halaman [Download Twitter
Bootstrap](http://getbootstrap.com/getting-started/#download). Kemudian ekstrak file yang telah didownload. Dalam folder tersebut terdapat tiga folder utama, yaitu: `css`, `js`, `font`.

### Percobaan Twitter Bootstrap

* Buatlah direktori dengan nama `hello-bootstrap` pada direktori `htdocs` web server.
* Tambahkan file `index.php` pada direktori tersebut.
* Copy file `css`, `js` serta `font` ke dalam direktori, sehingga terbentuk struktur seperti berikut.

```
- hello-bootstrap
  - css
  - font
  - js
  - index.php
```

* Buatlah struktur dasar html seperti di bawah ini

```html
<!DOCTYPE html>
<html>
<head>
<title>Hello Bootstrap</title>
</head>
<body>

</body>
</html>
```

* Tambahkan css bootstrap pada bagian `head`.

```html
<link href="css/bootstrap.min.css" rel="stylesheet">
```

* Tambahkan js bootstrap pada bagian akhir `body`.

```html
<script src="js/bootstrap.min.js"></script>
```

* Tuliskan kode berikut untuk menampilkan isi halaman.

```html
<h1 class="text-center">Hello Bootstrap</h1>
```

## Integrasi Twitter Bootstrap dengan CodeIgniter
