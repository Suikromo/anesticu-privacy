# VT-001 — Panduan Rakit (Assembly Guide untuk CapCut)

Semua aset produksi sudah jadi. Dokumen ini = **urutan kerja perakitan**, dibuat supaya kerja manual di CapCut seminimal mungkin.

_Dibuat 2026-08-01 · sumber: `VT-001-shotlist.md` (urutan) · `VT-001-script.md` (narasi & desain audio) · `VT-001-renders.md` (job ID aset) · `production-bible.md` (aturan)._

---

## 0. Ambil asetnya dulu (satu kali)
Semua aset ada di akun Higgsfield (gallery). Download ke 3 folder:
```
VT-001/
  clips/     ← ~46 klip motion (5 dtk, 1080p, 16:9)
  vo/        ← 10 file narasi (per scene)
  stills/    ← 48 still (cadangan; dipakai utk shot REUSE & thumbnail)
```
Penamaan disarankan: `S07.mp4`, `S20.mp4`, `vo-scene1.wav`, dst. — cocokkan dgn job ID di `VT-001-renders.md`. Penamaan rapi = separuh pekerjaan editing selesai.

## 1. Prinsip perakitan (baca sekali, hemat banyak waktu)
1. **Narasi adalah tulang punggung.** Taruh 10 file VO dulu di timeline sesuai urutan scene, baru pasang gambar di atasnya. Jangan sebaliknya.
2. **Klip 5 dtk, narasi lebih panjang** → satu shot bisa di-loop/diperpanjang, atau pakai 2–3 shot untuk satu paragraf. Ikuti kolom Waktu di shotlist sebagai patokan, bukan aturan mati — **narasi yang menentukan**.
3. **Shot REUSE (16 buah) tidak punya klip sendiri** — pakai ulang klip yang sudah ada + beri variasi (slow zoom, atau layer teks/angka baru). Ditandai 🔁 di shotlist.
4. **Teks tidak ada di dalam gambar** (sengaja). Semua judul/angka/etimologi ditempel di CapCut — plate-nya sudah disiapkan kosong.

## 2. Peta narasi → shot
| VO | Scene | Shot yang dipakai | Catatan |
|---|---|---|---|
| `vo-scene1` | 1 Cold open | S01(TPL) → S02 → S03 → S04🔁 | S04 = split-screen S02 vs S03 |
| — | 2 Title card | S05(TPL) | tanpa VO, maks 6 dtk |
| `vo-scene3` | 3 Holding area | S06 → S07 → S08 → S09🔁 → S10 → S11 | S09 = reuse S07 |
| `vo-scene4` | 4 Etimologi 1 | S12(TPL) → S13 → S14 | |
| `vo-scene5` | 5 Obat masuk | S15 → S16 → S17 → S18 → S19 | |
| `vo-scene6` | 6 Mekanisme | S20 → S21🔁 → S22 → S23 → S24 → S25 → S26🔁 → S27 → S28🔁 → S29🔁 → S30 → S31 | scene terpadat |
| `vo-scene7` | 7 Aritmetika | S32 → S33🔁 → S34🔁 → S35 → S36🔁 | 🔁 = S32/S35 + angka baru |
| `vo-scene8` | 8 **PIVOT** | S37 → S38🔁 → S39 → S40 → S41 → S42 → S43 → S44 → S45 → S46 → S47 → S48 → S49 | jantung video |
| `vo-scene9` | 9 Resolusi | S50 → S51 → S52 → S53 → S54 → S55 → S56🔁 → S57🔁 → S58 | S56=reuse S17, S57=reuse S07 |
| `vo-scene10` | 10 Zoom out | S59🔁 → S60🔁 → S61🔁 → S62 → S63🔁 | mayoritas reuse (membalik mekanisme) |
| `vo-scene11` | 11 Sign-off | S64(TPL) | |

## 3. Teks yang perlu ditempel (font bible bagian 2.6)
**Archivo Black** = judul & angka (angka warna Amber `#FFB23F`) · **Inter Semibold** = subtitle · **Inter Medium Italic** Cyan `#35E0D8` = istilah medis.

