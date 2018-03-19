#Pengenalan Model View Controller (Bagian 2)
{{'https://www.youtube.com/watch?v=YtjdrSS_dQw'|video}}
##Pengertian Model
Model merepresentasikan struktur data dari applikasi yang dibuat, biasanya model berisi fungsi untuk mengambil, menyimpan dan merubah informasi pada database.

Pada sebuah framework yang menggunakan design pattern MVC, maka kode program dipisahkan menjadi tiga bagian besar yaitu Model, View dan Controller. Pemisahan bagian kode program ini bertujuan agar proses pengembangan software menjadi lebih mudah dan teratur.

Pemisahan kode program menjadi 3 bagian M(model), V(view), dan C(controller) ini wajib diikuti oleh pengembang software, walaupun secara teknis bisa saja mencampur kode program dalam satu file yang sama.

MVC banyak digunakan di berbagai macam framework, khususnya pada framework Code Igniter.
Untuk menambah pengetahuan mengenai design pattern MVC silahkan merujuk pada link berikut ini :

* [Codeigniter Manual](https://www.codeigniter.com/user_guide/overview/mvc.html)
* [What is MVC](https://softwareengineering.stackexchange.com/questions/127624/what-is-mvc-really)

##Model Pada Codeigniter

Untuk membuat model pada framework codeigniter dapat dilakukan dengan aturan sebagai berikut :

* Semua file model di codeigniter secara default disimpan di folder models:

```
codeigniter
├── application
│   ├── controllers
│   ├── models
│   ├── views
├── assets
│   ├── css
│   ├── fonts
│   └── js
```

* Semua file models dalam codeigniter merupakan sebuah **class** yang diturunkan dari class CI_Model

```
class Blog_model extends CI_Model{

}
```

* Best practice nya pada file file yang ada di folder models pada codeigniter digunakan **khusus** untuk berurusan dengan data yang dibutuhkan oleh aplikasi, baik data ini berupa data yang berada di database, maupun file.

##Cara Membuat Model

Pada contoh kali ini kita akan membuat sebuah model pada codeigniter yang akan memberikan data dari tabel biodata di database mysql.

* Buat file baru dengan nama Biodata.php pada folder models (Perhatikan dengan seksama nama file (huruf capital), dan lokasi penyimpanan file di folder models)

```
codeigniter
├── application
│   ├── controllers
│   ├── models
|   |   └── Biodata.php
│   ├── views
├── assets
│   ├── css
│   ├── fonts
│   └── js
```

* Isilah di dalam class Biodata.php kode program yang membuat class Biodata mengekstend CI_Models, perhatikan ada function `__construct()` yang merupakan bawan default untuk konstruktor pada file Model di Codeigniter.

```
class Biodata extends CI_Model{
    function __construct(){
        parent::__construct()
    }
}
```

* Setelah itu class dapat di isi dengan method method yang dibutuhkan untuk mengakses database.

##Cara Load Model

Untuk dapat digunakan sebuah model pada codeigniter harus di load terlebih dahulu oleh controller yang menggunakan model tersebut, perhatikan bahwa untuk mengikuti konsep MVC yang benar yang dapat mengakses model secara langsung hanyalah sebuah controller, view tidak boleh menginstansiasi model.

Cara melakukan load model pada sebuah controller dapat dilakukan dengan perintah berikut :

* `$this->load->model('nama_model')`
* `$this->load->model('folder/nama_file')`

Kode program pertama adalah untuk me load file model yang langsung ada di folder model, sedangkan kode program kedua untuk model yang ada di dalam folder lain pada folder models.

##Autoload Model

##Koneksi Ke Database

##Jobsheet Praktikum Pengenalan Model Koneksi Model Ke Database
##Jobsheet Praktikum Pengenalan Model Query Model Dengan Query Biasa
##Jobsheet Praktikum Pengenalan Model Query Model dengan Query Builder
