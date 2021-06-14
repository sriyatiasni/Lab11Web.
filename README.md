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


