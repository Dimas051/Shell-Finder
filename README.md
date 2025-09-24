![alt text](https://h.top4top.io/p_3554w1z8i1.png?raw=true)
Mass Shell Finder adalah sebuah alat berbasis Python yang digunakan untuk mendeteksi keberadaan shell/backdoor yang tersembunyi di situs web, dengan cara melakukan pemeriksaan massal (massive scanning) terhadap daftar URL yang diberikan.

🎯 Tujuan Utama:

Untuk mencari dan mengidentifikasi URL yang mengarah ke web shell atau script berbahaya di server target, seperti:

c99.php, r57.php, b374k.php, wso.php
atau uploader shell yang memberikan kontrol penuh terhadap sistem.

🛠️ Cara Kerja Singkat:

1. Pengguna memasukkan file (contoh: urls.txt) yang berisi daftar URL target.
2. Tool ini akan melakukan permintaan HTTP (GET request) ke setiap URL.
3. Isi halaman diperiksa, apakah mengandung indikasi shell, seperti:
file → sering muncul di file manager shell.
uname -a → digunakan untuk melihat informasi sistem.
system( → fungsi PHP untuk mengeksekusi perintah OS.

Jika ditemukan, URL dianggap mengandung shell dan disimpan ke dalam file output (LifeTimeWorkingShells.txt dan Found.txt).

⚙️ Fitur-Fitur Utama:

✅ Multithreading    : Menggunakan ThreadPool (default 10 thread) untuk mempercepat scanning.

🎨 Output Berwarna   : Menggunakan modul colorama untuk membuat tampilan lebih jelas dan menarik.

🧠 Auto Save Result  : URL yang terdeteksi otomatis disimpan ke file log.

💡 Error Handling    : Menangani error seperti 404, timeout, URL salah, dsb.

🚀 Mudah Digunakan   : Antarmuka berbasis terminal yang langsung meminta input dan mulai scanning.

📥 Input:

File teks (misal: urls.txt) yang berisi daftar URL target, satu URL per baris.

📤 Output:

Found.txt → Daftar URL yang terdeteksi mengandung shell.

LifeTimeWorkingShells.txt → File log shell aktif (redundan untuk keperluan backup/dokumentasi).

📚 Contoh Kasus Penggunaan (Use Case):

Admin website  : Mengecek apakah ada shell tertinggal setelah website kena deface.
Bug hunter / security researcher  : Melakukan audit terhadap daftar situs target yang rawan shell upload.
Penetration tester  : Melacak shell yang tertinggal setelah exploit tertentu.
