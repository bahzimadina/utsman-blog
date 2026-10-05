# utsman-blog — eusi blog utsman.works

Repositori ieu **ngan eusi** (tulisan dina format markdown). Situs **ngabaca** ti dieu,
terus ngarobihna jadi halaman blog anu rapih dina <https://utsman.works/blog/>.

Tulisan anu di-push ka dieu bakal muncul dina situs dina **±10 menit** (otomatis).

---

## Cara nulis hiji tulisan

1. Jieun berkas anyar dina folder `posts/` kalayan ngaran: `YYYY-MM-DD-judul-singkat.md`
   (contona `2026-10-12-laporan-bulanan.md`).
2. Eusian bagian luhur (frontmatter) di antara dua garis `---`, tuluy tulis eusina dina markdown.
3. Simpen / commit / push. Bérés.

### Conto

```markdown
---
title: Cara Menyusun Laporan Bulanan yang Rapi
date: 2026-10-12
lang: id          # id = Indonesia, en = Inggris, su = Sunda
excerpt: Tiga langkah sederhana supaya laporan bulanan selesai tanpa lembur.
tags: [laporan, administrasi]
draft: false      # true = masih draf, teu kaluar dina situs
---

Paragraf bubuka...

## Sub judul

- poin kahiji
- poin kadua

> Kutipan atawa catetan penting.
```

### Widang frontmatter

| Widang    | Wajib | Katerangan                                                        |
|-----------|-------|-------------------------------------------------------------------|
| `title`   | enya  | Judul tulisan                                                     |
| `date`    | enya  | Kaping `YYYY-MM-DD` (urutkeun dina situs dumasar ieu)             |
| `lang`    | henteu| `id` (default), `en`, atawa `su`                                  |
| `excerpt` | henteu| Ringkesan 1–2 kalimat (dipaké dina daptar tulisan + Google)       |
| `tags`    | henteu| Daptar kata kunci, conto `[laporan, keuangan]`                    |
| `cover`   | henteu| Gambar judul — URL lengkep (`https://...`) atawa `/assets/...`    |
| `draft`   | henteu| `true` = henteu dipedalkeun                                          |

### Markdown anu dirojong

Judul (`##`), **kandel**, *miring*, daptar (pringkat/angka), kutipan, tabel, kode,
tautan, jeung gambar. HTML mentah teu dirojong (dibuang ku sistem — pikeun kaamanan).

### Gambar

Simpen gambar dina folder `images/` dina ieu repositori, tuluy rujuk dina tulisan:

```markdown
![Ilustrasi rapat](/blog/images/rapat.jpg)
```

Pénting: gambar anu disimpen dina `images/` kudu **disalin otomatis** ku panerap —
ukur payun `/blog/images/<ngaran-berkas>`.

---

## Kecap konci pikeun Google

Supaya gampang kapanggih: paké `title` anu jelas, tulisan `excerpt`, sareng `tags`.
Situs otomatis nyieun peta situs (`sitemap`) jeung RSS (`feed.xml`).
