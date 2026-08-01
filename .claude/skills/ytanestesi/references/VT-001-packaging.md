# VT-001 — Packaging (Judul · Deskripsi · Tag · Thumbnail)

Paket siap tempel untuk upload. Mengikuti **click-promise** (`retention-dna.md`) — memancing kuat tapi **ditepati isi video**, bukan clickbait. Etika & disclaimer wajib dari `production-bible.md`.

_Dibuat 2026-08-01._

---

## 1. JUDUL

**Pilihan utama (rekomendasi):**
```
What Actually Happens When You Are Put Under Anesthesia
```
Kenapa ini: kata **"Actually"** menciptakan curiosity gap (mengisyaratkan yang kamu kira selama ini keliru) dan **dijawab tuntas** di video → click-promise sehat. Netral secara medis, aman monetisasi, dan cocok jadi pola judul seri ("What Actually Happens When…").

**Alternatif (uji A/B kalau performa datar setelah ~1 minggu):**
| # | Judul | Sudut |
|---|---|---|
| 2 | `Anesthesia Is Not Sleep. Here Is What It Actually Does To You` | myth-busting langsung, sesuai hook cold open |
| 3 | `The 90 Seconds After Anesthesia That Almost Kill You` | taruhan/bahaya + angka spesifik (paling agresif — tetap ditepati video) |
| 4 | `Why Anesthesia Stops Your Breathing — And How They Keep You Alive` | pivot ada di judul, cocok utk audiens yang cari mekanisme |

⚠️ **Jangan** pakai judul yang tak ditepati isi (mis. "Dokter Menyembunyikan Ini"). Kanal medis = kredibilitas adalah aset utama.

---

## 2. DESKRIPSI YOUTUBE (siap tempel)

```
Everyone says general anesthesia is like falling asleep. It is not.

When you sleep, your brain stays active — it cycles, it dreams, it listens. Under
general anesthesia, none of that happens. For about two hours, you do not exist.

This video follows the first ninety seconds of an induction, one mechanism at a
time: what the drug does to a single synapse, why a dose small enough to fit in a
tablespoon can suspend everything you are, and the part most people never hear —
that the same drug that removes your awareness also stops your breathing, drops
your blood pressure, and closes your airway. Keeping you alive through that is the
actual job.

CHAPTERS
00:00  Anesthesia is not sleep
00:22  Title
00:28  The holding area
01:35  Anesthesia — what the word actually means
02:10  The drug enters
03:00  Inside a single synapse
04:45  The arithmetic: one tablespoon
05:30  The turn: the drug is the thing trying to kill you
07:05  How they keep you alive
08:45  Coming back
09:50  Sign-off

—

This video is for education only and is not medical advice. All cases discussed are
drawn from published medical literature. Sources are listed below.

SOURCES
• Miller's Anesthesia (Gropper et al.) — intravenous induction agents, propofol
  pharmacology and dosing.
• Stoelting's Pharmacology & Physiology in Anesthetic Practice — propofol
  mechanism at the GABA-A receptor; chloride conductance.
• Herculano-Houzel S. "The human brain in numbers: a linearly scaled-up primate
  brain." Front Hum Neurosci. 2009 — the 86 billion neuron figure.
• Mashour GA, Hudetz AG. "Neural Correlates of Unconsciousness in Large-Scale
  Brain Networks." Trends Neurosci. 2018 — loss of consciousness as network
  disintegration.
• Standard airway management references for laryngoscopy and intubation.

Clinical figures in this video were reviewed by a practising anaesthesiologist.
Induction dose figures refer to healthy adults; doses differ in the elderly and
in higher-risk patients.

—

VITAL THRESHOLD
Every body has a threshold. This channel explores what happens when it is crossed
— the physiology of drowning, sepsis, cardiac arrest, anesthesia and organ failure
— told through documented medical cases and explained one mechanism at a time.

Take the pulse. Know the threshold.

Visuals in this video are AI-generated.
```

> **Cek sebelum tempel:** sesuaikan timestamp CHAPTERS dgn hasil rakit final (angka di atas dari shotlist). YouTube butuh chapter pertama `00:00` dan minimal 3 chapter.
>
> **Sitasi on-screen** tetap wajib muncul di **20 detik pertama** (checklist bible) — deskripsi saja tidak cukup.

