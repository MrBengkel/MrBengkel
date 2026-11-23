# Mr. Bengkel CitraRaya

Website pelanggan untuk layanan servis sepeda motor, sepeda listrik, dan sparepart. HTML, CSS, JavaScript, dan Bootstrap 5 lokal. Dapat dibuka langsung atau diterbitkan melalui GitHub Pages.

## Mulai

1. Ekstrak ZIP.
2. Buka folder `mr-bengkel-resmi`.
3. Klik dua kali `index.html` untuk melihat website.
4. Internet dibutuhkan untuk Google Maps dan tautan layanan eksternal.

## Publikasi ke GitHub Pages

1. Masuk ke akun GitHub milik usaha. Buat repository **Public** bernama `mr-bengkel`.
2. Pilih **Add file > Upload files**. Seret seluruh ISI folder `mr-bengkel-resmi` ke area unggah. Pertahankan folder `css`, `js`, `images`, dan `vendor` beserta isinya.
3. Pastikan `index.html` terlihat di tingkat paling atas repository, sejajar dengan folder tersebut. Unggah file hasil ekstraksi, bukan ZIP.
4. Klik **Commit changes**.
5. Buka **Settings > Pages**. Di **Build and deployment**, pilih **Deploy from a branch**. Pilih branch `main`, folder `/(root)`, lalu **Save**.
6. Buka **Actions** dan tunggu proses publikasi selesai. Kembali ke **Settings > Pages** lalu buka alamat website yang ditampilkan.
7. Alamat mengikuti pola `https://NAMA-AKUN.github.io/mr-bengkel/`. Gunakan alamat yang benar-benar ditampilkan GitHub.
8. Buka dari HP dan laptop. Coba navigasi, galeri, ulasan panjang, formulir, WhatsApp, dan petunjuk arah.

File `.nojekyll` disertakan. Jika tersembunyi saat unggah melalui Windows, file tersebut dapat dibuat lewat **Add file > Create new file** dengan nama `.nojekyll`.

Panduan resmi GitHub
https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Isi paket

| File / folder | Fungsi |
| --- | --- |
| `index.html` | Halaman utama, data usaha, layanan, ulasan, FAQ, formulir dan peta |
| `privasi.html` | Informasi penggunaan data formulir dan layanan eksternal |
| `css/style.css` | Warna, tata letak dan tampilan responsif |
| `css/beranda.css` | Tampilan beranda sesuai referensi pemilik, dengan latar abu-abu muda, biru dan oranye |
| `js/script.js` | Menu HP, pesan WhatsApp, galeri, ulasan dan tahun footer |
| `images/` | Logo dan foto asli Mr. Bengkel |
| `vendor/` | Bootstrap lokal beserta lisensi |
| `.nojekyll` | Penanda website statis bagi GitHub Pages |
| `PANDUAN_GITHUB.html` | Panduan visual yang dapat dibuka di browser |

## Cara memperbarui isi

- Ubah teks usaha dan layanan di `index.html`. Cari judul bagian yang ingin diperbarui.
- Ubah jam operasional di bagian atas, hero, FAQ, kontak, dan data terstruktur JSON-LD pada `<head>` agar konsisten.
- Untuk nomor WhatsApp baru, cari dan ganti `628119057800` pada seluruh HTML dan `js/script.js`, lalu perbarui nomor yang tampil.
- Ganti foto dengan nama file yang sama atau ubah `src` pada HTML. Huruf besar/kecil nama file harus sama persis. Isi `alt` sesuai foto dan sesuaikan atribut `width` serta `height` bila ukuran gambar berubah.
- Warna utama tersedia pada variabel CSS `--navy`, `--blue`, `--orange`.
- Enam testimoni bersumber dari tangkapan layar ulasan yang diberikan pemilik. Ulasan tersimpan sebagai konten statis, sehingga pembaruannya dilakukan secara manual.
- Gambar memakai alamat relatif agar dapat digunakan pada repository GitHub Pages dengan nama apa pun.

## Setelah alamat final ditentukan

Untuk metadata berbagi yang lebih lengkap, tambahkan pada `<head>` di `index.html` menggunakan URL HTTPS final yang ditampilkan GitHub (termasuk nama repository bila ada).

```html
<link rel="canonical" href="https://NAMA-AKUN.github.io/mr-bengkel/">
<meta property="og:url" content="https://NAMA-AKUN.github.io/mr-bengkel/">
<meta property="og:image" content="https://NAMA-AKUN.github.io/mr-bengkel/images/depan.jpg">
```

Ganti `NAMA-AKUN` dengan akun sebenarnya sebelum memakai potongan di atas. Metadata judul, deskripsi, bahasa dan data terstruktur usaha sudah disertakan. Domain khusus dapat diatur setelah domain dibeli dan alamat DNS tersedia.

## Alur konsultasi

Pelanggan mengisi nama, kendaraan, pilihan layanan, dan keluhan. Tombol **Siapkan Pesan WhatsApp** memvalidasi isian lalu menampilkan tombol untuk membuka pesan. Pelanggan tetap menekan Kirim di WhatsApp. Admin mengonfirmasi jadwal, kebutuhan pekerjaan, harga dan ketersediaan. Isian form tidak disimpan di server website.

## Pemeriksaan saat paket disiapkan

- Referensi gambar, CSS, JavaScript dan tautan bagian halaman diperiksa.
- Sintaks JavaScript diperiksa.
- Formulir diuji menghasilkan tautan WhatsApp dengan isian terkodekan. Perubahan isian menyembunyikan tautan lama.
- Galeri dibuka/ditutup dan ulasan panjang dibuka di browser.
- Tampilan desktop dan lebar ponsel 390 px diperiksa di browser. Menu HP membuka dan menutup, serta halaman tidak melebar secara horizontal pada pengujian tersebut.
- Publikasi repository GitHub dan pengiriman pesan WhatsApp perlu dilakukan pemilik.

## Jika tampilan kurang lengkap setelah unggah

Pastikan `vendor/bootstrap.min.css`, `css/style.css`, `js/script.js`, dan `images/` ikut diunggah. Nama folder harus huruf kecil sesuai sumber. Pastikan tidak ada folder tambahan yang membungkus `index.html`. Tunggu deployment terbaru selesai lalu muat ulang dengan Ctrl+F5.

## Aset

Foto, logo, profil usaha dan ulasan berasal dari materi pemilik yang disediakan. Bootstrap mengikuti lisensi pada `vendor/LICENSE-bootstrap.txt`.
