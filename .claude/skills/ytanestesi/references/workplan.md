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
| Character sheet MONI | 🟡 Ter-generate, belum ter-commit | Higgsfield job `f3357d4e…`, Nano Banana Pro, 2752×1536 16:9, 5 pose. File `char-moni-master.png` belum bisa disimpan ke repo (CDN egress-blocked — lihat Blocker #1). URL di bawah. |
| Character sheet CARDIO | 🟡 Ter-generate, belum ter-commit | Higgsfield job `420f332c…`, Nano Banana Pro, 2752×1536 16:9, 5 pose. `char-cardio-master.png` — idem. |
| Character sheet ALVI | 🟡 Ter-generate, belum ter-commit | Higgsfield job `0d99e267…`, Nano Banana Pro, 2752×1536 16:9, 5 pose. `char-alvi-master.png` — idem. |
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
1. **CDN Higgsfield diblok egress → PNG tidak bisa di-download & di-commit ke repo.** MCP `mcp__Higgs__*` SUDAH tersambung dan generate BERHASIL (kredit 1000, plan plus). Tapi file hasil dilayani lewat `d8j0ntlcm91z4.cloudfront.net`, dan host itu + semua `*.higgsfield.ai` ditolak policy egress (403 CONNECT). Cuma host whitelist (mis. `github.com`) yang tembus, jadi byte gambar tidak bisa ditarik ke environment ini. **Fix (pilih satu):**
   - Whitelist `d8j0ntlcm91z4.cloudfront.net` (atau `*.cloudfront.net`) di network policy environment, lalu jalankan ulang download (URL di bawah) → simpan `char-*-master.png`, commit.
   - Atau download manual 3 URL di bawah dari akun Higgsfield, taruh di `references/`, commit.
   - Atau jalankan dari environment tanpa restriksi egress.

### URL hasil generate (siap di-download begitu egress dibuka)
Job Higgsfield tersimpan permanen di akun; URL PNG penuh (2k, 16:9):
- **MONI** (`f3357d4e-4216-4347-b0a7-43401bfce947`): `https://d8j0ntlcm91z4.cloudfront.net/user_3HGLmxg8ehmKtoLNSzMjqzKQ0Ec/hf_20260731_142808_f3357d4e-4216-4347-b0a7-43401bfce947.png`
- **CARDIO** (`420f332c-8f45-49bc-8e97-1b2f495a58e4`): `https://d8j0ntlcm91z4.cloudfront.net/user_3HGLmxg8ehmKtoLNSzMjqzKQ0Ec/hf_20260731_142814_420f332c-8f45-49bc-8e97-1b2f495a58e4.png`
- **ALVI** (`0d99e267-b395-463c-825d-b2815af012c3`): `https://d8j0ntlcm91z4.cloudfront.net/user_3HGLmxg8ehmKtoLNSzMjqzKQ0Ec/hf_20260731_142826_0d99e267-b395-463c-825d-b2815af012c3.png`

2. Setelah 3 PNG masuk repo: kunci sebagai reference image, review konsistensi (5 pose/karakter, palet 5 warna, glow-from-within), lalu lanjut ~48 shot `VT-001-shotlist.md`. Prompt sumber tetap di `references/character-sheet-prompts.md`.

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
