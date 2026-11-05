# Tracking Build — Praktikum AVR Pertemuan 4

Implementasi awal image tracking dan face tracking menggunakan MindAR 1.2.5 dan Three.js 0.160.0.

## Status berkas

Kode halaman dan demo sudah disiapkan. Modul JSON yang diberikan tidak menyertakan pustaka `vendor/`, target terkompilasi `targets/target-card.mind`, gambar `assets/images/target-card.png`, atau berkas dokumentasi acuan. Salin berkas tersebut dari `tracking-build.zip` yang disebut modul sebelum menjalankan demo. Struktur yang diperlukan:

```text
tracking-build/
  assets/images/target-card.png
  targets/target-card.mind
  vendor/three/three.module.js
  vendor/three/addons/...
  vendor/mindar/mindar-image-three.prod.js
  vendor/mindar/mindar-face-three.prod.js
  index.html
  image-tracking.html
  face-tracking.html
  src/
```

## Menjalankan

Di folder ini jalankan `python -m http.server 8080`, lalu buka `http://localhost:8080`. Tekan Mulai dan izinkan kamera. Face tracking memerlukan internet untuk mengunduh model dari CDN. Untuk uji HP gunakan deployment HTTPS seperti GitHub Pages.

## Uji dan bukti

Belum ada hasil uji aktual karena lingkungan/perangkat uji pengguna tidak tersedia di sini. Isi [docs/test-cases.md](docs/test-cases.md) dan [docs/device-matrix.md](docs/device-matrix.md) berdasarkan percobaan nyata; status awal di dokumen itu ditandai belum diuji. Tambahkan tangkapan layar/video pada `docs/evidence/`.

## Masalah dan investigasi

Keterbatasan yang diketahui saat menyiapkan proyek: aset runtime tidak ada di modul JSON. Investigasi: ekstrak ZIP solusi acuan yang disebut pada Bagian 4 modul, lalu pastikan berkas vendor, gambar target, dan `.mind` tersedia di lokasi di atas. Face tracking dan kecocokan posisi kacamata juga belum diverifikasi dengan kamera nyata.

Lengkapi nama/NIM, tautan GitHub Pages, hasil aktual, dan bukti sebelum pengumpulan. Jangan tandai pengujian sebagai berhasil tanpa menjalankannya.
