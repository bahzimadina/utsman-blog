---
title: "Bagian 6: Otomasi Kajadwalan — Tugas Rutin anu Jalan Tanpa Diingetkeun"
date: 2026-11-12
slug: otomasi-kajadwalan-agen
lang: su
pair: otomasi-terjadwal
excerpt: "Agén anu geus kasambung ka data masih ngadagoan dititah. Bagian ieu masangkeun jamna: tugas rutin anu jalan sorangan unggal isuk, unggal Jumaah, jeung unggal ahir bulan."
tags: [tutorial, agén-ai, otomasi, produktivitas]
draft: false
series: setup-ai-agent
series_title: Nyiapkeun Asisten AI Sorangan, Léngkah demi Léngkah
part: 6
---

Di bagian kalima agén geus bisa muka berkas, maca kalénder, jeung maluruh arsip. Mangpaat kabéh, tapi aya hiji kahéléhan anu teu katingali: agén téh ukur gerak lamun anjeun nyampeurkeun heula. Anjeun hilap nanya, euweuh kajadian. Anjeun keueung tilu poé, tilu poé éta ogé euweuh rekap nanaon.

Bagian ieu masangkeun jam dina éta agén. Lain kamampuh anyar anu rumit — sagala bahan anu dipaké geus aya di bagian saméméhna. Anu robah ukur pamicuana: lain deui pesen ti anjeun, tapi jadwal.

## Bédana obrolan jeung jadwal

Obrolan téh réaktif. Anjeun butuh hiji hal, anjeun nanya, agén ngajawab, anggeus. Ngeunah dipakéna, tapi sakabéh daptar pagawéan tetep cicing dina sirah anjeun. Barang sirah éta pinuh, aya anu kaliwat.

Jadwal mindahkeun sabagian daptar éta ka mesin. Anjeun nangtukeun sakali, mesin malikanana. Pikeun urusan anu polana sarua unggal minggu, ieu jauh leuwih tahan banting tibatan niat alus.

## Naon anu pantes dijadwalkeun

Ukuranna basajan: tugas anu diulang, jawabanana pondok, jeung teu butuh kaputusan gedé. Lamun unggal kali muncul anjeun kudu mikir panjang, éta can pantes diotomatiskeun — hadéna digawé sorangan waé.

Tilu conto anu biasana langsung kapaké:

- Ringkesan isuk: agenda poé ieu, kagiatan anu pangdeukeutna, jeung hal leutik anu can anggeus.
- Pangémut saméméh acara, dikirim dua poé leuwih awal sangkan masih aya waktu ngoméan persiapan.
- Rekap mingguan unggal Jumaah soré: naon anu anggeus, naon anu mandek, naon anu ngadagoan batur.

## Jadwal téh ukur lima kolom

Di balik ngaran keren "cron", eusina lima kolom: menit, jam, tanggal, bulan, poé dina saminggu. `0 5 * * *` hartina jam lima isuk unggal poé. `30 19 * * 5` hartina Jumaah jam satengah dalapan peuting. Tanda béntang hartina "sadaya".

Anjeun teu kudu apal. Anu kudu diinget ukur hiji: jam anu anjeun tulis téh jam mesin, lain jam dinding kantor. Lamun mesinna cicing di zona waktu séjén, ringkesan isuk bisa datang tengah peuting. Pasang zona waktu anu bener heula, kakara percaya kana jadwalna.

## Tugas kajadwalan téh poho sagalana

Ieu bagian anu paling sering ngajadikeun hasilna nguciwakeun. Unggal kali jadwal hurung, agén mimitian ti nol. Manéhna teu inget obrolan kamari, teu inget yén laporan anu sarua geus dikirim minggu kamari.

Ku kituna tulis brief-na lengkep: konteksna naon, bahanna di mana, kaluaranna wangun naon, jeung naon anu kudu digawé lamun bahanna euweuh. Bayangkeun nulis pituduh pikeun jalma anu kakara asup lima menit ka tukang. Kalimah siga "tuluykeun anu kamari" teu boga harti di dieu.

## Leuwih hadé cicing tibatan riweuh

Tugas kajadwalan anu ngirim pesen unggal kali jalan bakal teu dipaduli dina saminggu. Bewara anu datang tanpa aya anu kudu dilakukeun téh ngajar jalma sangkan eureun maca beware.

Pola anu leuwih séhat: laporan ukur lamun aya anu kudu ditingali. Lamun kabéhna normal, euweuh pesen. Tapi cicingna kudu bisa dibédakeun jeung ruksak. Ménta éta tugas tetep nyatet yén manéhna jalan, sarta ménta manéhna nyoara jelas lamun gagal — lain ngaleungit lantaran error teu kawengku.

## Jalankeun heula ku leungeun

Saméméh nyerahkeun hiji hal ka jadwal, panggil sakali sacara manual sarta pariksa hasilna. Dua atawa tilu kali, dina jam anu béda, jeung bahan anu béda. Lamun hasil manualna geus rapih, kakara dipasang jadwalna.

Pikeun bulan kahiji, watesan kana tugas anu maca jeung ngaringkes waé. Tugas anu ngirim ka loba jalma, ngarobah data, atawa mupus hiji hal tungguan nepi ka anjeun yakin betul kana polana. Awas ogé tumpang tindih: dua tugas anu hurung dina menit anu sarua bisa silih ganggu.

Di titik ieu agén geus gerak sorangan, tapi manéhna masih pohoan. Bagian katujuh ngabahas ingetan: cara nyieun agén nyatet naon anu geus digawé, sangkan ringkesan isukan teu malikan ringkesan poé ieu.
