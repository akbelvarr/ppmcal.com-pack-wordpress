Panduan Impor Konten WordPress dari File XML
Dokumen ini menjelaskan cara mengimpor konten ke situs WordPress Anda menggunakan file ekspor berformat .xml. File ini biasanya berisi postingan, halaman, komentar, kategori, tag, dan media dari situs WordPress lain.

Daftar Isi
Prasyarat

Langkah-langkah Impor

Pemecahan Masalah (Troubleshooting)

Catatan Tambahan

Prasyarat
Sebelum memulai, pastikan Anda memiliki:

Akses Administrator ke dashboard WordPress tujuan.

File .xml yang sudah diekspor dari situs WordPress sumber. Jika file Anda dalam format .zip, ekstrak terlebih dahulu untuk mendapatkan file .xml-nya.

Langkah-langkah Impor
Proses impor dilakukan melalui dashboard WordPress. Berikut adalah langkah-langkahnya:

Login ke Dashboard WordPress Masuk ke situs WordPress baru Anda (contoh: namasitusanda.com/wp-admin).

Buka Fitur Impor Dari menu navigasi di sebelah kiri, arahkan kursor ke Peralatan (atau Tools), lalu klik Impor (atau Import).

Instal WordPress Importer Di halaman Impor, Anda akan melihat daftar berbagai platform. Cari WordPress dan klik Pasang Sekarang (atau Install Now). Proses instalasi ini hanya perlu dilakukan sekali.

Jalankan Importer Setelah instalasi selesai, tautan akan berubah menjadi Jalankan Pengimpor (atau Run Importer). Klik tautan tersebut untuk memulai.

Unggah File XML Anda Anda akan diarahkan ke halaman "Impor WordPress".

Klik tombol Choose File atau Pilih Berkas.

Pilih file .xml yang sudah Anda siapkan dari komputer Anda.

Klik tombol Unggah berkas dan impor (atau Upload file and import).

Atur Penulis dan Lampiran Setelah file berhasil diunggah, Anda akan melihat halaman "Tetapkan Penulis" (Assign Authors):

Tetapkan Penulis: Anda bisa menetapkan konten dari pengguna di situs lama ke pengguna yang ada di situs baru. Anda juga bisa membuat pengguna baru dengan nama yang sama.

Impor Lampiran: Beri tanda centang pada opsi Unduh dan impor lampiran file (atau Download and import file attachments). Ini sangat penting agar semua gambar dan media dari konten Anda ikut terimpor.

Selesaikan Proses Impor Klik tombol Kirim (atau Submit). Proses impor akan berjalan. Lamanya proses tergantung pada ukuran file .xml dan jumlah lampiran media. Setelah selesai, Anda akan melihat pesan konfirmasi.

Pemecahan Masalah (Troubleshooting)
Terkadang, proses impor dapat mengalami kendala. Berikut adalah beberapa masalah umum dan solusinya:

Gagal Impor karena Ukuran File Terlalu Besar Jika file .xml Anda lebih besar dari batas unggah maksimum server (misalnya, 2MB), proses impor akan gagal.

Solusi: Hubungi penyedia hosting Anda untuk meminta kenaikan batas upload_max_filesize, post_max_size, dan memory_limit pada konfigurasi PHP server Anda.

Proses Impor Memakan Waktu Terlalu Lama (Timeout) Untuk file yang sangat besar, skrip impor bisa berhenti karena melampaui batas waktu eksekusi (max_execution_time).

Solusi: Sama seperti masalah ukuran file, minta penyedia hosting Anda untuk menaikkan batas waktu eksekusi skrip PHP.

Gambar atau Media Tidak Muncul (Gagal Impor Lampiran) Ini bisa terjadi jika situs sumber tidak lagi aktif atau direktori uploads di situs baru tidak memiliki izin tulis (write permission).

Solusi:

Pastikan Anda mencentang opsi "Unduh dan impor lampiran file" pada langkah 6.

Pastikan situs sumber masih dapat diakses secara publik jika memungkinkan.

Periksa izin folder wp-content/uploads di hosting Anda. Seharusnya diatur ke 755.

Catatan Tambahan
Proses impor ini tidak memindahkan tema, plugin, atau pengaturan widget. Anda perlu menginstal tema dan plugin secara manual di situs baru.

Jika Anda memindahkan konten dari WordPress.com, prosesnya pada dasarnya sama. Anda hanya perlu mengekspor data dari akun WordPress.com Anda terlebih dahulu.

Untuk migrasi situs yang lengkap (termasuk tema, plugin, dan pengaturan), disarankan menggunakan plugin migrasi seperti Duplicator, All-in-One WP Migration, atau sejenisnya.
