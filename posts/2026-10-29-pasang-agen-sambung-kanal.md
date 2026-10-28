---
title: "Bagian 4: Memasang Agen dan Menyambungkannya ke Kanal"
date: 2026-10-29
slug: pasang-agen-sambung-kanal
lang: id
pair: pasang-agen-sambung-kanal
excerpt: "Agen yang menyala di server belum bisa diajak bicara siapa pun. Bagian ini soal memasangnya, membuat bot Telegram, menyiapkan nomor WhatsApp, dan menjaga pintu masuknya tetap rapi."
tags: [tutorial, agen-ai, telegram, whatsapp]
draft: false
series: setup-ai-agent
series_title: Menyiapkan Asisten AI Sendiri, Langkah demi Langkah
part: 4
---

Di bagian ketiga kita sudah menyiapkan rumahnya: server kecil yang menyala terus, agen terdaftar sebagai layanan, dan pemeriksa harian supaya ketahuan kalau dia mati. Tapi agen yang hidup tanpa nomor itu seperti ruangan bersih yang tak punya pintu. Rapi, siap dipakai, dan tak ada seorang pun bisa mengetuk.

Kanal adalah pintunya. Bukan aplikasi baru yang harus diunduh orang lain, melainkan tempat orang sudah biasa mengobrol tiap hari. Dua nama cukup: Telegram dan WhatsApp.

## Pasang dulu, sambung kemudian

Urutannya sering dibalik orang. Pasang dulu agennya sampai dia bisa menjawab di terminal, baru sambungkan kanal. Kalau dikerjakan bersamaan dan ada yang gagal, Anda tidak tahu mana yang salah.

Pasang di server yang disiapkan minggu lalu, jalankan sebagai layanan, dan taruh semua pengaturan di satu berkas konfigurasi. Berkas yang memuat nilai rahasia diberi izin baca hanya untuk pemiliknya, dan jangan ditaruh di folder yang ikut terunggah ke repositori publik.

Yang perlu diingat: satu proses agen bisa melayani beberapa kanal sekaligus. Jangan bikin satu agen per kanal hanya karena terasa lebih rapi di awal — nanti aturannya dobel dan Anda yang pusing menyamakan.

## Telegram: paling cepat jadi

Bot Telegram dibuat lewat satu akun resmi di dalam aplikasi, ikuti percakapan singkatnya, dan Anda dapat kunci bot. Simpan kunci itu di berkas konfigurasi, jangan di dalam kode, jangan pula ditempel di grup obrolan pengurus untuk minta tolong diperiksa.

Dua hal kecil yang sering dilupakan setelah bot hidup. Pertama, daftar siapa yang boleh memerintah — username atau nomor pengguna yang Anda percaya, bukan semua orang yang menemukan bot itu. Kedua, uji dengan pesan sungguhan: sapa, tanya hal yang jawabannya Anda sudah tahu, lalu kirim perintah yang salah untuk memastikan dia menjawab sopan dan tidak diam membeku.

## WhatsApp: dekat ke warga, tapi lebih ribet

WhatsApp terasa lebih akrab karena di situ jemaah memang sudah berkirim pesan. Konsekuensinya lebih berat: aturan platformnya ketat dan nomor pribadi sebaiknya tidak dipakai. Siapkan nomor terpisah untuk agen.

Ada dua jalur. Lewat penyedia resmi, lebih stabil dan rapi, tetapi pendaftarannya berbelit dan biasanya berbayar. Lewat jembatan tidak resmi, lebih cepat dicoba, tetapi bisa kena pembatasan sewaktu-waktu. Untuk uji coba sendiri, jalur kedua masuk akal. Untuk melayani orang banyak, jalur pertama lebih aman.

Soal grup: jangan biarkan agen menjawab setiap pesan di grup jemaah. Cukup menanggapi kalau namanya disebut atau ada yang membalas pesannya. Grup ramai bisa berubah jadi dua robot yang saling menyahut.

## Satu agen, banyak pintu

Agen dengan dua kanal butuh satu kebiasaan: semua pesan masuk, dari mana pun asalnya, ditaruh di antrean yang sama. Agen mengolahnya satu per satu, lalu membalas ke kanal asal pesan itu. Kalau tidak, jawaban untuk WhatsApp bisa nyasar ke Telegram.

Simpan juga catatan percakapan: siapa pengirimnya, dari kanal mana, apa yang tadi dibahas. Tanpa itu, tiap pesan baru terasa seperti bicara dengan orang yang baru bangun tidur — sopan, tapi tidak ingat apa pun.

## Yang gampang bikin celaka

Batasi siapa yang boleh memerintah. Nilai rahasia jangan pernah masuk ke dalam percakapan. Pasang juga batas jumlah pesan per jam, karena pemakaian model tetap dihitung dan grup ramai bisa menguras anggaran dalam sehari.

Satu sikap yang perlu ditanam sejak awal: agen lebih baik menunda atau mengaku tidak tahu daripada menjawab salah dengan yakin. Untuk urusan jadwal kajian, jawaban keliru lebih mahal daripada balasan yang dua menit lebih lambat.

Uji terakhirnya sederhana: kirim pesan tengah malam, saat tak ada yang menunggui layar, lalu matikan server dan nyalakan lagi. Kalau balasannya tetap datang, pintunya sudah benar-benar terpasang.

Di bagian berikutnya: menyambungkan alat kerja — supaya agen bisa membaca berkas, mencari di internet, dan menyusun jadwal, plus ingatan agar percakapan tidak hilang tiap mesinnya menyala ulang.
