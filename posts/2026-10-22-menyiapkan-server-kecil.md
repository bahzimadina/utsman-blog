---
title: "Bagian 3: Menyiapkan Tempat Menjalankan Agen (Server Kecil)"
date: 2026-10-22
slug: menyiapkan-server-kecil
lang: id
pair: tempat-ngajalankeun-agen
excerpt: "Agen yang hanya hidup saat laptop menyala tidak akan banyak menolong. Ini soal tempat tinggalnya: seberapa kecil server yang cukup, dan bagaimana membuatnya jarang mati."
tags: [tutorial, server, agen-ai]
draft: false
series: setup-ai-agent
series_title: Menyiapkan Asisten AI Sendiri, Langkah demi Langkah
part: 3
---

Di bagian pertama kita sudah memetakan lima bagian penyusun asisten, dan di bagian kedua memilih mesin berpikirnya. Sekarang langkah yang paling sering ditunda: tempat tinggalnya.

Alesannya sederhana. Agen yang hanya hidup saat laptop terbuka tidak akan bisa diandalkan untuk pekerjaan yang paling berguna — menjawab pesan jam lima pagi, menyiapkan catatan sebelum rapat, atau mengirim pengingat jadwal kegiatan saat Anda sedang di jalan.

## Harus menyala terus

Asisten bekerja karena dia menunggu. Ada pesan masuk, dia harus ada di sana untuk membacanya. Ada pekerjaan yang dijadwalkan subuh, mesinnya harus hidup pada jam itu. Jadi yang sedang dicari bukan komputer cepat, tapi komputer yang jarang mati.

## Tidak perlu komputer mahal

Model bahasa berjalan di tempat lain, disewa dari penyedia, jadi server Anda kebanyakan bertugas sebagai kurir: menerima pesan, menyiapkan bahan, memanggil model, lalu mengirim jawabannya. Untuk pekerjaan itu, dua inti prosesor dan memori dua gigabyte sudah cukup. Kartu grafis tidak masuk hitungan.

Pilihannya biasa saja: laptop lama yang sudah tidak dipakai, komputer kecil di rumah, komputer papan tunggal, atau server sewaan bulanan dengan spesifikasi paling kecil. Yang terakhir paling sedikit repotnya — tidak ada kabel, tidak takut mati lampu, bisa diakses dari mana saja. Kekurangannya: Anda menyewa, bukan memiliki, dan tetap harus diawasi.

## Mulai lebih kecil dari dugaan

Ambil paket paling murah dulu untuk sebulan dua bulan. Kalau ternyata cukup, nanti bisa ditambah. Banyak orang membeli berlebihan di awal karena membayangkan beban kerja yang belum tentu datang.

Yang lebih penting daripada ukuran: memakai Linux, karena hampir semua panduan menganggap itu; masuk memakai kunci SSH dan bukan kata sandi yang diketik; serta membiarkan sistem memasang pembaruan keamanannya secara rutin.

## Supaya hidup sendiri

Program yang dijalankan manual akan mati begitu sesi terminal ditutup, atau begitu mesinnya dinyalakan ulang. Obatnya satu hal kecil: daftarkan agen sebagai layanan sistem, supaya dia menyala lagi bersama server dan dijalankan ulang kalau berhenti.

Tambahkan juga pemeriksa sederhana — satu pesan uji tiap pagi, atau pemberitahuan kalau tidak ada kabar sehari. Asisten yang diam biasanya bukan sedang sibuk, tapi sudah mati sejak kemarin.

## Dua hal yang sering terlewat

Pertama, cadangan. Simpan catatan, aturan, dan daftar tugas di tempat yang bisa dipulihkan. Server kecil bisa rusak, dan yang bikin repot bukan mesinnya, tapi kebiasaan yang hilang bersamanya.

Kedua, biaya bulanan yang kecil-kecil: sewa server, listrik kalau ditaruh di rumah, dan pemakaian model. Jumlahnya tidak besar, tapi lebih enak kalau dicatat sejak awal supaya tidak kaget di kemudian hari.

Server kecil bukan soal perangkat yang terlihat mewah, tapi soal janji bahwa asisten selalu ada saat dipanggil.

Di bagian berikutnya: menyambungkan alat kerja — supaya agen bisa membaca berkas, mencari di internet, dan mengirim pesan.
