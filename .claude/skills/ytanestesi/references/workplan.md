# Vital Threshold — Rencana Kerja (Work Plan)

Status hidup produksi channel **Vital Threshold**. Update kolom status tiap kali ada progres. Otoritas aturan = `production-bible.md`.

_Terakhir diperbarui: 2026-07-31_

---

## Status saat ini
| Aset / tahap | Status | Catatan |
|---|---|---|
| Production Bible v1.0 | ✅ Selesai | `references/production-bible.md` — dokumen terkunci |
| Retention DNA v1.0 | ✅ Selesai | `references/retention-dna.md` — lapisan hook/retensi (riset BRIGHT SIDE dkk, disaring lewat bible). Tertaut di SKILL.md. |
| Naskah VT-001 (Anesthesia) | ✅ Selesai (draft) | `references/VT-001-script.md` — hasil cowork, bible-compliant |
| Verifikasi angka klinis VT-001 | ✅ Terverifikasi dokter (2026-08-01) | 2 mg/kg (dewasa sehat; lansia 1–1,5) ✅ · 1% ✅ · durasi diperbaiki ~8→**5–10 mnt** · 86 M neuron ✅ · onset LOC ≈30 dtk, sirkulasi ~20 dtk. Detail + 1 keputusan terbuka (beat "won't reach fifteen") di Catatan Produksi naskah. |
| Character sheet MONI | ✅ Selesai & ter-commit | `references/char-moni-master.png` (2000×1116, 5 pose). Higgsfield job `f3357d4e…` (Nano Banana Pro, 16:9). |
| Character sheet CARDIO | ✅ Selesai & ter-commit | `references/char-cardio-master.png` (2000×1116, 5 pose). Higgsfield job `420f332c…`. |
| Character sheet ALVI | ✅ Selesai & ter-commit | `references/char-alvi-master.png` (2000×1116, 5 pose). Higgsfield job `0d99e267…`. |
| Character sheet BACTI | ⬜ Belum | `char-bacti-master.png` (belum dipakai di VT-001) |
| Master style reference terkunci | ⬜ Belum | simpan 1 still terbaik sbg acuan konsistensi |
| Shot list VT-001 (64 shot) | ✅ Selesai | `references/VT-001-shotlist.md` — padat di PIVOT, ~48 generate + 16 reuse |
| Master style reference terkunci | ✅ Selesai | still ruang-OR (`323c14a0`) jadi jangkar gaya shot NEW. Detail di `VT-001-renders.md`. |
| Ilustrasi still VT-001 | 🟡 Semua ter-generate, nunggu QC | 48 still ter-generate (9 CHAR + 1 style still + 38 NEW/TPL), Nano Banana Pro, anchor terkunci. Detail: `references/VT-001-renders.md`. Wave 1 sudah di-QC "bersih"; Wave 2–3 nunggu QC gallery. |
| Motion (image-to-video) VT-001 | 🟡 Semua ter-submit (~46 klip) | Kling 3.0 Turbo 5 dtk 1080p, gerak minimal. M1 hero ✅ QC lolos. M2 CHAR + M3 plate + M4 NEW rendering. **Skop: semua shot di-motion termasuk plate kartu** → CapCut tinggal teks+potong+subtitle. Semua preset sinematik ditolak (style-lock). Detail: `VT-001-renders.md`. |
| Narasi (voice terkunci) | ✅ Selesai | **Voice TERKUNCI: Cillian** (`seed_audio`, `d8ba9f14…`) — dicatat di bible bagian 1 + SKILL.md, dipakai selamanya. Narasi VT-001 lengkap 10/10 scene (job ID di `VT-001-renders.md`). |
| Panduan rakit (assembly) | ✅ Selesai | `references/VT-001-assembly.md` — peta VO→shot, daftar teks overlay, desain audio, lapisan retensi, checklist upload, ide Shorts. |
| Rakit + subtitle EN/ID | ⬜ Belum (kerja manual user) | Ikuti `VT-001-assembly.md` di CapCut. Semua aset sudah jadi & tercatat. |
| Packaging VT-001 (judul/deskripsi/tag/thumbnail) | ✅ Selesai | `references/VT-001-packaging.md` — judul + 3 alternatif A/B, deskripsi siap tempel (chapters + disclaimer + sumber), tag, konsep & prompt thumbnail. |
| Upload VT-001 + disclosure sintetis | ⬜ Belum | centang "altered/synthetic content" (WAJIB). Pakai paket di `VT-001-packaging.md`. |
| Potong 2–3 Shorts VT-001 | ⬜ Belum | 20–45 dtk |

