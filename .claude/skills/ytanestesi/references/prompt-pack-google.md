# Prompt Pack — Generate Manual di Google (Gemini / Flow)

Dipakai kalau generate **tidak** lewat Higgsfield MCP, tapi manual di produk Google dengan langganan **Google AI Pro**.

_Dibuat 2026-08-01._

---

## 0. Kabar bagus: modelnya sama
Yang selama ini dipakai lewat Higgsfield **adalah model Google**:
| Nama di Higgsfield | Nama aslinya di Google |
|---|---|
| `nano_banana_pro` | **Gemini 3 Pro Image** ("Nano Banana Pro") |
| `nano_banana` / flash | Gemini Flash Image |
| Kling 3.0 Turbo (motion) | ⚠️ bukan Google — padanan Google-nya **Veo** di Flow |

→ Untuk **gambar**, hasil di Gemini app akan konsisten dengan 48 still yang sudah jadi.
→ Untuk **video**, Veo ≠ Kling. Gerakannya akan sedikit beda karakternya — lihat catatan bagian 4.

## 1. Alur kerja manual (gambar)
1. Buka aplikasi **Gemini** → pilih mode gambar (**Nano Banana Pro** / Gemini 3 Pro Image).
2. **Upload reference image** (ini yang mengunci konsistensi — jangan dilewat):
   - Shot dgn maskot → upload `char-moni-master.png` / `char-cardio-master.png` / `char-alvi-master.png` (ada di `references/` repo ini).
   - Shot tanpa maskot → upload **master style still** (establishing ruang OR).
3. Tempel **BLOK A (master style)** + **BLOK B (adegan)** jadi satu prompt.
4. Set rasio **16:9**. Minta resolusi tertinggi yang tersedia.
5. Simpan hasil dgn nama shot: `S07.png`, `S20.png`, dst.

> **Aturan yang tidak boleh dilanggar:** tanpa reference image, konsistensi karakter/gaya **pasti gagal**. Ini bukan opsional.

## 2. BLOK A — Master style (tempel di SETIAP prompt, jangan diubah)
```
STYLE: flat vector illustration, medical educational infographic style,
strictly 2D, no photorealism, no 3D rendering, no depth of field.

PALETTE: dark abyss teal background (#062A2E), deep teal (#0E4249),
oxblood red (#7A1526), arterial red (#C42B3C), bone white (#E6DCC8),
amber (#FFB23F) and cyan (#35E0D8) as glow accents only.
Maximum 5 colours in frame.

LIGHTING: all light emanates from INSIDE the subject, bioluminescent
deep-sea logic. Background stays dark and unlit. No sun, no lamps,
no sky gradients, no rim light from outside.

FORMS: capsule and rounded-rectangle construction, visible seam lines,
thin bone-white outlines on subjects only, flat fills with a single
soft inner glow layer. No gradient mesh, no texture, no noise.

COMPOSITION: centred subject, generous negative space, 16:9,
clean vector edges, no text in image.
```

## 3. BLOK B — Template adegan (isi bagian [ ])

**B1 · Shot dengan maskot** (upload character sheet sbg reference):
```
SCENE: render ONE single [MONI / CARDIO / ALVI] character exactly matching
the character design in the reference image. [DESKRIPSI AKSI & STATE].
Single scene illustration, NOT a multi-pose character sheet.
No text, no numbers, no letters.
```

**B2 · Shot tanpa maskot** (upload master style still sbg reference):
```
Use the reference image ONLY as a style anchor (palette, flat-vector
rendering, inner-glow) — do NOT copy its objects.

SCENE: [DESKRIPSI ADEGAN]. Flat vector.
No text, no numbers, no letters.
```

**B3 · Plate kartu/teks** (untuk judul, etimologi, sign-off):
```
Use the reference image ONLY as a style anchor — do NOT copy its objects.

SCENE: [mis. a single vertical amber EKG line splitting the dark abyss-teal
frame into two empty balanced halves], glowing from within, halves left
EMPTY for text overlay added later in assembly. Flat vector.
No text, no numbers, no letters.
```

> **Kenapa "no text in image"?** Teks ditempel di CapCut (lihat `VT-001-assembly.md` bagian 3) supaya font & warna konsisten dgn bible, dan gampang direvisi. Gemini 3 Pro Image sebenarnya bagus merender teks — tapi tetap jangan, demi konsistensi & kemudahan revisi.

## 4. Motion (video) di Flow — catatan penting
Flow memakai **Veo**, bukan Kling. Prompt gerak yang sudah terbukti aman:
```
Subtle looping animation: [GERAK MINIMAL — mis. the amber EKG line traces
steadily with a gentle heartbeat pulse].
Flat 2D vector style strictly preserved, static camera, no zoom, no pan,
no 3D, no parallax, minimal calm motion, background stays still.
```
**Wajib ada di prompt:** `static camera`, `no 3D`, `no parallax`, `flat 2D preserved`. Model video paling sering "bocor" dgn menambah kedalaman 3D / gerak kamera sinematik — itu melanggar bible.

⚠️ **Jangan pakai preset/template sinematik apa pun** (di Higgsfield namanya "IN THE DARK" — game horor PS1; di Flow ada padanan serupa). Semua merusak style-lock. Selalu pilih generate **literal/custom**.

Kalau Veo terasa terlalu "hidup"/sinematik dibanding Kling: **turunkan durasi & perkuat kata kunci penahan** (`almost still`, `barely moves`, `only the glow changes`).

## 5. Kalau hasilnya meleset — urutan perbaikan
1. **Reference image lupa di-upload** → penyebab #1 gaya melenceng. Cek ini dulu.
2. **Ada objek nyasar dari reference** (mis. meja OR muncul di shot mikro) → tegaskan `do NOT copy its objects, style anchor only`.
3. **Muncul 3D/bayangan** → tambah `strictly 2D, no depth of field, no drop shadow`.
4. **Warna keluar palet** → tegaskan `Maximum 5 colours in frame` + sebut hex-nya lagi.
5. **Teks nyasar muncul** → tambah `absolutely no text, no letters, no numbers, no watermark`.

## 6. Setelah generate
- Simpan file dgn nama shot (`S20.png`, `S20.mp4`).
- Catat di `VT-001-renders.md` (atau `VT-00X-renders.md`) — sumber diganti `Google Gemini/Flow (manual)` alih-alih job ID Higgsfield.
- Commit ke repo supaya tidak hilang.

## 7. Batas yang jujur
- Aku **tidak bisa** menjalankan Flow/Gemini app dari sini (web UI, diblok egress). Jadi generate = kerja tanganmu; aku yang menyiapkan prompt, mereview hasil (kalau kamu paste gambarnya ke chat), dan menjaga catatan repo.
- Kalau nanti mau otomatis penuh lagi, jalurnya **API key Google AI Studio** (billing terpisah dari langganan Pro) — endpoint `generativelanguage.googleapis.com` sudah terbukti tembus dari environment ini. Jangan tempel key di chat; pasang sebagai environment variable.
