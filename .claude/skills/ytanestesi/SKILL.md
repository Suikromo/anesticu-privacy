---
name: ytanestesi
description: "Panduan faceless YouTube channel niche EDUKASI KESEHATAN / anestesi-ICU (gaya dokumenter AI penuh tanpa wajah) memakai Claude Fable 5 + Higgsfield MCP. Berisi ide topik aman & evergreen, contoh hook, prompt skrip & video siap pakai, plus aturan akurasi medis + disclaimer. Dipakai saat user minta \"channel edukasi kesehatan AI\", \"video dokumenter anestesi/ICU\", atau menyebut /ytAnestesi."
---

Kamu memandu user membangun **faceless YouTube channel edukasi kesehatan** (fokus anestesi/ICU & sains medis populer) bergaya **dokumenter AI penuh** — tanpa wajah, voice-over AI, visual sinematik. Basis alurnya sama dengan skill `ytfaceless`, tapi diadaptasi untuk niche medis: akurat, aman, evergreen, dan mendidik. Alat: **Claude Fable 5** (riset + skrip + fact-check) + **Higgsfield MCP** (visual, voice-over, musik, thumbnail).

## Positioning channel
- **Niche:** Education + Health (RPM tinggi, retensi bagus, evergreen).
- **Gaya:** dokumenter naratif "sehari dalam hidup / bagaimana tubuh bekerja / kisah medis" — bukan nasihat pengobatan personal.
- **Sudut khas dr. Hendra:** anestesi, ICU/perawatan kritis, fisiologi tubuh, sejarah kedokteran. Ini pembeda yang kredibel.

## Aturan WAJIB (akurasi & keamanan medis)
1. **Edukasi, BUKAN nasihat medis personal.** Jangan pernah menyuruh penonton mendiagnosis/mengobati diri sendiri, mengatur dosis, atau menghentikan terapi. Selalu arahkan ke tenaga kesehatan.
2. **Fact-check ketat.** Minta Claude memverifikasi angka, mekanisme, guideline. Hindari klaim sensasional/menakut-nakuti.
3. **Disclaimer di setiap video** (deskripsi + voice-over singkat): "Konten ini untuk edukasi umum, bukan pengganti konsultasi dokter."
4. **Hindari konten membahayakan** (cara menyalahgunakan obat, prosedur berbahaya untuk ditiru, dosis spesifik yang bisa disalahgunakan seperti obat anestesi/sedasi). Jaga level tetap konseptual & aman.
5. **Hormati privasi & etik.** Jangan pakai kasus pasien nyata yang bisa diidentifikasi.

## Prasyarat
- Higgsfield MCP tersambung ke Claude (lihat skill `ytfaceless` LANGKAH 1). Bila belum tersambung di sesi ini, workflow bisa dipelajari/di-dry-run tapi produksi otomatis belum bisa dijalankan.
- Channel YouTube untuk publikasi.

## LANGKAH 1 — Setup (sama seperti ytfaceless)
Ikuti LANGKAH 1 skill `ytfaceless`: buat akun Higgsfield → MCP and CLI → Add custom connector "Higgsfield" di Claude → lanjut di Claude Code.

## LANGKAH 2 — Pilih topik & tulis skrip (1 prompt)
1. Pilih 1 topik dari **Bank Ide** di bawah (atau minta Claude pilih yang paling berpotensi viral).
2. Prompt ke Claude:
   > "You are scripting for a faceless educational health documentary channel (host is an anesthesiologist/ICU angle). Topic: <TOPIK>. Write a 5-minute script in a cinematic, second-person narrative style with a strong hook in the first 5 seconds. Keep it medically accurate, evergreen, and educational — NOT personal medical advice. Add a one-line disclaimer. Fact-check key claims."
3. Tinjau skrip: hook kuat? akurat? aman (tidak memberi dosis/nasihat personal)? Perbaiki bila perlu.

## LANGKAH 3 — Generate video utuh (1 prompt)
Prompt:
> "Make a 5-minute cinematic documentary video from this script using Seedance 2.0 at 1080p, consistent visual style, AI voice-over that fits an educational medical tone, subtle background music. For a faceless YouTube channel."

Higgsfield MCP memecah skrip jadi klip, generate visual + voice-over + musik, jaga gaya konsisten; Claude fact-check. Aset tersimpan ke folder proyek. Tinjau hasil.

## LANGKAH 4 — Packaging (1 prompt)
> "Prepare a YouTube upload package: 3 thumbnails for A/B testing (clean, curiosity-driven, no clickbait medical fear), several title options, an SEO description including the educational disclaimer, and relevant tags (health, medicine, anesthesia, ICU, human body, science)."

## LANGKAH 5 — Skalakan (1 prompt)
> "Make me two more videos from the same channel. Pick evergreen health/medical-science topics with high retention. Deep-research each individually, keep them accurate and safe, unique script and visual style each."

(Opsi Shorts: minta Claude analisis Shorts kesehatan yang viral lalu buat Shorts edukatif original — cocok untuk pertumbuhan cepat.)

## LANGKAH 6 — Upload & jadwalkan
YouTube → Create → Upload → pilih file → tempel judul + deskripsi (dengan disclaimer) → unggah 3 thumbnail (A/B) → isi tags → Publish/Schedule. Ulangi.

## LANGKAH 7 — Monetisasi & anti-demonetisasi
- Syarat YPP: 1.000 subscriber + 4.000 jam tayang (atau jalur Shorts).
- 3 aturan kualitas: suara AI natural & sesuai konteks; skrip original berbasis insight; visual diedit rapi.
- Tambahan untuk niche kesehatan: jaga E-E-A-T (kredibilitas dokter), sertakan sumber di deskripsi bila mengutip data, hindari misinformasi medis (bisa memicu pembatasan monetisasi).

## Bank Ide Topik (aman, evergreen, sinematik)
Anestesi & ICU (konseptual, tanpa dosis):
- "Apa yang terjadi pada tubuhmu saat dibius total?" (fisiologi anestesi umum)
- "60 detik terakhir sebelum operasi: kerja tim anestesi"
- "Bagaimana ventilator menjaga seseorang tetap hidup di ICU"
- "Kenapa kita tidak mengingat apa pun saat operasi?"
- "Nyeri: bagaimana tubuh mengirim & mematikan sinyalnya"
- "Sepsis: perlombaan melawan waktu di ruang gawat darurat"
Sains tubuh & sejarah kedokteran (audiens luas):
- "Sejarah anestesi: dari eter 1846 sampai sekarang"
- "Bagaimana jantung tetap berdetak tanpa perintah sadar"
- "Apa yang sebenarnya terjadi saat kamu pingsan"
- "Perjalanan oksigen dari udara ke setiap selmu"
- "Kisah penemuan yang menyelamatkan jutaan nyawa di ICU"

Contoh HOOK (detik pertama):
- "Dalam 30 detik, dokter ini akan membuatmu tertidur tanpa kamu sadari — begini caranya."
- "Mesin ini bernapas untukmu 20.000 kali sehari. Inilah cara kerjanya."
- "Kamu tidak akan mengingat menit berikutnya. Dan itu memang disengaja."

## Ringkasan alur (TL;DR)
Setup MCP → pilih topik dari Bank Ide → 1 prompt skrip (akurat + disclaimer) → 1 prompt generate dokumenter → 1 prompt packaging → 1 prompt "2 video lagi" → upload & jadwalkan → jaga akurasi + E-E-A-T untuk monetisasi.
