---
title: "Progres Utsman Device: Layar Bundar Penuh, Koneksi Lokal, dan Kamera Watcher"
date: 2026-11-18
slug: utsman-device-progres-perangkat-fisik
lang: id
pair: utsman-device-progress
cover: /blog/images/utsman-device-watcher-2026-11.jpg
excerpt: Catatan perkembangan prototipe perangkat fisik Utsman berbasis SenseCAP Watcher, mulai dari tampilan layar bundar penuh hingga sinkronisasi kamera dan server lokal.
tags: [utsman-device, hardware, watcher, progres]
draft: false
---

Selama ini, Utsman lebih sering ditemui lewat layar ponsel di WhatsApp, Telegram, atau surel. Pekan ini kami mulai melangkah ke bentuk fisik: prototipe perangkat meja bernama **Utsman Device** yang dibangun di atas perangkat keras **Seeed Studio SenseCAP Watcher**.

Dalam wujud prototipe berwadah transparan ini, Utsman tidak lagi sekadar jendela obrolan. Di bagian depan terpasang layar sentuh bundar, dipadukan dengan kamera di sudut atas serta mikrofon dan speaker bawaan. Pada pengujian hari ini, antarmuka awal sudah berjalan: ikon status Wi-Fi dan baterai muncul di bagian atas layar, tulisan **"Mendengarkan..."** aktif di bawahnya, sementara avatar Utsman berpeci hitam duduk tepat di tengah lingkaran.

Fokus pengerjaan kali ini berada pada dua hal utama, yakni keandalan koneksi setelah proses pembaruan firmware dan penyempurnaan tampilan kamera pada layar bundar.

## Koneksi lokal lewat utsman.local dan MQTT

Agar respons suara dan pemrosesan gambar tetap cepat tanpa bergantung penuh pada jalur luar, perangkat dirancang terhubung langsung ke server lokal melalui alamat `utsman.local` dan protokol MQTT. Pengaturan awal jaringan juga sudah mendukung pemindaian **QR Wi-Fi**, sehingga proses pairing perangkat di meja kerja menjadi jauh lebih ringkas.

Sempat muncul kendala kecil sesudah proses flash firmware: perangkat tertahan sekitar dua menit sebelum kembali daring karena ikut ter-reset ketika port serial dibuka untuk pembacaan log. Setelah jalur sambungan di server diperiksa dan siklus reset dirapikan, Watcher kembali boot normal, terhubung ke Wi-Fi, menyambung ke broker MQTT, lalu menjalankan percakapan serta pengambilan gambar seperti semula.

## Pratinjau kamera penuh di layar bundar

Perubahan yang paling terasa di sisi antarmuka ada pada cara perangkat menampilkan hasil jepretan kamera di layar depan. Pada versi sebelumnya, gambar kamera berukuran 240x240 diperkecil menjadi kotak sekitar 200x200 di tengah layar, sehingga menyisakan bingkai kosong yang cukup lebar di sekelilingnya.

Pada patch firmware terbaru di `xiaoai-client.patch` dan `client.cpp`, pratinjau foto sekarang digambar memenuhi seluruh layar bundar berukuran 360x360 dengan perbandingan sisi yang tetap terjaga:

- Foto memenuhi seluruh lingkaran layar tanpa mengecil menjadi kotak di tengah, hanya menyisakan potongan tipis di tepi kiri-kanan agar proporsional.
- Status koneksi di bagian atas serta teks keterangan di bagian bawah tetap tampil terbaca di atas pratinjau gambar.
- Resolusi foto yang dikirim ke server tidak dikurangi sama sekali, tetap utuh di ukuran 480x480 agar analisis visual dari sisi server tetap tajam.

## Langkah uji berikutnya

Setelah tampilan kamera penuh dan jalur QR Wi-Fi berjalan baik pada perangkat keras, pekerjaan berlanjut ke pengujian menu sentuh serta alur ambil foto langsung dari Watcher, sebelum seluruh perubahan firmware dikunci dan di-commit ke repositori utama.

Target jangka pendeknya sederhana: perangkat meja yang cukup dicolokkan ke listrik, tersambung ke jaringan lokal, lalu siap diajak bicara atau dimintai tolong membaca dokumen maupun kondisi sekitar secara langsung.
