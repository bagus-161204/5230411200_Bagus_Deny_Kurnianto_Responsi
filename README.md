# 5230411200_Bagus_Deny_Kurnianto_ResponsiFitur Utama:
Deskripsi Aplikasi
a. Untuk Admin:
Manajemen Produk:

Tambahkan produk baru ke dalam database.
Perbarui informasi produk seperti nama, harga, dan stok.
Hapus produk dari database jika tidak diperlukan lagi.
Lihat daftar semua produk yang tersedia dalam bentuk tabel.
Histori Transaksi:

Lihat daftar semua transaksi yang terjadi, termasuk detail produk, jumlah, total harga, dan tanggal transaksi.
b. Untuk User:
Pembelian Produk:
Memilih produk yang tersedia berdasarkan daftar.
Memasukkan jumlah produk yang akan dibeli.
Sistem akan otomatis memvalidasi ketersediaan stok dan mencatat transaksi baru ke dalam database.
c. Login Sistem:
Aplikasi memiliki halaman login sederhana untuk membedakan peran pengguna:
Admin: Memiliki akses penuh untuk mengelola produk dan melihat transaksi(email:admin@example.com),(password:admin123).
User: Hanya memiliki akses untuk melakukan transaksi pembelian(email:user@example.com),(password:user123).

Cara Kerja:
Login:

Pengguna memasukkan email dan password.
Jika login berhasil, pengguna diarahkan ke halaman sesuai dengan perannya (Admin/User).
Manajemen Produk (Admin):

Admin dapat melihat daftar produk yang tersedia dalam bentuk tabel.
Admin dapat menambahkan, memperbarui, atau menghapus produk melalui form input.
Transaksi (User):

User memilih produk dari dropdown menu.
Memasukkan jumlah pembelian.
Sistem memeriksa ketersediaan stok, mengurangi stok jika valid, dan mencatat transaksi ke database.
Histori Transaksi:

Admin dapat melihat seluruh data transaksi, termasuk detail produk, jumlah pembelian, total harga, dan tanggal transaksi.

Struktur Tabel Database
nama databese:retail_db
CREATE TABLE `products` (
  `id_produk` int(11) NOT NULL,
  `nama_produk` varchar(255) DEFAULT NULL,
  `harga_produk` decimal(10,2) DEFAULT NULL,
  `stok` int(11) NOT NULL
)

CREATE TABLE `transactions` (
  `id_transaksi` int(11) NOT NULL,
  `id_produk` int(11) DEFAULT NULL,
  `jumlah_produk` int(11) DEFAULT NULL,
  `total_harga` decimal(10,2) DEFAULT NULL,
  `tanggal_transaksi` date DEFAULT NULL
)
