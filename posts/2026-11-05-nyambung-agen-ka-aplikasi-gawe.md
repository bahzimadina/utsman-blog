---
title: "Bagian 5: Nyambungkeun Agén ka Aplikasi Gawé (Integrasi Data MCP)"
date: 2026-11-05
slug: nyambung-agen-ka-aplikasi-gawe
lang: su
pair: integrasi-data-mcp
excerpt: "Agén anu geus bisa diajak ngobrol can tangtu nyaho eusi berkas atawa jadwal gawé anjeun. Bagian ieu muka pantona liwat MCP, hiji protokol pikeun nyambungkeun loba aplikasi sakaligus."
tags: [tutorial, agén-ai, mcp, integrasi]
draft: false
series: setup-ai-agent
series_title: Nyiapkeun Asisten AI Sorangan, Léngkah demi Léngkah
part: 5
---

Di bagian kaopat agén geus boga panto: nomer WhatsApp jeung bot Telegram anu ngajawab iraha waé. Masalahna, éta agén téh masih siga pagawé anyar anu nyaho loba hal umum tapi buta kana méjana sorangan. Ditanya jadwal kajian bulan ieu, manéhna ngaduga. Dipénta ngarapihkeun catetan rapat, manéhna bingung catetanna aya di mana.

MCP nutup éta celah. Ngaranna kadéngéna téknis — Model Context Protocol — tapi gagasanana basajan: hiji kasapukan cara nyarita antara agén jeung aplikasi séjén, sangkan agén bisa muka berkas, maca kalénder, nyatet kana spreadsheet, atawa maluruh arsip tanpa anjeun nulis kode sambungan hiji-hiji.

## Ku naon henteu disambungkeun sorangan waé

Bisa, tapi mahal. Unggal aplikasi boga jalan sorangan: nu hiji ménta konci aksés, nu séjén liwat polder babarengan, nu katilu liwat API anu dokuméntasina satengah jadi. Lamun aya lima aplikasi, anjeun nulis lima sambungan, sarta unggal sambungan ruksak sorangan basa aplikasina robah.

Ku MCP, sambunganana dipisahkeun ti agén. Aya nu ngaranna server MCP — program leutik anu nangtung di hareupeun hiji aplikasi sarta narjamahkeun paréntah agén jadi aksi nyata. Ganti aplikasi, ganti server-na waé; agénna teu kudu dibongkar.

## Mimitian ti méja sorangan

Urutan anu asup akal: berkas heula, tuluy kalénder, kakara aplikasi kantor. Polder gawé téh sumber paling loba pananya sapopoé — surat, notulen, daptar hadir. Sambungkeun dina mode baca waé pikeun sababaraha poé kahiji. Anjeun bakal reuwas sabaraha sering agén dipaké pikeun maluruh "éta surat anu bulan kamari téh".

Kalénder nyusul lantaran mangpaatna langsung karasa: agén bisa ngajawab "minggu hareup aya rapat naon" tanpa anjeun muka aplikasi. Spreadsheet jeung catetan digital asup panungtung, sarta biasana paling rawan, sabab di dinya agén meunang nulis, lain ukur maca.

## Konfigurasi dina hiji tempat

Sadaya server MCP didaptarkeun dina hiji berkas konfigurasi: ngaran server, paréntah pikeun ngajalankeunana, jeung nilai rusiahna. Tilu kabiasaan anu nyalametkeun:

- Nilai rusiah disimpen dina berkas misah kalawan idin maca keur nu bogana wungkul, ulah ditempelkeun dina jero kode.
- Hiji server, hiji idin. Ulah méré hiji sambungan aksés ka sadaya polder ngan ku lantaran leuwih praktis.
- Béré ngaran anu jelas: "arsip-dkm" leuwih gampang dilacak tibatan "server1".

Lamun hiji server gagal jalan, agén biasana tetep hirup tapi kaleungitan hiji kamampuh. Éta malah hadé — kagagalan leutik teu ngajungkiringkeun sadayana sakaligus.

## Uji hiji-hiji

Ulah sambungkeun lima aplikasi tuluy miharep kabéhna bener. Hurungkeun hiji, taroskeun hal anu jawabanana geus anjeun terang, pariksa naha jawabanana bener-bener dicokot tina berkas atawa ukur dugaan anu kadéngéna rapih.

Pananya uji anu hadé téh spesifik sarta bisa dipariksa. "Sebutkeun tilu berkas dina polder notulen" jauh leuwih mangpaat tibatan "naon eusi polder abdi". Lamun jawabanana meleset, paéhkeun heula éta server, ulah nuluykeun ka aplikasi saterusna.

## Wates anu kudu dipasang

Agén anu bisa nulis téh agén anu bisa salah nulis. Pikeun arsip jeung catetan resmi, buka mode baca heula; idin nulis dibéré sanggeus anjeun yakin polana bener. Simpen salinan polder penting, sarta ulah ngarahkeun agén ka tempat anu teu meunang dirampa ku saha waé.

Hiji deui: sebutkeun dina obrolan yén agén boga aksés kana data gawé. Jalma kudu nyaho, komo lamun di grup aya nu naroskeun soal data pribadi.

Di titik ieu agén robah tina babaturan ngobrol jadi batur gawé. Sanggeus datana asup, bagian kagenep nambahkeun hiji deui: agén anu gerak sorangan nurutkeun jadwal, tanpa kudu diingetkeun ku anjeun.
