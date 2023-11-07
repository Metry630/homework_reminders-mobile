<h1>Tugas 7</h1>


<h2>1. Apa perbedaan utama antara stateless dan stateful widget dalam konteks pengembangan aplikasi Flutter?</h2>

Dalam pengembangan aplikasi Flutter, stateless widget dan stateful widget memiliki perbedaan utama dalam cara mereka mengelola perubahan data dan tampilan dalam aplikasi. Perbedaan utama antara keduanya adalah sebagai berikut:

Stateless Widget:


Widget stateless adalah jenis widget yang tidak memiliki keadaan internal yang dapat berubah setelah dibuat.

Mereka ideal digunakan untuk bagian tampilan yang tidak memerlukan perubahan atau tidak bergantung pada data yang mungkin berubah.

Dengan menggunakan stateless widget, Anda tidak perlu secara eksplisit memerintahkan Flutter untuk merender ulang tampilan saat ada perubahan data; proses ini akan dilakukan otomatis oleh Flutter sesuai kebutuhan.

Contoh penggunaan stateless widget mencakup ikon, teks, gambar, dan elemen antarmuka pengguna (UI) yang bersifat statis.

Stateful Widget:

Widget stateful, sebaliknya, memiliki keadaan internal (state) yang dapat berubah selama siklus hidupnya.

Mereka sangat berguna untuk bagian tampilan yang perlu merespons perubahan data atau input dari pengguna.

Ketika terjadi perubahan data atau input yang mempengaruhi tampilan, Anda harus memanggil metode setState untuk memicu pembaruan tampilan widget. Langkah ini akan memaksa Flutter untuk merender ulang widget dengan keadaan yang baru.

Contoh penggunaan stateful widget mencakup formulir, daftar item yang dapat di-scroll, dan elemen antarmuka pengguna yang memerlukan pembaruan dinamis.

Perbedaan utama antara keduanya terletak pada cara mereka mengelola perubahan tampilan dan keadaan dalam aplikasi Flutter. Stateless widget cocok untuk elemen tampilan yang bersifat statis, sementara stateful widget cocok untuk elemen tampilan yang memerlukan perubahan dan interaktivitas.

<h2>2. Sebutkan seluruh widget yang kamu gunakan untuk menyelesaikan tugas ini dan jelaskan fungsinya masing-masing.</h2>

menu.dart:
1. Scaffold:
   - Scaffold adalah kerangka dasar yang menyediakan elemen-elemen dasar seperti AppBar dan body. Ini adalah komponen utama yang digunakan untuk mengatur struktur dasar halaman.
   
2. AppBar:
   - AppBar adalah komponen yang menampilkan bilah atas pada halaman dengan judul "Homework Reminders".

3. SingleChildScrollView:
   - SingleChildScrollView adalah widget yang mengizinkan kontennya dapat di-scroll. Ini digunakan untuk mengelola konten yang mungkin lebih panjang daripada layar.

4. Padding:
   - Padding adalah widget yang digunakan untuk menambahkan ruang sekitar kontennya. Dalam kode ini, itu digunakan untuk memberikan jarak sekitar elemen-elemen dalam Column.

5. Column:
   - Column adalah widget yang digunakan untuk mengatur anak-anaknya secara vertikal. Ini digunakan di dalam SingleChildScrollView untuk menata konten vertikal.

6. Text:
   - Widget Text digunakan untuk menampilkan teks "PBP Shop" dengan gaya teks tertentu.

7. GridView.count:
   - GridView.count adalah widget yang digunakan untuk membuat tampilan grid dengan jumlah kolom tetap. Ini digunakan untuk menampilkan item toko (ShopItem) dalam tampilan grid.

8. ShopCard:
   - ShopCard adalah widget kustom yang digunakan untuk menampilkan item toko (ShopItem) dalam sebuah kartu (Card). Ini juga menangani tindakan ketika kartu ditekan, menampilkan SnackBar dengan pesan yang sesuai.

9. ShopItem:
   - ShopItem adalah kelas yang merepresentasikan item toko dengan nama dan ikonnya.

10. List<ShopItem> items:
    - Ini adalah daftar item toko yang digunakan untuk menginisialisasi elemen-elemen dalam GridView.

main.dart:

1. MaterialApp:
   - MaterialApp adalah widget yang digunakan untuk mengatur aplikasi Flutter. Ini menyediakan konfigurasi global untuk aplikasi, termasuk judul aplikasi dan tema.

2. title:
   - Properti title digunakan untuk mengatur judul aplikasi Flutter ("Flutter Demo" dalam kasus ini).

3. theme:
   - Properti theme digunakan untuk mengatur tema aplikasi. Di sini, tema didefinisikan menggunakan ThemeData.

4. ThemeData:
   - ThemeData adalah widget yang digunakan untuk mengatur tema aplikasi. Ini mencakup berbagai properti seperti warna, fon, dan sebagainya. Di sini, warna dasar (seedColor) diatur sebagai Colors.indigo, dan useMaterial3 diatur sebagai true.

5. home:
   - Properti home digunakan untuk menentukan halaman awal aplikasi, dalam hal ini MyHomePage.

6. MyHomePage:
   - MyHomePage adalah halaman utama dari aplikasi. Ini adalah widget yang digunakan untuk menampilkan konten utama aplikasi. Namun, definisi kode untuk MyHomePage tidak disediakan dalam kode yang Anda berikan.

<h2>Implementasi Checklist</h2>

1. Saya membuka Terminal atau Command Prompt.
2. Saya masuk ke direktori tempat saya ingin menyimpan proyek Flutter.
3. Saya membuat proyek Flutter baru dengan nama homework_reminders, lalu saya masuk ke dalam direktori proyek tersebut.
   ```
   flutter create homework_reminders
   cd homework_reminders
   ```
4. Saya menjalankan proyek dengan perintah:
   ```
   flutter run
   ```

5. Saya membuat file baru bernama menu.dart di direktori homework_reminders/lib.
6. Saya menambahkan kode berikut pada baris pertama file menu.dart:
   ```
   import 'package:flutter/material.dart';
   ```
7. Saya memindahkan kode dari file main.dart yang berisi class MyHomePage ke dalam file menu.dart.
8. Saya menambahkan impor yang diperlukan di file main.dart untuk mengatasi masalah perpindahan class MyHomePage ke file menu.dart.
9. Saya menjalankan proyek untuk memastikan aplikasi tetap berjalan dengan baik.
10. Saya mengubah tema warna aplikasi menjadi indigo dengan mengedit kode di main.dart.
11. Saya mengubah sifat widget halaman menu dari stateful menjadi stateless di file main.dart dan menu.dart.
12. Saya mendefinisikan tipe ShopItem yang berisi nama dan ikon barang.
13. Saya menambahkan daftar barang-barang yang dijual ke dalam proyek.
14. Saya menambahkan kode untuk menampilkan teks dan kartu yang mewakili barang yang dijual.
15. Saya membuat widget stateless baru bernama ShopCard untuk menampilkan kartu dengan ikon dan teks.

Dengan mengikuti langkah-langkah ini, saya dapat memulai dengan Flutter, merapikan struktur proyek, dan membuat widget sederhana untuk aplikasi saya.