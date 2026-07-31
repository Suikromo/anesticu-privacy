---
name: ytfaceless
description: "Panduan langkah demi langkah membuat faceless YouTube channel bermonetisasi memakai Claude Fable 5 + Higgsfield MCP (riset channel, tulis skrip, generate video utuh, packaging thumbnail/judul/tags, upload & jadwalkan, sampai aturan anti-demonetisasi). Dipakai saat user minta \"buat channel YouTube AI\", \"faceless YouTube\", \"video AI dari 1 prompt\", atau menyebut /ytFaceless."
---

Kamu memandu user membuat **faceless YouTube channel** (tanpa tampil wajah, tanpa tim) yang bisa dimonetisasi, dengan kombinasi **Claude Fable 5** (otak: riset + skrip + fact-check) dan **Higgsfield MCP** (mesin produksi: gambar, video, voice-over, musik, thumbnail). Alurnya: pinjam FORMAT channel yang terbukti (bukan videonya), lalu produksi otomatis lewat prompt.

## Prinsip dasar (sampaikan bila user beginner)
1. **Pinjam format, BUKAN video.** Meniru format (storytelling + visual sinematik + niche edukatif evergreen) = inspirasi yang aman. Menyalin/mengunggah ulang video orang = kena strik konten daur ulang. Jangan pernah lakukan yang kedua.
2. **Views ≠ jumlah subscriber.** Kalau kontennya bagus, algoritma mendorongnya ke non-subscriber. Channel baru tetap bisa besar.
3. **Nilai konten yang menentukan monetisasi**, bukan "AI atau bukan". YouTube hanya menghukum spam AI berkualitas rendah, bukan AI itu sendiri.

## Prasyarat (cek dulu sebelum mulai)
- Akun **Higgsfield AI** + koneksi **Higgsfield MCP** sudah terpasang di Claude (lihat LANGKAH 1). Jika MCP belum tersambung di sesi ini, beri tahu user bahwa produksi otomatis tidak bisa dijalankan sampai koneksi ada — panduan tetap bisa dipelajari/di-dry-run.
- Akun/channel YouTube untuk publikasi.

## LANGKAH 1 — Hubungkan Claude Fable 5 + Higgsfield MCP
1. Buka browser → cari **Higgsfield AI** → buat akun bila belum punya.
2. Di Higgsfield, buka menu **MCP and CLI** → **copy** perintah/URL instalasi yang ditampilkan.
3. Di **Claude**: **Settings → Connectors → Add custom connector**.
4. Beri nama connector **"Higgsfield"** → **paste URL** → klik **Connect**.
5. Pindah ke **Claude Code**; seluruh proses produksi dikerjakan dari sini. Setup selesai.

## LANGKAH 2 — Tentukan niche & tulis skrip (1 prompt)
1. Pilih **niche RPM tinggi**: **Finance**, **Tech**, atau **Education**. Default rekomendasi: **Education** (retensi tinggi, audiens luas, evergreen).
2. Cari 1 channel referensi yang formatnya terbukti di niche itu (contoh video aslinya: "Bright Side").
3. Prompt ke Claude (tempel link channel referensi):
   > "Analyze this channel, its scenarios and hooks, find the common patterns, pick a strong topic yourself, and write me a full script for a similar video. Reference: <LINK_CHANNEL>"
4. Claude Fable 5 otomatis: menganalisis video paling viral, hook, struktur; menemukan pola; memilih topik; menulis skrip lengkap dengan hook kuat di detik pertama.
5. Tinjau skrip bersama user sebelum lanjut (topik cocok? hook menarik? akurat?).

## LANGKAH 3 — Generate video utuh (1 prompt)
1. Ingatkan: video butuh ganti visual tiap 5–10 detik (puluhan klip). Higgsfield MCP menangani semua itu sekaligus.
2. Prompt tunggal (sesuaikan durasi/model/kualitas):
   > "Make a 5-minute video like on the reference account, using Seedance 2.0 at 1080p. It's going on a faceless YouTube channel."
3. Higgsfield MCP otomatis: memecah skrip jadi klip + atur durasi tiap klip, generate visual, **voice-over**, **musik**, dan menjaga **karakter & gaya visual konsisten** sepanjang video. Claude sekaligus **fact-check** dan riset bila ada yang kurang.
4. Semua aset tersimpan otomatis ke **folder proyek** di komputer. Tinjau hasilnya.

> Catatan model: "Seedance 2.0" adalah contoh engine video; ganti sesuai model yang tersedia di Higgsfield saat itu.

## LANGKAH 4 — Packaging untuk YouTube (1 prompt)
1. Prompt:
   > "Put together a complete YouTube upload package: prepare 3 thumbnails for A/B testing, several title options, a description, and tags."
2. Higgsfield generate **3 thumbnail** (untuk A/B test), **opsi judul**, **deskripsi**, **tags** — semua otomatis masuk ke folder proyek.

## LANGKAH 5 — Skalakan jadi content machine (1 prompt)
1. Prompt:
   > "Make me two more videos. Pick topics that would perform well on YouTube for the same channel."
2. Tiap video mendapat riset + skrip + gaya visual UNIK (bukan template copy-paste) karena Claude melakukan deep research per topik.
3. (Opsi Shorts, tumbuh lebih cepat) Prompt: "Analyze the most viral shorts in this niche, find the mechanics that work, and create original shorts based on those insights."

## LANGKAH 6 — Upload & jadwalkan di YouTube
1. YouTube → **Create → Upload video** → pilih file video dari folder proyek.
2. Tempel **judul** + **deskripsi** dari chat; unggah **3 thumbnail** (A/B test); isi **tags**.
3. **Publish** atau **Schedule** (atur tanggal & jam). Ulangi untuk video lain.

## LANGKAH 7 — Monetisasi & aturan anti-demonetisasi
- Syarat monetisasi (YPP): **1.000 subscriber + 4.000 jam tayang** (atau jalur Shorts sesuai kebijakan YouTube terbaru).
- 3 aturan agar AMAN dari demonetisasi:
  1. **Suara AI harus pas dengan konteks** (natural, tidak sumbang).
  2. **Skrip original** dengan insight nyata — bukan teks generik daur ulang.
  3. **Visual diedit rapi** (bukan klip acak asal tempel).
- Peluang tambahan setelah monetisasi: brand deals / paid collaborations.

## Etika & hal yang WAJIB dijaga
- Jangan mengunggah ulang / meniru video orang; hanya format.
- Konten faktual harus benar — manfaatkan fact-check Claude, verifikasi klaim penting.
- Patuhi Pedoman Komunitas & kebijakan konten AI YouTube (mis. label "altered/synthetic content" bila relevan).

## Ringkasan alur (TL;DR)
Setup MCP → 1 prompt riset+skrip → 1 prompt generate video utuh → 1 prompt packaging (thumbnail/judul/tags) → 1 prompt "buat 2 video lagi" → upload & jadwalkan → penuhi syarat monetisasi sambil jaga 3 aturan kualitas.
