# Vital Threshold — Rencana Kerja (Work Plan)

Status hidup produksi channel **Vital Threshold**. Update kolom status tiap kali ada progres. Otoritas aturan = `production-bible.md`.

_Terakhir diperbarui: 2026-07-31_

---

## Status saat ini
| Aset / tahap | Status | Catatan |
|---|---|---|
| Production Bible v1.0 | ✅ Selesai | `references/production-bible.md` — dokumen terkunci |
| Naskah VT-001 (Anesthesia) | ✅ Selesai (draft) | `references/VT-001-script.md` — hasil cowork, bible-compliant |
| Verifikasi angka klinis VT-001 | ⬜ Perlu dokter | 2 mg/kg, propofol 1%, ~8 mnt kerja, 86 M neuron, ~20 dtk sirkulasi (lihat Catatan Produksi di naskah) |
| Character sheet MONI | ⬜ Belum | 5 pose, `char-moni-master.png` — via higgsfield-generate |
| Character sheet CARDIO | ⬜ Belum | `char-cardio-master.png` |
| Character sheet ALVI | ⬜ Belum | `char-alvi-master.png` |
| Character sheet BACTI | ⬜ Belum | `char-bacti-master.png` (belum dipakai di VT-001) |
| Master style reference terkunci | ⬜ Belum | simpan 1 still terbaik sbg acuan konsistensi |
| Shot list VT-001 (64 shot) | ✅ Selesai | `references/VT-001-shotlist.md` — padat di PIVOT, ~48 generate + 16 reuse |
| Ilustrasi still VT-001 | ⬜ Belum | master prompt + reference sheet |
| Motion (image-to-video) VT-001 | ⬜ Belum | klip 5 dtk, gerak minimal (denyut/partikel/cairan) |
| Narasi (voice terkunci) | ⬜ Belum | 1 voice selamanya (ElevenLabs / Higgsfield audio) |
| Rakit + subtitle EN/ID | ⬜ Belum | CapCut atau assembly Higgsfield |
| Upload VT-001 + disclosure sintetis | ⬜ Belum | centang "altered/synthetic content" (WAJIB) |
| Potong 2–3 Shorts VT-001 | ⬜ Belum | 20–45 dtk |

## Blocker aktif
1. **Higgsfield credits = 0 (plan free).** Semua generate gambar/video/voice tertahan sampai kredit diisi / trial aktif.
2. **Egress policy:** beberapa host diblok di sesi ini (YouTube, clerk auth). Generate tetap bisa via MCP `mcp__Higgs__*` saat kredit ada.

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
