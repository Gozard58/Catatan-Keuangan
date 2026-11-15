BUKU KAS - PANDUAN PASANG DI HP
================================

Isi folder:
  index.html            aplikasi
  manifest.webmanifest  data aplikasi (nama, ikon, warna)
  sw.js                 service worker (mode offline)
  icons/                ikon aplikasi

1) PASANG DI SERVER (wajib HTTPS)
   Cara paling mudah, gratis, tanpa coding:
   - Netlify Drop: buka app.netlify.com/drop, lalu seret folder ini ke halaman itu.
   - Cloudflare Pages atau GitHub Pages: unggah semua file di folder ini ke root.
   Anda akan mendapat alamat seperti https://nama-anda.netlify.app

2) PASANG DI HP
   Android (Chrome): buka alamatnya, ketuk "Pasang aplikasi" di aplikasi
                     (atau menu titik tiga, lalu "Instal aplikasi").
   iPhone (Safari):  buka alamatnya, ketuk tombol Bagikan, lalu
                     "Tambah ke Layar Utama".
   Ikon Buku Kas akan muncul di layar utama dan terbuka tanpa bilah browser.

3) CATATAN
   - Data disimpan di localStorage perangkat itu saja. Ponsel dan laptop tidak
     saling sinkron. Gunakan Ekspor CSV sebagai cadangan.
   - Menghapus data situs atau mencopot aplikasi dapat menghapus catatan.
   - iPhone bisa membersihkan data situs yang lama tidak dibuka (sekitar 7 hari)
     bila aplikasi TIDAK dipasang ke Layar Utama. Setelah dipasang, data lebih aman.
   - Setelah mengubah index.html, ubah VERSION di sw.js (misalnya "v2")
     agar HP mengambil versi baru.
   - Mencoba di komputer: jalankan "python3 -m http.server 8000" di folder ini,
     lalu buka http://localhost:8000
