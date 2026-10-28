---
title: "Bagian 4: Masang Agén jeung Nyambungkeunana ka Kanal"
date: 2026-10-29
slug: masang-agen-jeung-nyambung-kanal
lang: su
pair: pasang-agen-sambung-kanal
excerpt: "Agén anu hurung dina server can bisa diajak ngobrol ku saha waé. Bagian ieu soal masangna, nyieun bot Telegram, nyiapkeun nomer WhatsApp, jeung ngajaga pantona sangkan teu pabalatak."
tags: [tutorial, agén-ai, telegram, whatsapp]
draft: false
series: setup-ai-agent
series_title: Nyiapkeun Asisten AI Sorangan, Léngkah demi Léngkah
part: 4
---

Di bagian katilu urang geus nyiapkeun imahna: server leutik anu hurung terus, agén didaptarkeun jadi layanan, jeung pamariksa poéan sangkan gancang kanyahoan lamun manéhna eureun. Tapi agén anu hirup tanpa nomer téh siga kamar beresih anu taya pantona. Rapih, siap dipaké, tapi taya nu bisa ngetok.

Kanal téh pantona. Sanés aplikasi anyar anu kudu diunduh batur, tapi tempat jalma geus biasa ngobrol unggal poé. Dua ngaran geus cukup: Telegram jeung WhatsApp.

## Masang heula, nyambungkeun engké

Loba nu malikkeun urutanana, tuluy bingung sorangan. Pasang heula agénna nepi ka manéhna bisa ngajawab dina terminal, kakara sambungkeun kanal. Lamun duanana digarap babarengan jeung aya nu gagal, anjeun moal nyaho mana nu salah.

Pasang dina server anu geus disiapkeun minggu kamari, jalankeun salaku layanan, sarta simpen sadaya pangaturanna dina hiji berkas konfigurasi. Berkas anu ngandung nilai rusiah dibéré idin maca keur nu bogana wungkul, jeung ulah diteundeun dina polder anu milu kaunggah ka repositori umum.

Nu kudu diinget: hiji prosés agén bisa ngalayanan sababaraha kanal sakaligus. Ulah nyieun hiji agén per kanal ngan ku lantaran kaciri leuwih rapih di awal — engké aturanna jadi dobel, anjeun nu lieur nyaruakeunana.

## Telegram: panggancangna hirup

Bot Telegram dijieun ngaliwatan hiji akun resmi di jero aplikasi, turutan obrolan pondokna, tuluy anjeun meunang kunci bot. Simpen éta kunci dina berkas konfigurasi, ulah dina jero kode, ulah ogé ditémplokeun di grup obrolan pangurus ménta dipariksa.

Dua hal leutik anu mindeng poho sanggeus botna hirup. Kahiji, daptar saha nu meunang maréntah — ngaran pamaké atawa nomer pamaké anu anjeun percaya, sanés sakur nu manggihan éta bot. Kadua, uji ku pesen beneran: sapa, taroskeun hal anu jawabanana geus anjeun terang, tuluy kirim paréntah anu salah pikeun mastikeun manéhna ngajawab sopan sarta teu ngajawab nanaon.

## WhatsApp: leuwih deukeut, tapi leuwih ribet

WhatsApp leuwih akrab karana di dinya jamaah geus biasa silih kirim pesen. Balukarna leuwih beurat: aturan platformna ketat jeung nomer pribadi saéna ulah dipaké. Sadiakeun nomer misah keur agénna.

Aya dua jalan. Ngaliwatan panyadia resmi, leuwih stabil jeung rapih, tapi pendaftaranna pabalatak jeung biasana mayar. Ngaliwatan sasak henteu resmi, leuwih gancang dicoba, tapi bisa waé kawatesan iraha-iraha. Pikeun uji coba sorangan, jalan kadua asup akal. Pikeun ngalayanan loba jalma, jalan kahiji leuwih aman.

Soal grup: ulah ngantep agén ngajawab unggal pesen di grup jamaah. Cukup ngaréspon lamun ngaranna disebut atawa aya nu ngabales pesenna. Grup anu ramé bisa robah jadi dua robot silih témbal.

## Hiji agén, loba panto

Agén anu boga dua kanal butuh hiji kabiasaan: sadaya pesen asup, ti mana waé asalna, diteundeun dina antrean anu sarua. Agén ngolahna hiji-hiji, tuluy ngabales ka kanal asal éta pesen. Lamun henteu, jawaban keur WhatsApp bisa nyasarkeun ka Telegram.

Simpen ogé catetan obrolan: saha nu ngirim, ti kanal mana, naon nu karék dibahas. Tanpa éta, unggal pesen anyar téh siga ngobrol jeung jalma anu karék hudang — sopan, tapi teu inget nanaon.

## Nu gampang nyilakakeun

Watesan saha nu meunang maréntah. Nilai rusiah ulah kungsi asup kana obrolan. Pasang ogé wates jumlah pesen per jam, sabab pamakéan modél tetep diitung jeung grup anu ramé bisa ngabéréskeun anggaran sa poé.

Hiji sikep anu kudu dipelak ti awal: agén leuwih hadé nunda atawa ngaku teu nyaho tibatan ngajawab salah kalawan yakin. Keur urusan jadwal kajian, jawaban anu salah leuwih mahal tibatan balasan anu datang dua menit engke.

Uji pamungkasna basajan: kirim pesen tengah peuting, basa taya nu nungguan layar, tuluy paéhkeun server sarta hirupkeun deui. Lamun jawabanana tetep datang, hartina pantona geus bener-bener kapasang.

Di bagian salajengna: nyambungkeun parabot gawé — sangkan agén bisa maca berkas, maluruh di internét, jeung nyusun jadwal, katambah ingetan sangkan obrolan teu leungit unggal mesinna hurup deui.
