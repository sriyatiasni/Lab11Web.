# Lab11Web.
## Nama : Sriyati Asni
## NIM : 311910697

## Langkah-langkah praktikum
## Langkah 1

Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan 
pengembangan Codeigniter 4.

Berikut beberapa ekstensi yang perlu diaktifkan:
-php-json ekstension untuk bekerja dengan JSON;
-php-mysqlnd native driver untuk MySQL;
-php-xml ekstension untuk bekerja dengan XML;
-php-intl ekstensi untuk membuat aplikasi multibahasa;
-libcurl (opsional), jika ingin pakai Curl.

Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian 
Apache klik Config -> PHP.ini

![ss XAMPP1](https://user-images.githubusercontent.com/56379905/121889995-0fb62e80-cd44-11eb-84e9-18e1a9a68aaa.png)

Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan 
diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.
![ss notepad XAMPP1](https://user-images.githubusercontent.com/56379905/121890320-67ed3080-cd44-11eb-90db-3f8826262aca.png)

## Langkah 2
## Instalasi Codeigniter 4

-Unduh Codeigniter dari website https://codeigniter.com/download
-Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.
-Ubah nama direktory framework-4.x.xx menjadi ci4.
-Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/
![ss 1](https://user-images.githubusercontent.com/56379905/121890730-e053f180-cd44-11eb-85c8-8a7bfff9253d.png)

## Langkah 3
## Menjalankan CLI (Command Line Interface)

Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk 
mengakses CLI buka terminal/command prompt.
![ss 2](https://user-images.githubusercontent.com/56379905/121891151-5193a480-cd45-11eb-82c3-ec6720cef1a8.png)

kemudian Arahkan lokasi direktori sesuai dengan direktori kerja project dibuat 
(xampp/htdocs/lab11_ci/ci4/) 
Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah:
-php spark
![ss 3](https://user-images.githubusercontent.com/56379905/121891528-bf3fd080-cd45-11eb-81b2-1af7713e9540.png)

## Langkah  4
## Mengaktifkan Mode Debugging
Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk 
mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.

![image](https://user-images.githubusercontent.com/56379905/122571557-0d6f0f80-d077-11eb-99aa-7bff49efc250.png)

Cara mengaktifkannya dengan mengubah nama file env menjadi .env kemudian buka filenya dan ubah nilai CI_ENVIRONMENT menjadi development.

![image](https://user-images.githubusercontent.com/56379905/122568426-ee22b300-d073-11eb-8247-d7720117e84c.png)

Maka pesan kesalahan akan ditampilkan.
![image](https://user-images.githubusercontent.com/56379905/122568300-cf242100-d073-11eb-8333-d8ed28eee8d4.png)

## Langkah 5
## Membuat Route
-Router terletak pada file app/config/Routes.php
-Untuk mengetahui route yg ada atau telah berjalan dapat menggunakan perintah php spark routes.

![image](https://user-images.githubusercontent.com/56379905/122568679-33df7b80-d074-11eb-9834-dc7b2c48197d.png)

Selanjutnya mencoba akses route yang telah dibuat dengan mengakses http://localhost:8080/contact
Terjadi error file not found dikarenakan tidak ada file/page untuk halaman contact.

![image](https://user-images.githubusercontent.com/56379905/122568814-58d3ee80-d074-11eb-90b4-980fc4e4a9a9.png)

## Langkah 6
## Membuat Controller
Membuat file page.php di dalam direktori Controller (/app/Controllers)
![image](https://user-images.githubusercontent.com/56379905/122568954-799c4400-d074-11eb-9b9c-7314a55d4f19.png)

Kemudian refresh browser maka halaman sudah dapat diakses dan menampilkan hasilnya.
![image](https://user-images.githubusercontent.com/56379905/122569493-fd563080-d074-11eb-8cd2-0db0b95daf92.png)

## Selanjutnya Menambahkan method baru pada controller page.
Method ini dapat diakses dengan menggunakan alamat: http://localhost:8080/page/tos
![image](https://user-images.githubusercontent.com/56379905/122569579-15c64b00-d075-11eb-90f1-3dfedd8d6210.png)
## Langkah 7
## Membuat View
Membuat file about.php di dalam direktori View (/app/view/about.php)
![image](https://user-images.githubusercontent.com/56379905/122569711-37bfcd80-d075-11eb-8c36-58076867f407.png)
## selanjutnya Mengubah method about dalam controller page.
![image](https://user-images.githubusercontent.com/56379905/122569794-4c9c6100-d075-11eb-9ccb-d076a06f74a8.png)
Maka akan tampil seperti ini
![image](https://user-images.githubusercontent.com/56379905/122569861-5d4cd700-d075-11eb-8213-3dce07207dcf.png)
## Langkah 8
## Membuat Layout Web dengan CSS
Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout).
![image](https://user-images.githubusercontent.com/56379905/122569966-7b1a3c00-d075-11eb-8615-b714f7c4a652.png)
## Kemudian buat folder template pada direktori view, lalu buat file header.php dan footer.php.
![image](https://user-images.githubusercontent.com/56379905/122570040-9127fc80-d075-11eb-8fd6-65aed6f30a53.png)
![image](https://user-images.githubusercontent.com/56379905/122570068-97b67400-d075-11eb-8946-94ec0d25f35e.png)
## Kemudian ubah file about.php (/app/view/about.php) seperti berikut.

<?= $this->include('template/header'); ?>
<h1><?= $title; ?></h1>
<hr>
<p><?= $content; ?></p>
<?= $this->include('template/footer'); ?>
Kemudian refresh browser atau akses alamat http://localhost:8080/about
![image](https://user-images.githubusercontent.com/56379905/122570258-c6344f00-d075-11eb-9c76-e8185e88da7b.png)

## Pertanyaan dan Tugas
Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

## Hasil tugas
![image](https://user-images.githubusercontent.com/56379905/122570822-507cb300-d076-11eb-985e-961d9f9ec10f.png)





## Lab12Web
## Nama : Sriyati Asni
## NIM : 311910697
## Praktikum 12 - Pemrograman Web (Framework Lanjutan - CRUD)

## Langkah-langkah praktikum

Pastikan MySQL server sudah berjalan dan buat sebuah database sebagai berikut:
![image](https://user-images.githubusercontent.com/56379905/122574031-6e97e280-d079-11eb-827a-967d1bb3a494.png)

## Langkah 1 
## Konfigurasi Database
Membuat konfigurasi hubungan ke database server dengan menggunakan file .env.
![image](https://user-images.githubusercontent.com/56379905/122574176-971fdc80-d079-11eb-875a-8657d58275b0.png)

## Langkah 2 
## Membuat Model
Buat file baru pada direktori /app/Models dengan nama ArtikelModel.php
![image](https://user-images.githubusercontent.com/56379905/122574269-b0288d80-d079-11eb-8137-c734f5eafea9.png)

## Langkah 3 
## Membuat Controller
Buat Controller baru dengan nama Artikel.php pada direktori /app/Controllers.
![image](https://user-images.githubusercontent.com/56379905/122574376-cb939880-d079-11eb-93f7-d88f4e89917a.png)

## Langkah 4 
## Membuat View
Buat direktori baru dengan nama artikel pada direktori /app/Views, kemudian buat file baru dengan nama index.php.
![image](https://user-images.githubusercontent.com/56379905/122574496-e6fea380-d079-11eb-9966-4a12200b6015.png)
Lalu buka alamat http://localhost:8080/artikel untuk melihat hasilnya.
Tidak ada data yang ditampilkan karena database masih kosong.
![image](https://user-images.githubusercontent.com/56379905/122574879-54123900-d07a-11eb-95e2-b91b5f5afbc1.png)

Tambahkan data pada database untuk ditampilkan datanya.
![image](https://user-images.githubusercontent.com/56379905/122575311-d1d64480-d07a-11eb-9c26-29497b60f123.png)
ketikaa di refresh akan muncul tampilan seperti ini.
![image](https://user-images.githubusercontent.com/56379905/122575475-00541f80-d07b-11eb-8473-06eb8431de9c.png)

## Langkah 5 
## Membuat Tampilan Detail Artikel
Tampilan pada saat judul berita di klik maka akan diarahkan ke halaman yang berbeda. 
Tambahkan sebuah fungsi baru pada Controller Artikel (/app/Controllers/Artikel.php) dengan nama view().
![image](https://user-images.githubusercontent.com/56379905/122575620-22e63880-d07b-11eb-943b-b296940a4441.png)

## Langkah 6 
## Membuat View Detail
Buat file baru dalam folder artikel (/app/Views/artikel/) dengan nama detail.php untuk menampilkan halaman detail.
![image](https://user-images.githubusercontent.com/56379905/122575714-385b6280-d07b-11eb-9e5b-7a72e1bc508d.png)

## Langkah 7 
## Membuat Route
Buka file Routes.php dalam folder (/app/Config/) dan tambahkan routing untuk ke halaman detail artikel.
$routes->get('/artikel/(:any)', 'Artikel::view/$1');
![image](https://user-images.githubusercontent.com/56379905/122575816-4f01b980-d07b-11eb-9a5e-3e1329dbd084.png)
Maka akan tampil halaman dari artikel yang diklik.
![image](https://user-images.githubusercontent.com/56379905/122575896-5fb22f80-d07b-11eb-8357-47414060f815.png)

## Langkah  8 
## Membuat Menu Admin
Menu admin adalah untuk proses CRUD data artikel.
Buat method atau fungsi baru pada Controller Artikel dengan nama admin_index().
![image](https://user-images.githubusercontent.com/56379905/122576005-76f11d00-d07b-11eb-93b5-72b11137775b.png)
Kemudian buat file admin_index.php dalam folder 
(/app/Views/artikel/) untuk tampilan halaman admin.
![image](https://user-images.githubusercontent.com/56379905/122576085-8a9c8380-d07b-11eb-8303-c457ef60e8ee.png)
Kemudian tambahkan routing untuk menu admin sebagai berikut:
![image](https://user-images.githubusercontent.com/56379905/122576232-ab64d900-d07b-11eb-8eb2-b657adc352d5.png)

Menu admin dapat diakses dengan alamat
http://localhost:8080/admin/artikel
![image](https://user-images.githubusercontent.com/56379905/122576323-c33c5d00-d07b-11eb-8bf9-8c5d258f63db.png)

## Langkah 9 
## Menambah Data Artikel
Tambahkan fungsi/method baru pada Controller Artikel dengan nama add().
![image](https://user-images.githubusercontent.com/56379905/122576406-dc450e00-d07b-11eb-9b16-45383750df6d.png)
Kemudian buat view untuk form tambah dengan nama form_add.php dalam folder (/app/Views/artikel/).
![image](https://user-images.githubusercontent.com/56379905/122576494-ee26b100-d07b-11eb-8e4a-36ce038361fe.png)
Tampilannya akan seperti ini
![image](https://user-images.githubusercontent.com/56379905/122576564-00a0ea80-d07c-11eb-8a82-57afb4f652a2.png)

## Langkah 10 
## Mengubah Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama edit().
![image](https://user-images.githubusercontent.com/56379905/122576631-131b2400-d07c-11eb-830c-e3df763a662b.png)
Kemudian buat view untuk form tambah dengan nama form_edit.php dalam folder (/app/Views/artikel/).
![image](https://user-images.githubusercontent.com/56379905/122576680-21694000-d07c-11eb-91ae-c211aedc45fc.png)
Maka tampilannya akan seperti ini ketika ingin mengubah data.
![image](https://user-images.githubusercontent.com/56379905/122576745-37770080-d07c-11eb-9806-68a63d108e0e.png)

## Langkah 11 
## Menghapus Data
Tambahkan fungsi/method baru pada Controller Artikel dengan nama delete().
![image](https://user-images.githubusercontent.com/56379905/122576806-4c539400-d07c-11eb-9a06-f3630dc0d195.png)


## Pertanyaan dan Tugas
## Selesaikan programnya sesuai Langkah-langkah yang ada. Anda boleh melakukan improvisasi.

## Jawab
Saya telah menyelesaikan program diatas sehingga semua programnya bisa berjalan dengan baik dan benar. 

