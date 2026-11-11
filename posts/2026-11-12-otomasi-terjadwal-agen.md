---
title: "Bagian 6: Otomasi Terjadwal — Tugas Rutin yang Jalan Tanpa Diingatkan"
date: 2026-11-12
slug: otomasi-terjadwal-agen
lang: id
pair: otomasi-terjadwal
excerpt: "Agen yang sudah tersambung ke data masih menunggu diperintah. Bagian ini memasang jamnya: tugas rutin yang berjalan sendiri tiap pagi, tiap Jumat, dan tiap akhir bulan."
tags: [tutorial, agen-ai, otomasi, produktivitas]
draft: false
series: setup-ai-agent
series_title: Menyiapkan Asisten AI Sendiri, Langkah demi Langkah
part: 6
---

Di bagian kelima agen sudah bisa membuka berkas, membaca kalender, dan mencari arsip. Semua itu berguna, tapi ada satu kelemahan yang tidak kelihatan: agen cuma bergerak kalau Anda lebih dulu menyapa. Anda lupa bertanya, tidak ada yang terjadi. Anda tenggelam tiga hari, tiga hari itu juga tidak ada rekap apa pun.

Bagian ini memasang jam di agen itu. Bukan kemampuan baru yang rumit — semua bahan yang dipakai sudah ada di bagian sebelumnya. Yang berubah cuma pemicunya: bukan lagi pesan dari Anda, tapi jadwal.

## Bedanya obrolan dan jadwal

Obrolan itu reaktif. Anda butuh sesuatu, Anda tanya, agen jawab, selesai. Enak dipakai, tapi seluruh daftar hal yang perlu dikerjakan tetap tinggal di kepala Anda. Begitu kepala itu penuh, ada yang terlewat.

Jadwal memindahkan sebagian daftar itu ke mesin. Anda menentukan sekali, mesin mengulanginya. Untuk urusan yang polanya sama tiap minggu, cara ini jauh lebih tahan banting daripada niat baik.

## Apa yang layak dijadwalkan

Ukurannya sederhana: tugas yang berulang, jawabannya pendek, dan tidak butuh keputusan besar. Kalau tiap kali muncul Anda harus berpikir panjang, itu belum layak diotomatiskan — masih lebih baik dikerjakan sendiri.

Tiga contoh yang biasanya langsung kepakai:

- Ringkasan pagi: agenda hari ini, kegiatan terdekat, dan hal kecil yang belum selesai.
- Pengingat menjelang acara, dikirim dua hari lebih awal supaya masih ada waktu memperbaiki persiapan.
- Rekap mingguan tiap Jumat sore: apa yang selesai, apa yang mandek, apa yang menunggu orang lain.

## Jadwal itu cuma lima kolom

Di balik nama keren "cron", isinya lima kolom: menit, jam, tanggal, bulan, hari dalam sepekan. `0 5 * * *` artinya jam lima pagi setiap hari. `30 19 * * 5` artinya Jumat jam setengah delapan malam. Tanda bintang berarti "semua".

Anda tidak perlu hafal. Yang perlu diingat cuma satu: jam yang Anda tulis itu jam mesin, bukan jam dinding kantor. Kalau mesinnya duduk di zona waktu lain, ringkasan pagi bisa datang tengah malam. Pasang zona waktu yang benar dulu, baru percaya jadwalnya.

## Tugas terjadwal itu lupa segalanya

Ini bagian yang paling sering bikin hasilnya mengecewakan. Setiap kali jadwal menyala, agen mulai dari nol. Dia tidak ingat percakapan kemarin, tidak ingat bahwa laporan yang sama sudah dikirim minggu lalu.

Jadi tulis brief-nya lengkap: konteksnya apa, bahannya di mana, keluarannya berbentuk apa, dan apa yang harus dikerjakan kalau bahannya tidak ada. Bayangkan menulis instruksi untuk orang yang baru masuk lima menit lalu. Kalimat seperti "lanjutkan yang kemarin" tidak ada artinya di sini.

## Lebih baik diam daripada berisik

Tugas terjadwal yang mengirim pesan tiap kali jalan akan diabaikan dalam sepekan. Notifikasi yang datang tanpa ada yang perlu dilakukan itu mengajari orang untuk berhenti membaca.

Pola yang lebih sehat: laporan hanya kalau ada yang perlu dilihat. Kalau semuanya normal, tidak ada pesan. Tapi diamnya harus bisa dibedakan dari rusak. Minta tugas itu tetap mencatat bahwa dirinya jalan, dan minta dia bersuara jelas kalau gagal — bukan menghilang karena error tidak tertangkap.

## Jalankan dulu dengan tangan

Sebelum menyerahkan sesuatu ke jadwal, panggil sekali secara manual dan periksa hasilnya. Dua atau tiga kali, di jam yang berbeda, dengan bahan yang berbeda. Kalau hasil manualnya sudah rapi, baru dipasang jadwalnya.

Untuk bulan pertama, batasi ke tugas yang membaca dan meringkas saja. Tugas yang mengirim ke banyak orang, mengubah data, atau menghapus sesuatu tunggu sampai Anda yakin betul polanya. Awas juga tumpang tindih: dua tugas yang menyala di menit yang sama bisa saling mengganggu.

Di titik ini agen sudah bergerak sendiri, tapi dia masih pelupa. Bagian ketujuh membahas ingatan: cara membuat agen mencatat apa yang sudah dikerjakan, supaya ringkasan besok tidak mengulang ringkasan hari ini.
