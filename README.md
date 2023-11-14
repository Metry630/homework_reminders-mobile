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


<h1>Tugas 8</h1>


<h2>Perbedaan antara Navigator.push() dan Navigator.pushReplacement()</h2> 

Fungsi `Navigator.push()` digunakan untuk menambahkan rute baru ke dalam tumpukan navigasi tanpa menghapus rute sebelumnya. Sebaliknya, `Navigator.pushReplacement()` berfungsi untuk menggantikan rute saat ini dengan rute baru. Sebagai contoh, ketika berpindah dari halaman A ke halaman B, penggunaan `Navigator.push()` akan menambahkan halaman B ke dalam tumpukan, sementara `Navigator.pushReplacement()` akan menggantikan halaman A dengan halaman B.

```dart
// Contoh Navigator.push()
Navigator.push(
  context,
  MaterialPageRoute(builder: (context) => HalamanB()),
);

// Contoh Navigator.pushReplacement()
Navigator.pushReplacement(
  context,
  MaterialPageRoute(builder: (context) => HalamanB()),
);
```

<h2>Layout Widget pada Flutter dan Konteks Penggunaannya</h2>

1. **Container**: Berfungsi untuk menempatkan widget lain dalam suatu kotak dengan batas dan dekorasi tertentu.
2. **Column**: Mengatur widget dalam susunan kolom vertikal.
3. **Row**: Menyusun widget dalam baris horizontal.
4. **Stack**: Menempatkan widget di atas satu sama lain.

Contoh penggunaan:

```dart
Column(
  children: [
    Text('Widget 1'),
    Text('Widget 2'),
  ],
);

Container(
  width: 100,
  height: 100,
  color: Colors.blue,
  child: Text('Container Widget'),
);

Stack(
  children: [
    Positioned(
      top: 10,
      left: 10,
      child: Text('Top Left'),
    ),
    Positioned(
      bottom: 10,
      right: 10,
      child: Text('Bottom Right'),
    ),
  ],
);
```

<h2>Elemen Input pada Form dan Penjelasannya</h2>

Elemen input pada formulir ini mencakup `TextField` untuk memasukkan teks dan `DropdownButton` untuk pemilihan opsi. Penggunaan keduanya memungkinkan pengguna untuk memasukkan teks dan memilih opsi dari daftar dropdown dengan mudah. `TextField` umumnya digunakan untuk input teks seperti nama atau alamat, sementara `DropdownButton` berguna untuk memilih opsi seperti jenis kelamin atau status.

<h2>Penerapan Clean Architecture pada Aplikasi Flutter</h2> 

Penerapan Clean Architecture pada aplikasi Flutter melibatkan pembagian aplikasi ke dalam beberapa lapisan: **Domain Layer** (logika bisnis), **Data Layer** (akses data), dan **Presentation Layer** (antarmuka pengguna). Setiap lapisan memiliki tanggung jawabnya sendiri, mempermudah pengujian dan pemeliharaan.

Contoh struktur proyek:

- `lib/domain`: Mengandung logika bisnis dan aturan aplikasi.
- `lib/data`: Menangani akses data dari API atau database.
- `lib/presentation`: Berisi tampilan dan logika presentasi.

Penerapan clean architecture membantu memisahkan konsep dan memastikan fleksibilitas serta uji coba yang lebih baik dalam pengembangan aplikasi Flutter.

<h2>Cara implementasi</h2>

1. **Menambahkan Drawer Menu untuk Navigasi:**
   - Saya membuat berkas baru `left_drawer.dart` dalam direktori widgets.
   - Saya mengimpor halaman-halaman yang ingin saya tambahkan navigasinya.
   - Saya menambahkan routing untuk halaman-halaman tersebut.
   - Saya mendesain drawer dengan menambahkan drawer header.
   - Saya memasukkan drawer ke halaman yang ingin saya tambahkan drawer.

2. **Menambahkan Form dan Elemen Input:**
   - Saya membuat berkas baru `shoplist_form.dart` dalam direktori lib.
   - Saya mengimplementasikan Form, SingleChildScrollView, dan TextFormField.
   - Saya menggunakan GlobalKey<FormState> untuk validasi dan penanganan form state.
   - Saya membuat TextFormField untuk input Nama Produk, Harga, dan Deskripsi.
   - Saya menambahkan tombol "Save" untuk menyimpan data dengan menggunakan showDialog() untuk menampilkan hasil.

3. **Memunculkan Data:**
   - Saya mengimplementasikan showDialog() untuk menampilkan hasil penyimpanan.
   - Saya mereset form setelah data disimpan.

4. **Menambahkan Fitur Navigasi pada Tombol:**
   - Saya menggunakan `Navigator.push` pada tombol untuk navigasi ke halaman lain.
   - Saya memberikan contoh implementasi pada tombol "Tambah Produk" untuk menuju `ShopFormPage`.

5. **Refactoring File:**
   - Saya membuat berkas `shop_card.dart` pada direktori widgets.
   - Saya memindahkan isi widget `ShopItem` dari `menu.dart` ke `shop_card.dart`.
   - Saya membuat folder `screens` pada direktori lib.
   - Saya memindahkan file `menu.dart` dan `shoplist_form.dart` ke dalam folder `screens` dengan menggunakan fitur refactoring pada IDE atau text editor.