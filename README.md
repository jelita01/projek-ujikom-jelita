# projek-ujikom-jelita
1. Fungsi Login dalam Sistem
Memastikan Keamanan Data
Hanya pengguna yang memiliki akun yang bisa masuk dan mengakses tugas mereka.
Password disimpan dalam bentuk hash agar lebih aman.
Mengidentifikasi Pengguna
Setelah berhasil login, sistem akan menyimpan session dengan informasi pengguna.
Ini memungkinkan pengguna untuk mengakses data yang sesuai dengan akun mereka.
Mengontrol Akses ke Halaman Tertentu
Pengguna yang belum login tidak bisa langsung mengakses dashboard atau halaman lain.
Sistem akan mengarahkan mereka kembali ke halaman login.
Mendukung Multi-User
Jika ada banyak pengguna, masing-masing hanya bisa melihat dan mengelola tugas mereka sendiri.
Hal ini menghindari data satu pengguna diakses oleh pengguna lain tanpa izin.
2. dashboard.php (Halaman Dashboard)
Fitur:
Menampilkan Daftar Tugas: Kemungkinan besar halaman ini menampilkan daftar tugas yang telah dibuat oleh pengguna.
Navigasi ke Fitur Lain: Terdapat akses ke fitur pengeditan (edit_task.php) dan penghapusan (hapus_task.php).
Manajemen Sesi: Dashboard ini hanya bisa diakses jika pengguna sudah login.
3. edit_task.php (Halaman Edit Tugas)
Fitur:
Mengedit Tugas: Pengguna dapat memperbarui informasi tugas yang sudah ada.
Mengambil Data dari Database: Sistem akan mengambil data tugas yang dipilih dan menampilkan di form.
Menyimpan Perubahan ke Database: Setelah pengguna mengedit tugas, perubahan akan disimpan ke database.
Validasi Input: Ada kemungkinan sistem memeriksa apakah input yang diberikan sudah sesuai sebelum menyimpannya.
4. hapus_task.php (Halaman Hapus Tugas)
Fitur:
Menghapus Tugas dari Database: File ini kemungkinan menerima task_id dari dashboard.php untuk menghapus tugas.
Konfirmasi Penghapusan: Bisa jadi ada mekanisme konfirmasi sebelum tugas benar-benar dihapus.
Redirect ke Dashboard: Setelah tugas dihapus, pengguna akan diarahkan kembali ke dashboard.php.
5. register.php
Fungsi:
Digunakan sebagai halaman registrasi untuk pengguna baru.
Fitur:
Form pendaftaran dengan input username, email, dan password.
Hashing password sebelum disimpan ke database (password_hash()).
Memastikan tidak ada duplikasi username.
Menampilkan pesan sukses atau error setelah registrasi.
6. koneksi.php
Fungsi:
File konfigurasi koneksi database.
Fitur:
Berisi kode PHP untuk menghubungkan sistem ke database menggunakan mysqli_connect().
Digunakan di semua halaman yang memerlukan akses database.
7. logic.js
Fungsi:
Mengelola interaksi pengguna dan pengolahan data tugas dengan JavaScript.
Fitur:
Menangani event ketika pengguna mengisi dan mengirim form tambah tugas.
Mengirim data tugas ke add_task.php menggunakan fetch API.
Melakukan validasi input sebelum dikirim.
Menampilkan notifikasi jika tugas berhasil atau gagal ditambahkan.
Me-refresh halaman setelah tugas berhasil ditambahkan
8. selesaikan_task.php
Fungsi:
Menandai tugas sebagai selesai.
Fitur:
Mengubah status tugas di database dari "belum selesai" menjadi "selesai".
Memungkinkan pengguna melihat daftar tugas yang sudah diselesaikan.
9. logout.php
Fungsi:
Menghapus sesi pengguna dan mengembalikan mereka ke halaman login.
Fitur:
Menggunakan session_destroy() untuk menghapus semua sesi.
Redirect ke halaman login setelah logout.

Kesimpulan
Sistem ini adalah aplikasi manajemen tugas sederhana berbasis web yang memiliki fitur utama:
✅ Autentikasi pengguna (Login & Register).
✅ Manajemen tugas (Tambah, Edit, Hapus, Selesaikan).
✅ Interaksi real-time menggunakan JavaScript (logic.js).
✅ Keamanan dengan hashing password dan sesi.

