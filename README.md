JOBSHEET 6 - FLUTTER 3

LANGKAH 1 : Mmebuat project flutter baru

LANGKAH 2 : Menambahkan Plugin
<img width="714" height="334" alt="image" src="https://github.com/user-attachments/assets/a6095644-9495-4985-97b3-cc60afbf7e88" />
<img width="706" height="275" alt="image" src="https://github.com/user-attachments/assets/93c4c50b-b72d-4069-b34d-ae75bc21c385" />

LANGKAH 3 : Buat file red_text_widget.dart
<img width="635" height="293" alt="image" src="https://github.com/user-attachments/assets/240013f9-944f-498a-beb0-ae7dbcfe3c74" />

LANGKAH 4 : Tambah Widget AutoSizeText
<img width="642" height="351" alt="image" src="https://github.com/user-attachments/assets/34ee24d6-a2fa-46a9-8d4e-4b43e6b8100d" />
Terjadi error karena belum melakukan import package auto_size_text dan tidak ada deklarasi pada variable text

LANGKAH 5 : Buat Variabel text dan parameter di constructor
<img width="786" height="376" alt="image" src="https://github.com/user-attachments/assets/08f5efb4-7add-47b0-9085-7f66369f01b1" />

LANGKAH 6 : Tambahkan widget di main.dart
<img width="940" height="499" alt="image" src="https://github.com/user-attachments/assets/7ebed297-6a84-479f-9b8e-c0d1ab24914b" />

TUGAS PRAKTIKUM

- Jelaskan maksud dari langkah 2 pada praktikum tersebut!
  
  langkah tersebut bertujuan untuk menambahkan plugin auto_size_text ke proyek Flutter dengan perintah flutter pub add auto_size_text pada terminal. Ini mengintegrasikan library ke pubspec.yaml agar widget AutoSizeText dapat menampilkan teks dengan ukuran font yang menyesuaikan secara otomatis.

- Jelaskan maksud dari langkah 5 pada praktikum tersebut!

  Langkah tersebut bertujuan untuk menambahkan variabel final String text; dan parameter required this.text di construktor. Memungkinkan widget menerima dan menampilkan teks secara dinamis, memperbaiki error pada langkah 4, dan mendukung penggunaan teks di AutoSizeText.

- Pada langkah 6 terdapat dua widget yang ditambahkan, jelaskan fungsi dan perbedaannya!

  Container dengan RedTextWidget:
  Fungsi: Menampilkan teks dengan AutoSizeText, menyesuaikan ukuran font otomatis dalam Container berwarna kuning, dengan style merah, max 2 baris. Karakteristik: Fleksibel untuk ruang terbatas karena penyesuaian font.

  Container dengan Text:
  Fungsi: Menampilkan teks dengan widget Text bawaan dalam Container berwarna hijau, tanpa penyesuaian font otomatis. Karakteristik: Gaya default, cocok untuk ruang lebih besar.

  Perbedaan: RedTextWidget menggunakan AutoSizeText untuk menyesuaikan font secara dinamis dan memiliki gaya khusus (merah), sedangkan Text menggunakan gaya default tanpa penyesuaian font.

