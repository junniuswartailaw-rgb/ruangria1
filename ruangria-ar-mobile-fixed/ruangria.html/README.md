# RuangRia: versi HTML5

## Langsung buka

Ekstrak seluruh folder, lalu buka `index.html` di browser modern. File `style.css` dan `script.js` adalah hasil build yang sudah menyertakan kode aplikasi, React, Three.js, font, dan ilustrasi. Tidak perlu memasang Node.js atau internet untuk menggunakan materi, jaring-jaring, dan kuis. Sumber yang dapat dikembangkan tersedia di folder `src/` proyek utama.

## Mengganti backsound

Cara paling mudah: tekan **Ganti musik** (ikon pengaturan di bagian atas), pilih file MP3, WAV, atau OGG maksimal 20 MB, dan atur volumenya. Lagu berulang dan disimpan di browser perangkat bila penyimpanan tersedia. Tombol **Gunakan musik bawaan** menghapus pilihan lagu lokal. Musik tidak diunggah ke server. Browser hanya mengizinkan suara setelah pengguna berinteraksi.

Untuk mengganti lagu bawaan bagi semua pengguna, simpan lagu di `assets/sounds/backsound.mp3`, lalu buka `music-config.js` dan ubah `defaultSrc` menjadi `./assets/sounds/backsound.mp3`. Anda juga dapat mengganti nama, format, dan volume di file tersebut. Jika sebelumnya sudah memilih lagu lewat aplikasi, tekan **Gunakan musik bawaan** agar konfigurasi baru dipakai. Pakai lagu yang Anda berhak gunakan.

## Localhost, AR, dan PWA

Kamera/AR serta instalasi PWA membutuhkan HTTPS atau localhost, bukan sekadar `file://`. Mode AR asli menggunakan WebXR `immersive-ar` dan pelacakan permukaan jika didukung perangkat. Jika WebXR tidak tersedia (misalnya pada sebagian browser iPhone/iPad), RuangRia mencoba membuka mode kamera alternatif: kamera belakang tampil dengan model 3D yang dapat diputar menggunakan sentuhan. Mode alternatif ini **bukan pelacakan permukaan dunia nyata** dan model tidak otomatis menempel pada lantai/meja.

Untuk localhost dengan Python, jalankan perintah berikut di dalam folder ini:

```sh
python -m http.server 8000
```

Buka `http://localhost:8000`. Mode kamera alternatif dan AR memerlukan izin kamera. Gunakan browser terbaru dan HTTPS/localhost. Perangkat yang mendukung WebXR dapat menggunakan AR dengan pelacakan permukaan; perangkat lain dapat menggunakan mode kamera alternatif atau model 3D. Hasilnya tetap bergantung pada browser, kamera, dan dukungan grafis perangkat. Kunjungi aplikasi sekali saat online untuk mengaktifkan cache offline. Penyimpanan lokal dapat berbeda antara `file://` dan localhost, atau dibatasi di beberapa browser.