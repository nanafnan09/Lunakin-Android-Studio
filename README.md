# Lunakin

Nama : Afnan Dika Ramadhan

NIM : 312410518

Kelas : TI.24.A5

MataKuliah : Pemrograman Mobile

# StoryBoard

![Foto](https://github.com/nanafnan09/Lunakin-Android-Studio/blob/d9f1492df900f144102a7f502c149ab65f211db2/Pict%20Lunakin/Lunakin%20StoryBoard.png)

Berdasarkan rancangan antarmuka StoryBoard, berikut adalah alur kerja aplikasi:

### 1. Splash Screen & Lokasi
* **Splash 1:** Menampilkan logo aplikasi dengan animasi transisi pembuka.
* **Splash 2:** Fitur deteksi lokasi yang menampilkan bendera negara sesuai lokasi pengguna, logo, dan ucapan "Selamat Datang".

### 2. Halaman Utama (Dashboard)
Halaman awal yang sederhana dengan dua navigasi utama:
* **Tombol "Pesanan":** Untuk memulai pemesanan baru.
* **Tombol "List Pesanan":** Untuk melihat riwayat atau status pesanan yang sedang berjalan.

### 3. Pemilihan Menu (Menu List)
* Menampilkan daftar makanan yang tersedia.
* Informasi harga (Rp) untuk setiap item.
* Fitur input jumlah pesanan.
* Tombol "Order" untuk melanjutkan ke tahap pembayaran.

### 4. Pengisian Data & Pembayaran (Checkout)
Formulir untuk melengkapi detail pesanan:
* **Input Data:** Nama Pembeli dan Alamat Pengiriman.
* **Metode Pembayaran:** Dropdown untuk memilih opsi pembayaran (QRIS atau Cash).
* **Tombol Simpan:** Untuk memvalidasi data.

### 5. Ringkasan Pesanan (Order Summary)
Halaman konfirmasi yang memuat:
* Judul "List Pesanan".
* Rincian menu yang dipilih beserta total harga.
* Data pemesan (Nama, Alamat, Metode Pembayaran).
* **Tombol QR:** Memunculkan kode QR atau informasi transfer (seperti nomor Dana) jika memilih pembayaran non-tunai.
* **Tombol Selesai:** Menyelesaikan proses transaksi.

# WireFrame

![foto](https://github.com/nanafnan09/Lunakin-Android-Studio/blob/d9f1492df900f144102a7f502c149ab65f211db2/Pict%20Lunakin/Wireframe.png)

📱 Penjelasan Alur Wireframe (Digital)
### Splash Screen (Layar 1 & 2):

Fungsi: Tampilan pembuka aplikasi saat pertama kali dijalankan.

Detail: Menampilkan Logo di tengah layar. Pada layar kedua, terdapat teks "Selamat Datang" dan indikator lokasi (lingkaran di pojok kanan atas) untuk memberi konteks personalisasi wilayah.

### Dashboard Utama (Layar 3):

Fungsi: Pusat navigasi bagi pengguna.

Fitur: Hanya terdapat dua tombol utama agar antarmuka bersih (clean UI), yaitu tombol "PESANAN" untuk memulai order dan "LIST PESANAN" untuk cek status.

### Halaman Menu & Order (Layar 4):

Fungsi: Katalog digital tempat pengguna memilih makanan.

Fitur Detail:

List Menu Berharga: Menampilkan item spesifik (Ayam Goreng/Bakar 15k, Lele 10k, Tahu/Tempe 5k, dll).

Counter Quantity: Menggunakan tombol (- 0 +) untuk menambah atau mengurangi jumlah porsi dengan mudah.

Opsi Tambahan: Pilihan varian sambal (Sambal Penyet / Sambal biasa).

Footer Bar: Menampilkan total harga ("Rp:0") yang terupdate otomatis dan tombol "Order".

### Formulir Data Pembeli (Layar 5):

Fungsi: Pengumpulan data untuk pengiriman/identitas pesanan.

Input: Kolom "Nama Pembeli", "Alamat", dan Dropdown "Metode Pembayaran".

Aksi: Tombol "Simpan" untuk konfirmasi data sebelum masuk ke invoice.

### Invoice / Ringkasan Pesanan (Layar 6):

Fungsi: Bukti pemesanan digital (struk).

Detail Tampilan: Menampilkan kartu ringkasan berisi Nama (cth: Sahromy), Rincian Menu (cth: Ayam bakar x2), Total Harga, dan Metode Pembayaran.

Fitur: Tombol "QR" kecil untuk memunculkan kode bayar dan tombol status "Done" jika pesanan selesai.

### Informasi Pembayaran (Layar 7):

Fungsi: Instruksi khusus untuk pembayaran manual/e-wallet.

Konten: Menampilkan instruksi "Gunakan Nomer ini untuk Transfer Dana" beserta nomor tujuan yang jelas (089514483266), memudahkan pengguna yang tidak bisa scan QRIS.


# UI

![foto](https://github.com/nanafnan09/Lunakin-Android-Studio/blob/d9f1492df900f144102a7f502c149ab65f211db2/Pict%20Lunakin/UI.png)

Aplikasi ini dirancang dengan antarmuka *High-Fidelity* yang intuitif dan responsif. Berikut adalah penjelasan elemen visual dan fitur utamanya:

### 📍 Fitur Deteksi Lokasi Otomatis (Smart Localization)
Salah satu fitur unggulan pada *Splash Screen* adalah indikator bendera dinamis di pojok kanan atas.
* **Cara Kerja:** Sistem secara otomatis mendeteksi lokasi geografis pengguna berdasarkan IP Address atau GPS.
* **Logika Perubahan:**
    * Jika pengguna mengakses dari **Indonesia** 🇮🇩, ikon bendera Merah Putih akan muncul.
    * Jika pengguna mengakses dari **Amerika Serikat** 🇺🇸, ikon secara otomatis berubah menjadi bendera *Stars and Stripes*.
    * Fitur ini bertujuan untuk memberikan pengalaman pengguna (*User Experience*) yang lebih personal dan relevan sesuai wilayah operasional.

### 📱 Alur Pemesanan (Ordering Flow)
1.  **Dashboard:** Desain minimalis dengan fokus pada dua aksi utama: *Buat Pesanan* dan *Cek List Pesanan*.
2.  **Smart Menu:**
    * Menggunakan tombol *counter* (`+` / `-`) untuk input jumlah pesanan yang cepat.
    * Kalkulasi harga *real-time* yang langsung muncul di bagian bawah layar.
    * Opsi kustomisasi sambal menggunakan *toggle switch*.
3.  **Pembayaran Digital:**
    * Mendukung instruksi pembayaran manual (Transfer via Dana) dengan tampilan nomor tujuan yang jelas dan mudah dibaca.

### 🎨 Desain Visual (UI Style)
* **Tema Warna:** Menggunakan palet warna hangat (Krem & Kuning) identik dengan "Ayam Tulang Lunak", dipadukan dengan warna Hijau untuk tombol aksi (*Call to Action*) guna menarik perhatian mata pengguna.
* **Tipografi:** Menggunakan font *Sans-Serif* yang modern dan mudah dibaca pada layar ponsel.


# UX

### Link Youtube : (https://youtu.be/lDyoqxzHs-8?si=4naDa1XulNSM_UdW)

Klik link tersebut untuk melihat UX dari projek ini

# Tampilan Pada HP

# 1. Deteksi Lokasi & Lokalisasi Bahasa (Splash Screen)

<img src="Pict Lunakin/1.jpeg" width="240">  <img src="Pict Lunakin/lokasi.jpeg" width="240">

Ini adalah fitur unik yang Anda minta untuk ditekankan.

Fungsi: Aplikasi secara otomatis mendeteksi lokasi pengguna saat aplikasi dibuka.

Logika:

Jika lokasi terdeteksi di Indonesia, ikon bendera di pojok kanan atas menjadi Merah Putih dan teks sambutan menggunakan Bahasa Indonesia ("Selamat Datang").

Jika lokasi terdeteksi di Amerika Serikat (atau luar Indonesia), ikon bendera berubah menjadi bendera AS dan teks sambutan berubah menjadi Bahasa Inggris ("Welcome").

Istilah Teknis untuk Readme: Automatic Location-Based Localization atau Geo-location Language Support.

# 2. Halaman Menu Utama (Dashboard)

<img src="Pict Lunakin/2.jpeg" width="240">

Fungsi: Gerbang navigasi utama aplikasi.

Fitur: Terdapat dua tombol navigasi utama:

PESANAN: Untuk memulai pesanan baru.

LIST PESANAN: Untuk melihat riwayat atau detail pesanan yang sudah dibuat.

# 3. Pemilihan Menu Makanan (Ordering Interface)

<img src="Pict Lunakin/3.jpeg" width="240">

Fungsi: Halaman katalog di mana pengguna memilih item.

Fitur:

Daftar menu dengan harga.

Counter (+/-) untuk menambah jumlah porsi per item.

Toggle Switch untuk opsi tambahan (misal: Sambal Penyet, Sambal).

Kalkulasi total harga otomatis secara real-time di bagian bawah (Rp:29000).

# 4. Input Data Pemesan (Checkout Form)

<img src="Pict Lunakin/4.jpeg" width="240">

Fungsi: Pengguna memasukkan detail identitas untuk pengiriman.

Fitur:

Input Nama Pembeli.

Input Alamat Lengkap.

Dropdown pemilihan Metode Pembayaran (contoh di gambar: Dana).

Tombol "Simpan" untuk memproses data ke database/sistem.

# 5. Instruksi Pembayaran (Payment Gateway Simulation)

<img src="Pict Lunakin/5.jpeg" width="240">

Fungsi: Memberikan instruksi transfer sesuai metode yang dipilih.

Fitur:

Menampilkan UI dinamis berdasarkan metode pembayaran (contoh: Menampilkan nomor Virtual Account/Transfer untuk DANA).

# 6. Notifikasi Sistem

<img src="Pict Lunakin/notif.jpeg" width="240">

Fungsi: Memberikan umpan balik (feedback) kepada pengguna bahwa proses berhasil.

Fitur: Push Notification yang muncul di status bar berisi konfirmasi "Orderan Disimpan" beserta nama pemesan.

# 7. Ringkasan Pesanan (Order History/Summary)

<img src="Pict Lunakin/6.jpeg" width="240">

Fungsi: Menampilkan rekapitulasi data yang telah tersimpan.

Fitur:

Menampilkan detail lengkap: Nama, Alamat, Rincian Menu (Item & Qty), Total Harga, dan Metode Pembayaran.

Status pesanan (tombol "Done").



