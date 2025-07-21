# Panduan Impor Konten WordPress dari File .XML

Dokumen ini menjelaskan langkah-langkah untuk mengimpor konten ke situs WordPress menggunakan file ekspor berformat `.xml`. File ini umumnya berisi Postingan, Halaman, Komentar, Kategori, Tag, dan data Media dari situs WordPress lain.

## Daftar Isi
- [Prasyarat](#prasyarat)
- [Langkah-langkah Impor](#langkah-langkah-impor)
- [Pemecahan Masalah (Troubleshooting)](#pemecahan-masalah-troubleshooting)
- [Catatan Tambahan](#catatan-tambahan)

---

## Prasyarat

Sebelum memulai, pastikan Anda sudah menyiapkan:
* **Akses Administrator** ke dashboard WordPress tujuan.
* **File `.xml`** yang sudah diekspor dari situs WordPress sumber. Jika file Anda dalam format `.zip`, ekstrak terlebih dahulu untuk mendapatkan file `.xml`-nya.

---

## Langkah-langkah Impor

Proses impor dilakukan sepenuhnya melalui dashboard WordPress. Ikuti langkah-langkah berikut:

1.  **Login ke Dashboard WordPress**
    * Masuk ke area admin situs Anda (contoh: `https://situsanda.com/wp-admin`).

2.  **Buka Fitur Impor**
    * Dari menu navigasi di sebelah kiri, arahkan kursor ke **Peralatan** (atau **Tools**), lalu klik **Impor** (atau **Import**).

3.  **Instal WordPress Importer**
    * Di halaman Impor, cari opsi **WordPress** di bagian bawah daftar.
    * Klik **Pasang Sekarang** (atau **Install Now**). Proses instalasi ini cepat dan hanya perlu dilakukan sekali.

4.  **Jalankan Pengimpor (Run Importer)**
    * Setelah instalasi selesai, tautan akan berubah menjadi **Jalankan Pengimpor** (atau **Run Importer**). Klik tautan tersebut.

5.  **Unggah File XML Anda**
    * Anda akan diarahkan ke halaman "Impor WordPress".
    * Klik tombol **Choose File** atau **Pilih Berkas**.
    * Pilih file `.xml` yang sudah Anda siapkan dari komputer Anda.
    * Klik tombol **Unggah berkas dan impor** (atau **Upload file and import**).

6.  **Atur Penulis dan Lampiran**
    * Setelah file berhasil diunggah, Anda akan masuk ke halaman "Tetapkan Penulis" (Assign Authors).
    * **Tetapkan Penulis (Assign Authors):** Anda dapat menetapkan konten dari pengguna lama ke pengguna yang sudah ada di situs baru, atau membuat pengguna baru secara otomatis.
    * **Impor Lampiran (Import Attachments):** **PENTING!** Beri tanda centang pada opsi **"Unduh dan impor lampiran file"** (atau **"Download and import file attachments"**). Ini akan memastikan semua gambar dan media dari konten Anda ikut terimpor.

7.  **Selesaikan Proses**
    * Klik tombol **Kirim** (atau **Submit**).
    * Proses impor akan berjalan. Lamanya proses tergantung pada ukuran file `.xml` dan jumlah lampiran media. Setelah selesai, Anda akan melihat pesan konfirmasi.

---

## Pemecahan Masalah (Troubleshooting)

Berikut adalah beberapa masalah umum yang mungkin terjadi dan cara mengatasinya:

* **Gagal Impor karena Ukuran File Terlalu Besar**
    * **Masalah:** File `.xml` Anda lebih besar dari batas unggah maksimum server (misalnya 2MB, 8MB).
    * **Solusi:** Hubungi penyedia hosting Anda dan minta untuk menaikkan nilai `upload_max_filesize`, `post_max_size`, dan `memory_limit` pada konfigurasi PHP server Anda.

* **Proses Impor Berhenti di Tengah Jalan (Timeout)**
    * **Masalah:** Untuk file yang sangat besar, skrip impor bisa berhenti karena melampaui batas waktu eksekusi (`max_execution_time`).
    * **Solusi:** Minta penyedia hosting Anda untuk menaikkan batas `max_execution_time`.

* **Gambar atau Media Gagal Diimpor**
    * **Masalah:** Konten teks berhasil diimpor, tetapi gambar tidak muncul.
    * **Solusi:**
        1.  Pastikan Anda mencentang opsi "Unduh dan impor lampiran file" pada langkah 6.
        2.  Pastikan situs sumber (situs lama) masih dapat diakses secara publik agar situs baru bisa mengunduh gambar.
        3.  Periksa izin folder `wp-content/uploads` di hosting Anda. Seharusnya diatur ke `755`.

---

## Catatan Tambahan

* Proses impor ini **tidak** memindahkan tema, plugin, atau pengaturan widget. Anda perlu menginstal dan mengonfigurasi tema serta plugin secara manual di situs baru.
* Metode ini adalah cara standar WordPress untuk memindahkan konten. Untuk migrasi situs secara keseluruhan (termasuk tema, plugin, dan pengaturan), disarankan menggunakan plugin migrasi khusus seperti **All-in-One WP Migration** atau **Duplicator**.
