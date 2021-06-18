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