| Shot | Teks | Warna/Font |
|---|---|---|
| S05 | `WHAT ACTUALLY HAPPENS WHEN YOU ARE PUT UNDER ANESTHESIA` + sub `VITAL THRESHOLD` | Bone / Archivo Black · sub Cyan |
| S12 | `ANESTHESIA` | Bone, besar |
| S13 | `AN` \| `AISTHESIS` + arti "without" / "sensation" | Cyan italic |
| S19 | `~20 seconds` | Amber |
| S30 | `eleven… twelve… nothing` | Bone |
| S32 | `2 mg/kg` | Amber |
| S33 | `75 kg → 150 mg` | Amber |
| S34 | `1% = 10 mg/mL → 15 mL` | Amber |
| S36 | `5–10 min` ⚠️ (**bukan** ~8 min — sudah dikoreksi dokter) | Amber |
| S40 | `APNEA` = `A` (without) + `PNOIA` (breath) | Cyan italic |
| S42 | `HYPOTENSION` = `HYPO` (under) + `TENSIO` (pressure) | Cyan italic |
| S53 | `LARYNGOSCOPE` = `LARYNX` (voice box) + `SKOPEIN` (to look) | Cyan italic |
| S58 | `every breath = a decision` | Bone |
| S64 | `VITAL THRESHOLD` | Bone |
| 0:00–0:20 | **Sitasi sumber on-screen** (WAJIB, checklist bible) | kecil, Bone |

## 4. Desain audio — ini separuh nyawa video
Bible: *"Suara mengerjakan separuh pekerjaan. Jangan perlakukan sebagai musik latar."* Elemen kunci = **nada pulse-oximeter**.

| Scene | Audio |
|---|---|
| 1 | Sunyi. Satu bunyi monitor tunggal di kata terakhir. |
| 3 | Monitor stabil, tempo pelan, nada tinggi konstan. **Jangan ditutup musik.** |
| 5–6 | Tempo monitor tetap; musik masuk sangat pelan. Saat neuron meredup, musik surut. |
| 6 (bulu mata, S31) | **SEMUA audio berhenti kecuali satu bunyi monitor.** Titik paling sunyi di video. |
| 8 PIVOT | **Pitch monitor turun bertahap & nyata** — penonton harus *mendengar*, bukan diberi tahu. Lalu alarm. |
| 9 | Alarm berhenti → bunyi ventilator ritmis-mekanis → nada monitor naik lagi. |
| 10 | **Musik penuh, pertama kali di seluruh video.** |
| 11 | Kembali ke satu bunyi monitor, lalu sunyi. |

Cari SFX pulse-oximeter bebas royalti, atau buat dari nada sinus sederhana yang di-pitch-shift.

## 5. Lapisan retensi (dari `retention-dna.md`)
- Hook tajam **0:00–0:03** sebelum title card — jangan taruh intro apa pun di depannya.
- **Pattern interrupt tiap 7–12 dtk**: ganti shot / angka Amber masuk / nada monitor berubah.
- **Re-hook sebelum PIVOT** (akhir scene 7, kalimat "Which brings us to the problem") — beri jeda kecil, biarkan menggantung.
- Title card **maksimal 6 detik** — jangan bunuh momentum.
- Opsional (kalau mau rasa sinematik): **slow push-in** ~2–3% pada klip statis. Di CapCut bisa diterapkan sekali ke banyak klip.

## 6. Subtitle
- **EN** dari naskah (`VT-001-script.md`, blok `[NARASI]`) — sudah final, tinggal salin.
- **ID** = terjemahan naskah.
- Inter Semibold, putih, outline gelap tipis.

## 7. Checklist sebelum upload (bible bagian 8)
- [ ] Sitasi sumber tampil on-screen ≤20 dtk pertama
- [ ] Disclaimer di deskripsi (teks wajib bible bagian 1)
- [ ] **Centang disclosure "altered or synthetic content"** di YouTube Studio ← WAJIB
- [ ] Tidak ada nama pasien (episode ini tanpa pasien spesifik)
- [ ] ≥3 etimologi ✅ (ANESTHESIA, APNEA, HYPOTENSION, LARYNGOSCOPE = 4)
- [ ] 1 analogi skala absurd ✅ (satu sendok makan)
- [ ] Pivot jelas di paruh kedua ✅ (5:30–7:05)
- [ ] Palet tidak keluar 7 warna terkunci
- [ ] Subtitle EN + ID terpasang
- [ ] Sign-off terucap ✅ ("Take the pulse. Know the threshold.")

## 8. Setelah upload
Potong **2–3 Shorts** (20–45 dtk) dari momen terkuat:
1. **Analogi sendok makan** (S35) — paling shareable.
2. **Tes bulu mata** (S31) — paling emosional/sunyi.
3. **Pivot** "The drug is the thing trying to kill you" (S49) — paling menghentikan scroll.
