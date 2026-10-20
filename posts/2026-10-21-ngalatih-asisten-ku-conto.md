---
title: "Ajari Asisten AI dengan Contoh, Bukan Perintah Panjang"
date: 2026-10-21
slug: ngalatih-asisten-ku-conto
lang: id
pair: ngalatih-asisten-ku-conto
excerpt: "Perintah panjang sering bikin asisten AI malah bingung. Kasih dua-tiga contoh yang pas, hasilnya lebih akurat dan cepat."
tags: [ai, prompting, produktivitas, teknologi]
draft: false
---

## Perintah Panjang Tidak Menjamin Hasil Lebih Baik

Banyak yang mengira semakin panjang perintahnya, semakin pintar pula jawaban asisten AI. Nyatanya tidak begitu. Ketika Anda menulis ratusan kata mengikuti peta pikiran yang rumit, asistennya justru tersesat dan banyak menyimpang. Model bahasa besar tidak berpikir seperti manusia; ia hanya mendeteksi pola dari kata-kata yang masuk. Kalau polanya rumit, outputnya juga akan rumit.

## Contoh Lebih Efektif

Cara yang lebih simpel adalah *few-shot prompting*: alih-alih menjelaskan aturan panjang, Anda cukup memberikan dua atau tiga contoh input-output yang benar. Misalnya, kalau ingin membuat ringkasan dari catatan rapat, jangan deskripsikan formatnya dalam dua paragraf. Lebih baik: berikan contoh catatan mentah dan hasil ringkasannya.

Contoh sederhana lainnya: mengelompokkan email. Daripada menulis "Tentukan apakah email ini permintaan, laporan, atau promosi. Jika bingung, jawab 'bukan di atas'.", hasilnya lebih tepat kalau Anda memberi contoh seperti ini:

- "Tolong kirim laporan bulanan besok pagi." → permintaan
- "Laporan bulanan Oktober sudah saya kirim kemarin." → laporan
- "Diskon 50% paket premium, hanya hari ini!" → promosi

Asistennya langsung menangkap pola, tanpa perlu membaca aturan panjang.

## Kapan Cara Ini Paling Manjur?

Cara *few-shot* paling manjur ketika Anda perlu mengeluarkan format khusus: tabel, JSON, atau gaya tulisan yang tertentu. Kalau mengelola layanan pelanggan, contoh jawaban yang sopan dan jawaban yang langsung akan menuntun asistennya bagaimana menulis. Uji benchmark LangChain tahun 2024 soal *tool-calling* memperlihatkan bedanya jelas: satu model hanya benar 16% tanpa contoh, lalu naik jadi 52% setelah diberi tiga contoh yang mirip pertanyaannya.

## Praktik Terbaik

- Pilih contoh yang benar, bukan yang kira-kira.
- Patokkan 2–3 contoh; lebih banyak tidak selalu lebih baik.
- Pastikan contoh-contoh itu mencakup kasus yang berbeda (positif, negatif, dan yang agak rumit).
- Kalau asistennya masih salah, ganti contoh, bukan menambah aturan.

## Penutup

Mengajari asisten AI itu mirip mengajari orang lain: contoh langsung lebih efektif dibanding pidato panjang. 🎯
