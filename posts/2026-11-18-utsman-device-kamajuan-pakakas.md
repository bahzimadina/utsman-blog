---
title: "Kamajuan Utsman Device: Layar Buleud Pinuh, Sambungan Lokal, jeung Kaméra Watcher"
date: 2026-11-18
slug: utsman-device-kamajuan-pakakas
lang: su
pair: utsman-device-progress
cover: /blog/images/utsman-device-watcher-2026-11.jpg
excerpt: Catetan kamajuan prototipe pakakas fisik Utsman dina papan SenseCAP Watcher, ti mimiti tampilan kaméra layar buleud pinuh nepi ka sinkronisasi server lokal.
tags: [utsman-device, pakakas, watcher, kamajuan]
draft: false
---

Salila ieu, Utsman leuwih mindeng dipaké liwat layar telepon di WhatsApp, Telegram, atawa surélék. Minggu ieu mimiti nincak kana wangun fisik: prototipe pakakas méja anu dingaranan **Utsman Device**, diwangun dina papan **Seeed Studio SenseCAP Watcher**.

Dina wadah transparan ieu, Utsman henteu ngan saukur jadi rohangan obrolan. Bagian hareupna maké layar rampa buleud, dilengkepan kaméra di juru luhur, mikropon, sarta spiker bawaan. Dina tés poé ieu, antarbeungeut munggaran geus jalan dina layar buleud: ikon Wi-Fi jeung batré némbongan di luhur, kecap **"Mendengarkan..."** aya di handapeunana, sarta avatar Utsman maké peci hideung cicing di tengah bunderan.

Garapan dina sési ieu museur kana dua perkara utama, nyaéta kakuatan sambungan sanggeus prosés flash firmware jeung ngaropéa tampilan kaméra supaya merenah dina layar buleud.

## Sambungan lokal ngaliwatan utsman.local jeung MQTT

Supaya réspon sora jeung pamrosésan gambar tetep gancang di jaringan sorangan, pakakas ieu disambungkeun langsung ka server lokal ngaliwatan alamat `utsman.local` maké protokol MQTT. Pangaturan awal jaringan ogé geus ngarojong nyeken **QR Wi-Fi**, jadi nyambungkeun alat anyar leuwih ringkes.

Sempet aya hahalang leutik sanggeus prosés flash firmware: alat teu langsung nyambung kira-kira dua menit lantaran ka-reset nalika port serial dibuka pikeun maca log. Sanggeus jalur sambungan di server diparios, prosés hurung balik normal, Wi-Fi nyambung, MQTT jalan, sarta obrolan sora jeung kaméra bisa dipaké deui.

## Tampilan kaméra pinuh dina layar buleud

Parobahan anu paling katingal aya dina cara alat némbongkeun hasil potrét kaméra dina layar hareup. Dina vérsi saméméhna, gambar ukuran 240x240 diperleutik jadi kotak sakitar 200x200 di tengah layar, jadi loba rohangan kosong di sabudeureunana.

Dina patch firmware anyar dina `xiaoai-client.patch` jeung `client.cpp`, pratinjau poto ayeuna digambar minuhan sakabéh layar buleud ukuran 360x360 bari tetep ngajaga babandingan sisi:

- Poto minuhan sakabéh bunderan layar tanpa ngaleutikan di tengah, ngan kakeureut saeutik di sisi kénca-katuhu supaya pas jeung wangun buleud.
- Ikon status di luhur jeung téks katerangan di handap tetep kabaca jelas di luhureun gambar.
- Ukuran poto anu dikirim ka server teu dikurangan pisan, tetep pinuh 480x480 supaya pamrosésan gambar di server tetep seukeut.

## Léngkah tés saterusna

Sanggeus tampilan kaméra pinuh, QR Wi-Fi, jeung sambungan `utsman.local` jalan mulus dina alatna, pagawéan dituluykeun kana nguji menu rampa sarta alur motrét langsung tina Watcher sateuacan sakabéh parobahan firmware di-commit ka repositori.

Tujuan jangka pondokna sederhana: hiji pakakas méja anu cukup dicolokkeun kana listrik, nyambung kana jaringan lokal, tuluy siap diajak nyarita atawa ngabantu maca dokumén langsung.