- Jelaskan maksud dari tiap parameter yang ada di dalam plugin auto_size_text berdasarkan tautan pada dokumentasi ini !

  Berdasarkan dokumentasi di tautan https://pub.dev/documentation/auto_size_text/latest/, berikut penjelasanya:

  - key
  Deskripsi: Mengontrol bagaimana satu widget menggantikan widget lain dalam pohon widget. penjelasan: Digunakan untuk mengidentifikasi widget secara unik, memungkinkan Flutter menentukan apakah widget perlu diperbarui atau digantikan.

  - textkey
  Deskripsi: textKey Mengatur kunci untuk widget Text yang dihasilkan fungsi: Memungkinkan Flutter mengenali, melacak, dan mengontrol widget Text secara spesifik dalam widget, terutama saat rebuild, testing, atau manipulasi state

  - style
  Deskripsi: Jika tidak null, gaya teks akan digunakan untuk widget ini. Penjelasan: Menentukan properti teks seperti warna, font, dll., meskipun ukuran font akan diatur ulang oleh auto-sizing.

 - minFontSize
  Deskripsi: Ukuran font minimum yang akan digunakan saat teks di-auto-sizing, diabaikan jika presetFontSizes diset. Penjelasan: Menetapkan batas bawah ukuran font agar teks tetap terbaca meskipun harus mengecil.

  - maxFontSize
  Deskripsi: Ukuran font maksimum yang akan digunakan saat teks di-auto-sizing. Penjelasan: Menentukan ukuran awal font sebelum penyesuaian, membatasi seberapa besar teks bisa ditampilkan.

  - stepGranularity
  Deskripsi: Langkah di mana ukuran font akan dikurangi saat mencari ukuran yang pas. Penjelasan: Mengatur seberapa halus atau kasar penyesuaian ukuran font (misalnya, 1.0 untuk penurunan 1 poin).

  - presetFontSizes
  Deskripsi: Menentukan semua ukuran font yang mungkin, dalam urutan menurun. Penjelasan: Memberikan daftar ukuran font spesifik yang akan dicoba secara berurutan untuk menemukan yang pas.

  - group
  Deskripsi: Menyinkronkan ukuran font dari beberapa widget AutoSizeText. Penjelasan: Memastikan semua widget dalam grup memiliki ukuran font yang sama untuk konsistensi tampilan.

  - textAlign
  Deskripsi: Menentukan bagaimana teks harus disejajarkan secara horizontal. Penjelasan: Mengatur posisi teks (kiri, tengah, kanan) di dalam ruang yang tersedia.

  - textDirection
  Deskripsi: Seperti TextAlign, start, dan TextAlign.end yang diinterpretasikan. Penjelasan: Menentukan arah teks (kiri-ke-kanan atau kanan-ke-kiri) berdasarkan konteks bahasa.

  - locale
  Deskripsi: Digunakan untuk memilih font saat karakter Unicode bisa dirender berbeda tergantung pada lokal. Penjelasan: Menyesuaikan rendering teks berdasarkan pengaturan bahasa atau wilayah.

  - softWrap
  Deskripsi: Menentukan apakah teks harus dipotong di akhir garis. Penjelasan: Mengontrol apakah teks dilanjutkan ke baris baru atau dipotong saat mencapai batas.

  - wrapWords
  Deskripsi: Menentukan apakah teks harus "benar-benar seperti" teks. Penjelasan: Memastikan kata tidak dipotong di tengah (jika true), atau memungkinkan pemotongan kata (jika false).

  - overflow
  Deskripsi: Menentukan bagaimana teks yang kelebihan harus ditangani. Penjelasan: Menentukan perilaku saat teks tidak muat, seperti menambahkan ellipsis ("...") atau memotongnya.

  - overflowReplacement
  Deskripsi: Widget yang ditampilkan jika teks kelebihan dan tidak muat dalam batas. Penejelasan: Menggantikan teks dengan widget lain (misalnya ikon) jika auto-sizing gagal.

  - textScaleFactor
  Deskripsi: Mengubah ukuran font untuk semua ukuran minFontSize, maxFontSize, dan presetFontSizes. Penjelasan: Menyesuaikan skala teks secara keseluruhan berdasarkan pengaturan perangkat.

  - maxLines
  Deskripsi: Jumlah maksimum baris teks yang dapat ditampilkan. Penjelasan: Membatasi jumlah baris teks yang akan ditampilkan sebelum overflow diterapkan.

  - semanticsLabel
  Deskripsi: Label alternatif untuk semantik teks. Penjelasan: Memberikan deskripsi teks untuk aksesibilitas, berbeda dari teks yang ditampilkan.