---

## 3. TAG
Tempel di YouTube Studio (dipisah koma):
```
anesthesia, general anesthesia, what happens under anesthesia, propofol, anaesthesia,
how anesthesia works, medical animation, human body, physiology, intubation,
laryngoscope, apnea, hypotension, consciousness, neuroscience, operating room,
anesthesiologist, medical education, science explained, vital threshold
```

**Hashtag di deskripsi (maks 3, taruh paling atas atau bawah):**
`#anesthesia #physiology #medicine`

---

## 4. THUMBNAIL

### 4.1 Konsep terpilih
**Satu syringe berisi cairan putih, menyala mengancam dengan tepi merah arterial, di atas latar Abyss Teal gelap — dengan garis EKG Amber melintas horizontal sebagai pembatas.**

Alasannya:
- **Menepati janji judul** — syringe = "what actually happens", dan glow merah = pivot ("obat ini yang mencoba membunuhmu").
- **Patuh bible** (2.4): garis EKG sebagai pembatas thumbnail; palet terkunci; cahaya dari dalam.
- **Beda sendiri di feed.** Kompetitor medis pakai wajah kaget + panah merah. Kita gelap, sunyi, bercahaya dari dalam → justru menarik mata karena kontras dgn thumbnail lain yang ramai terang.
- Aset dasarnya **sudah ada**: still **S49** (syringe mengancam, hero klimaks).

### 4.2 Cara membuat (Gemini manual — lihat `prompt-pack-google.md`)
Upload **master style still** sbg reference, lalu prompt:
```
[BLOK A — MASTER STYLE, salin utuh dari prompt-pack-google.md]

Use the reference image ONLY as a style anchor — do NOT copy its objects.

SCENE (THUMBNAIL): a single bone-white syringe filled with milky white liquid,
centred slightly LEFT, glowing from within with an ominous arterial-red edge glow.
A thin amber EKG line runs horizontally across the frame behind it. The RIGHT
THIRD of the frame is deliberately left EMPTY and dark for a text overlay added
later. Dark abyss-teal void, high contrast, iconic and readable at small size.
Flat vector. No text, no numbers, no letters.
```
Rasio **16:9**, resolusi tertinggi. Simpan `VT-001-thumb-base.png`.

### 4.3 Teks di thumbnail (tempel di CapCut/Canva)
Font **Archivo Black**, HURUF BESAR, warna **Bone `#E6DCC8`**, taruh di **sepertiga kanan**:
```
NOT
SLEEP
```
Opsional baris ketiga kecil warna **Amber `#FFB23F`**: `90 SECONDS`

**Aturan thumbnail:**
- Maksimal **3 kata besar** — harus terbaca di layar ponsel sekecil kuku jempol.
- Jangan ulang judul; thumbnail **melengkapi** judul, bukan menyalinnya. (Judul bilang "what actually happens" → thumbnail menjawab sebagian: "NOT SLEEP".)
- Tanpa wajah, tanpa panah merah, tanpa lingkaran kuning. Bukan gaya kita.
- Uji: perkecil ke lebar 120px — masih terbaca & masih jelas apa objeknya?

### 4.4 Alternatif thumbnail (kalau mau A/B)
| # | Visual | Teks |
|---|---|---|
| B | Sendok makan vs siluet tubuh (still **S35**) | `ONE TABLESPOON` |
| C | Jari menyentuh bulu mata (still **S31**) | `THE TEST` |

Opsi B paling "shareable" (analogi skala absurd — elemen wajib bible), opsi C paling emosional.

---

## 5. Checklist upload (dari bible bagian 8)
- [ ] Sitasi sumber tampil **on-screen ≤20 detik pertama**
- [ ] Disclaimer ada di deskripsi ✅ (sudah di paket ini)
- [ ] **Centang "altered or synthetic content"** di YouTube Studio ← WAJIB
- [ ] Chapters disesuaikan dgn timecode final
- [ ] Subtitle EN + ID di-upload
- [ ] Tidak ada nama pasien ✅ (episode ini tanpa pasien spesifik)
- [ ] Thumbnail terbaca di 120px
- [ ] Judul & thumbnail **ditepati** isi video (click-promise)
