# Pengantar Model View Controller

Framework CodeIgniter menggunakan paradigma MVC yang merupakan singkatan dari
Model View Controller.

- Model

Model merepresentasikan struktur data dari aplikasi yang dibuat. Biasanya model
berisi fungsi untuk **mengambil**, **menyimpan** dan **merubah** informasi pada
database.

- View

Informasi yang ditampilkan ke user, biasanya berupa sebuah halaman atau bagian
dari halaman seperti header/footer.

- Controller

Penghubung antara model dan view, biasanya bertugas sebagai pengatur alur logika
aplikasi.

Tetapi pada pertemuan ini hanya akan ditekankan pada pembahasan `controller`
saja.

# Controller

Sebelum membuat `controller` pada `CodeIgniter` ada beberapa ketentuan yang
perlu diperhatikan, antara lain:

- Nama file dimulai dengan huruf kapital (akan sangat berpengaruh jika anda
menggunakan sistem operasi yang filesystemnya sifatnya *case sensitive*).
- Penamaan `class` dimulai dengan huruf kapital.
- `controller` harus merupakan turunan dari `class` bawaan dari `Codeigniter`,
yaitu **CI_Controller**.

## Pretty URL

Pada pertemuan 1, jika anda perhatikan link hasil dari helper `site_url` akan
selalu diakhiri dengan `index.php`. Untuk merubah url sehingga didapatkan url
tanpa akhiran `index.php` dapat digunakan `pretty url` dengan konfigurasi
`.htaccess` (file `.htaccess` hanya tersedia di web server Apache). Contoh:

```
// Tanpa pretty url
http://localhost/folder/index.php/controller/method/param
```

```
// Dengan pretty url
http://localhost/folder/controller/method/param
```

## Controller dengan Parameter

Controller dapat menerima informasi dari `view` atau `request` melalui
parameter. Untuk pembuatan tersebut, cukup ditambahkan deklarasi parameter di
dalam tanda `()` pada fungsi. Anda dapat menambahkan lebih dari satu jumlah
parameter (sesuaikan dengan kebutuhan). Contoh:

```php
<?php
defined('BASEPATH') OR exit('No direct script access allowed');

class Welcome extends CI_Controller {

  /**
   * Index Page for this controller.
   *
   * Maps to the following URL
   * 		http://example.com/index.php/welcome
   *	- or -
   * 		http://example.com/index.php/welcome/index
   *	- or -
   * Since this controller is set as the default controller in
   * config/routes.php, it's displayed at http://example.com/
   *
   * So any other public methods not prefixed with an underscore will
   * map to /index.php/welcome/<method_name>
   * @see https://codeigniter.com/user_guide/general/urls.html
   */
  public function index()
  {
    $this->load->view('welcome_message');
  }

  public function about()
  {
    $this->load->view('about');
  }
}
```

## Controller dengan Custom Routing

Contoh:

```
$route['journals'] = 'blogs'
$route['blog/joe'] = 'blogs/users/34'
$route['product/(:num)'] = 'catalog/product_lookup_by_id/$1'
```

## Praktikum Controller 1

Pada praktikum ini berisi tentang pembuatan halaman static pada CodeIgniter. Ada
tiga buah halaman static yang akan dibuat, yaitu: **home**, **about** dan
**contact**.

- Tambahkan `url` helper pada `autoload` yang ada di file
`application/config/autoload.php`.

```php
$autoload['helper'] = array('url');
```

- Buatlah tiga file `home.php`, `about.php` dan `contact.php` pada views
`Codeigniter`.
- Buatlah tiga file controller `Home.php`, `About.php` dan `Contact.php`
(perhatikan penamaan file, diawali dengan huruf kapital).

## Praktikum Controller 2

Pada praktikum ini membahas tentang pengiriman data dari controller ke view.