## Blocker aktif
**Kredit Higgsfield habis (2026-08-01).** Tidak menghambat VT-001 — semua aset (48 still, 46 klip, 10 narasi) sudah jadi & tercatat; sisa pekerjaan VT-001 murni perakitan di CapCut.
**Jalur pengganti dipilih user: generate MANUAL di Google (Gemini app / Flow) dgn langganan Google AI Pro** → panduan: `references/prompt-pack-google.md`.
- Modelnya sama: `nano_banana_pro` = **Gemini 3 Pro Image**. Jadi gaya visual tetap konsisten dgn aset yang sudah ada.
- Untuk video, Flow memakai **Veo** (bukan Kling) — perkuat kata kunci penahan gerak (lihat prompt pack bagian 4).
- ⚠️ Google AI Pro = akses web UI saja, **bukan** API key. Otomatisasi penuh butuh API key AI Studio (billing terpisah); endpoint `generativelanguage.googleapis.com` sudah terbukti tembus dari environment ini bila suatu saat ditempuh.
- Claude tidak bisa menjalankan Flow/Gemini app (web UI diblok egress) → generate = kerja manual user, Claude menyiapkan prompt & menjaga catatan.

### Catatan aset character sheet
- 3 PNG di `references/` (`char-moni/cardio/alvi-master.png`, 2000×1116) = versi yang di-review & di-approve user, di-decode dari attachment chat lalu convert ke PNG. **Konsistensi sudah dicek visual: 5 pose/karakter, palet, glow-from-within — approved.**
- Master resolusi penuh (2752×1536, 16:9) masih tersimpan di akun Higgsfield bila nanti butuh yang lebih besar. Job ID: MONI `f3357d4e…`, CARDIO `420f332c…`, ALVI `0d99e267…`. URL CDN (`d8j0ntlcm91z4.cloudfront.net/user_3HGLmxg8ehmKtoLNSzMjqzKQ0Ec/…`) hanya bisa di-download dari environment tanpa restriksi egress (di sesi ini host itu diblok policy 403).
- BACTI belum dibuat (tidak dipakai di VT-001).

### Berikutnya
Kunci 3 PNG ini sebagai reference image, lalu lanjut generate ~48 shot `VT-001-shotlist.md` (pakai master prompt + reference sheet). Prompt sumber tetap di `references/character-sheet-prompts.md`.

## Urutan kerja berikutnya (begitu kredit ada)
1. Generate **4 character sheet** (MONI, CARDIO, ALVI, BACTI) → pilih terbaik → simpan `char-*-master.png`. **Ini aset paling berharga — kunci gaya dulu sebelum apa pun.**
2. Kunci **master style reference** (1 still lingkungan ruang operasi bergaya bible).
3. Pecah **VT-001 jadi shot list** (55–65 scene, 1 gambar / 8–10 dtk).
4. Generate still per shot (master prompt + reference sheet).
5. image-to-video motion halus per shot.
6. Rekam/generate **narasi** (verifikasi angka klinis dulu).
7. Rakit + subtitle EN/ID + desain audio (pulse-ox pitch = elemen kunci).
8. Upload + disclosure sintetis + deskripsi (disclaimer + sumber).
9. Potong Shorts.
10. Lanjut ke VT-002 … VT-010 (lihat bible bagian 7) mengikuti ritme bulanan.

## Roadmap 10 video (bible bagian 7)
VT-001 ✅ naskah → VT-002 Cardiac arrest → VT-003 Drowning → VT-004 Sepsis → VT-005 Ventilator → VT-006 Awake during surgery → VT-007 Coma → VT-008 Autoimmune ("body kills you saving you") → VT-009 Bleeding out → VT-010 ECMO ("machine that replaces heart & lungs").

## Prinsip proses (dari bible bagian 6)
- Tanggal 1–15 (kerja klinis): **riset + naskah saja**, 45 mnt/hari.
- Tanggal 16–30 (libur): **batch produksi visual + rakit** semua video bulan depan.
- Rilis terjadwal otomatis; tidak ada produksi mendadak.
