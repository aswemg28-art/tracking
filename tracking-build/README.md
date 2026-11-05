# Tracking Build — Praktikum AVR Pertemuan 4

Proyek image tracking dan face tracking menggunakan MindAR 1.2.5 dan Three.js 0.160.0.

## Status berkas

Pustaka runtime resmi sudah disertakan di `vendor/`. Gambar target khusus sudah dibuat di `assets/images/target-card.svg` dan `assets/images/target-card.png`. **Berkas `targets/target-card.mind` masih perlu dibuat** dengan mengompilasi PNG tersebut melalui compiler resmi MindAR. Jangan pakai `.mind` dari gambar lain, karena tidak akan mengenali target-card proyek ini.

## Membuat berkas target `.mind`

1. Buka [MindAR Image Target Compiler](https://hiukim.github.io/mind-ar-js-doc/tools/compile/).
2. Muat `assets/images/target-card.png`.
3. Jalankan compile dan unduh hasilnya.
4. Simpan sebagai `targets/target-card.mind`.

## Menjalankan

Setelah `.mind` tersedia, jalankan `python -m http.server 8080` di folder ini dan buka `http://localhost:8080`. Tekan **Mulai** dan izinkan kamera. Face tracking memerlukan internet untuk mengunduh model dari CDN. Untuk uji HP, deploy ke HTTPS seperti Cloudflare Pages.

## Uji dan bukti

Belum ada hasil uji kamera aktual. Isi [docs/test-cases.md](docs/test-cases.md) dan [docs/device-matrix.md](docs/device-matrix.md) berdasarkan percobaan nyata. Simpan tangkapan layar/video di `docs/evidence/`.

## Keterbatasan dan investigasi

Target `.mind` harus dikompilasi khusus dari PNG proyek ini. Face tracking dan posisi kacamata belum diverifikasi melalui kamera nyata. Lengkapi nama/NIM, tautan deployment, hasil aktual, dan bukti sebelum pengumpulan. Jangan tandai pengujian berhasil tanpa menjalankannya.
