# VITAL THRESHOLD — Production Bible v1.0

Dokumen referensi permanen. Buka setiap kali produksi. Jangan improvisasi di luar dokumen ini sampai ada 10 video terbit.

---

## 1. BRAND LOCK

| Item | Nilai |
|---|---|
| Nama channel | Vital Threshold |
| Handle | @vitalthreshold (YouTube, Instagram, TikTok) |
| Bahasa utama | English |
| Bahasa kedua | Subtitle Indonesia |
| Durasi long-form | 8–12 menit |
| Wajah dokter | Tidak ditampilkan |
| Tanda tangan penutup | "Take the pulse. Know the threshold." |

**Positioning (satu kalimat, hafalkan):**
The human body at the edge of survival, explained through real documented cases.

**Deskripsi channel (tempel di YouTube About):**
Every body has a threshold. This channel explores what happens when it is crossed — the physiology of drowning, sepsis, cardiac arrest, anesthesia and organ failure — told through documented medical cases and explained one mechanism at a time.

**Disclaimer wajib di setiap deskripsi video:**
This video is for education only and is not medical advice. All cases discussed are drawn from published medical literature. Sources are listed below.

---

## 2. STYLE GUIDE VISUAL

Logika inti: **interior, bukan kosmik.** Kita melihat tubuh dari dalam. Gelap, basah, bercahaya dari dalam. Referensi mental: bioluminesensi laut dalam, bukan luar angkasa.

### 2.1 Palet (kunci, jangan tambah warna)

| Peran | Nama | Hex |
|---|---|---|
| Dasar / latar | Abyss Teal | `#062A2E` |
| Dasar sekunder | Deep Teal | `#0E4249` |
| Bahaya / darah | Oxblood | `#7A1526` |
| Bahaya terang | Arterial | `#C42B3C` |
| Struktur / tulang | Bone | `#E6DCC8` |
| Aksen vital 1 | Amber Pulse | `#FFB23F` |
| Aksen vital 2 | Cyan Signal | `#35E0D8` |

Aturan: maksimal 5 warna per scene. Aksen (Amber/Cyan) hanya untuk elemen yang hidup atau vital. Jangan pernah memakai aksen sebagai latar.

### 2.2 Logika cahaya

Semua sumber cahaya berasal **dari dalam objek**, tidak pernah dari luar. Tidak ada matahari, tidak ada lampu, tidak ada gradasi latar seperti langit. Objek bercahaya sendiri; latar tetap gelap.

Ini adalah pembeda struktural terpenting dari channel edukasi lain. Jangan dilanggar.

### 2.3 Konstruksi bentuk

- Bentuk dasar: **kapsul dan persegi bulat**, bukan lingkaran sempurna.
- Setiap karakter punya **garis sambung (seam)** yang terlihat, memisahkan bagian organik dan mekanik.
- Outline tipis warna Bone pada karakter, tidak ada outline pada latar.
- Tanpa tekstur, tanpa gradient mesh. Flat vector murni dengan satu lapis inner glow.

### 2.4 Motif tanda tangan

**Garis EKG** warna Amber Pulse yang mengalir horizontal menembus scene. Dipakai sebagai:
- Transisi antar bab
- Pembatas di thumbnail
- Elemen intro dan outro
- Indikator ketegangan (garis menjadi kacau saat pasien memburuk, datar saat henti jantung)

Ini elemen paling sering muncul di channel. Perlakukan seperti logo.

### 2.5 Logika kedalaman

Setiap video bergerak satu arah: **ke dalam**. Tubuh → organ → jaringan → sel → molekul. Tidak pernah melompat keluar sampai bagian penutup. Konsistensi arah ini yang membuat penonton merasa berada di dunia yang sama tiap episode.

### 2.6 Tipografi

| Peran | Font | Catatan |
|---|---|---|
| Judul & thumbnail | Archivo Black | Gratis, Google Fonts. Huruf besar semua. |
| Angka & data on-screen | Archivo Black | Warna Amber Pulse |
| Subtitle | Inter Semibold | Gratis. Putih, outline gelap tipis. |
| Istilah medis on-screen | Inter Medium Italic | Warna Cyan Signal |

Jangan pakai lebih dari dua keluarga font.

---

## 3. MASTER STYLE PROMPT

Blok ini ditempel di **setiap** prompt gambar, tanpa diubah. Ini yang menjaga konsistensi.

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

FORMS: capsule and rounded-rectangle construction, visible seam lines
dividing organic and mechanical parts, thin bone-white outlines on
subjects only, flat fills with a single soft inner glow layer.
No gradient mesh, no texture, no noise.

COMPOSITION: centred subject, generous negative space, 16:9,
clean vector edges, no text in image.
```

**Cara pakai:** generate character sheet dulu (bagian 4), simpan hasil terbaik sebagai file referensi, lalu untuk semua gambar berikutnya gunakan gambar itu sebagai reference image ditambah master prompt. Tanpa reference image, konsistensi akan gagal.

---

## 4. CHARACTER SHEET PROMPTS

Generate keempatnya minggu ini. Untuk setiap karakter, hasilkan **satu lembar berisi 5 pose/ekspresi** sekaligus, agar gaya terkunci.

Simpan hasil final dengan nama file: `char-moni-master.png`, `char-cardio-master.png`, dst. File inilah aset paling berharga Anda.

### 4.1 MONI — pemandu

Paling sering muncul. Sengaja dibuat kaku agar mudah dianimasikan.

```
[MASTER STYLE PROMPT]

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: MONI. A small friendly patient-monitor robot.
Body: a rounded-rectangle screen unit in bone white with a visible
horizontal seam across the middle, standing on two short capsule legs,
two short capsule arms. Screen face occupies 70% of the front,
glowing softly from within in cyan.

The five variations show the screen face displaying:
1. neutral: a calm flat cyan waveform line
2. alert: an amber jagged waveform, screen tinted amber
3. alarm: a red chaotic waveform, screen tinted arterial red
4. flatline: a single flat cyan horizontal line, screen dimmed
5. explaining: a small rising bar chart in amber

No text, no numbers, no letters anywhere in the image.
```

### 4.2 CARDIO — jantung

Karakter paling ekspresif. Pembawa emosi.

```
[MASTER STYLE PROMPT]

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: CARDIO. A stylised heart character built from
capsule shapes in oxblood red with bone-white seam lines marking
the four chambers. Two large simple eyes in bone white.
Four short capsule vessel-stubs at the top acting as limbs.
Glows from within in amber, brightest at the centre.

The five variations show:
1. healthy: upright, steady, even amber glow
2. straining: leaning forward, glow pulsing brighter, sweat-drop shapes
3. failing: slumped, glow dimmed to faint amber, eyes half closed
4. fibrillating: body shape slightly distorted, glow flickering chaotically
5. recovering: upright again, glow returning, one eye open

No text, no numbers, no letters anywhere in the image.
```

### 4.3 ALVI — alveolus

Paling visual. Perubahan bentuknya menceritakan seluruh mekanisme.

```
[MASTER STYLE PROMPT]

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: ALVI. A small round alveolar sac character,
bone white, translucent, with a thin cyan capillary net wrapping
around its outer surface. Two small simple eyes. A single short
capsule airway stem at the top. Glows softly from within in cyan.

The five variations show:
1. healthy: fully inflated sphere, bright even cyan glow
2. collapsed: deflated and crumpled, glow nearly gone
3. flooded: half filled with a flat oxblood-red fluid level inside,
   glow muted and reddish
4. inflamed: swollen, outer wall thickened, arterial red edge glow
5. recruited: re-inflating, glow returning from the centre outward

No text, no numbers, no letters anywhere in the image.
```

### 4.4 BACTI — antagonis

Bukan jahat, hanya berkembang biak. Harus bisa digandakan menjadi kerumunan.

```
[MASTER STYLE PROMPT]

SUBJECT: character sheet, 5 variations in one image, evenly spaced
on dark teal background.

Character name: BACTI. A small rod-shaped bacterium character,
capsule body in deep teal with a darker seam line down its length,
short thin flagella tails, two tiny simple eyes set close together.
Glows faintly from within in sickly amber.

The five variations show:
1. single: one calm rod, faint glow
2. dividing: mid-fission, pinched in the middle
3. swarm: a tight cluster of eight identical rods
4. aggressive: elongated, glow shifted to arterial red, tails rigid
5. dying: shrunken and cracked, glow almost extinguished

No text, no numbers, no letters anywhere in the image.
```

---

## 5. STRUKTUR EPISODE (TERKUNCI)

Struktur ini tidak berubah antar video. Konsistensi format bukan risiko, itu yang membuat channel terasa seperti acara.

| Waktu | Bagian | Isi |
|---|---|---|
| 0:00–0:20 | **Cold open** | Bunuh satu miskonsepsi, atau presentasi pasien. Inisial, umur, keluhan masuk, bentuk waktu sekarang. Tanpa sapaan, tanpa intro. |
| 0:20–0:30 | **Title card** | Garis EKG + judul. Maksimal 6 detik. |
| 0:30–1:30 | **Latar manusia** | Dibuka dengan "You see, ..." Siapa orang ini sebelum jadi pasien. Penonton harus peduli sebelum fisiologi masuk. |
| 1:30–3:30 | **Eskalasi + etimologi** | Gejala memburuk bertahap. Setiap istilah medis dibelah akar katanya. Jangan menyederhanakan, belah. |
| 3:30–5:00 | **Mekanisme** | Turun ke dunia mikro. Maskot bekerja di sini. Arah selalu ke dalam. |
| 5:00–6:00 | **Aritmetika terbuka** | Hitung di depan penonton. Biarkan mereka sampai sendiri ke kesimpulan. Angka on-screen warna Amber. |
| 6:00–7:00 | **PIVOT** | Titik pembalikan. Sesuatu yang seharusnya menolong justru merusak, atau angka membaik tapi pasien memburuk. Ini jantung video. |
| 7:00–9:00 | **Resolusi** | Apa yang terjadi selanjutnya. Jujur, termasuk bila hasilnya buruk. |
| 9:00–10:00 | **Zoom out** | Satu analogi skala absurd + tempat mendarat bagi penonton. Pertanyaan, bukan ringkasan. |
| Penutup | **Sign-off** | "Take the pulse. Know the threshold." |

### Aturan naskah

1. **Satu pertanyaan besar per video**, bukan satu topik.
2. **Kasus dari literatur terpublikasi**, dengan sitasi ditampilkan on-screen di detik pertama. Bukan pasien nyata dari bangsal.
3. **Inisial dua huruf** untuk pasien. Tidak pernah nama.
4. **Etimologi minimal 3 kali** per video.
5. **Satu analogi skala absurd** per video, wajib, itu yang diingat dan dibagikan orang.
6. **Tidak ada permintaan subscribe** di awal atau tengah. Hanya di akhir, satu kalimat.

---

## 6. PIPELINE PRODUKSI

1. **Riset** — cari laporan kasus terpublikasi. Catat sitasi lengkap.
2. **Naskah** — tulis penuh mengikuti tabel bagian 5. Hitung durasi: 150 kata per menit.
3. **Shot list** — pecah naskah menjadi scene, satu gambar per 8–12 detik narasi.
4. **Ilustrasi** — generate still image, master prompt + reference character sheet.
5. **Gerakan halus** — image-to-video, prompt gerakan minimal saja (denyut, partikel melayang, cairan mengalir). Klip 5 detik.
6. **Narasi** — ElevenLabs, satu voice terkunci selamanya.
7. **Rakit** — CapCut. Gerakan kamera, elemen masuk, angka naik, transisi EKG.
8. **Subtitle** — English dari naskah, Indonesia dari terjemahan naskah.
9. **Upload** — centang disclosure "altered or synthetic content" di YouTube Studio. Wajib.
10. **Potong Shorts** — ambil 2–3 momen dari video, 20–45 detik.

### Ritme bulanan

| Tanggal | Aktivitas |
|---|---|
| 1–15 (kerja klinis) | Riset dan penulisan naskah saja. 45 menit per hari. |
| 16–30 (libur) | Produksi visual, perakitan, batch semua video bulan berikutnya. |
| Sepanjang bulan | Rilis terjadwal otomatis. Tidak ada produksi mendadak. |

---

## 7. DAFTAR 10 VIDEO PERTAMA

1. What Actually Happens When You Are Put Under Anesthesia
2. What Happens To Your Body In The Last 10 Minutes Of Cardiac Arrest
3. What Happens To Your Body When You Drown
4. Sepsis: How An Infection Kills You In 12 Hours
5. What A Ventilator Actually Does To Your Lungs
6. Can You Be Awake During Surgery And Not Know It?
7. What Happens To Your Brain In A Coma
8. Why Your Body Kills You Trying To Save You
9. What Happens To Your Body When You Bleed Out
10. The Machine That Replaces Your Heart And Lungs

---

## 8. CHECKLIST SEBELUM UPLOAD

- [ ] Sitasi sumber tampil on-screen di 20 detik pertama
- [ ] Disclaimer ada di deskripsi
- [ ] Disclosure konten sintetis dicentang di YouTube Studio
- [ ] Tidak ada nama pasien, hanya inisial
- [ ] Minimal 3 etimologi istilah
- [ ] Ada satu analogi skala absurd
- [ ] Titik pivot jelas dan ada di paruh kedua
- [ ] Palet tidak keluar dari 7 warna terkunci
- [ ] Subtitle English dan Indonesia terpasang
- [ ] Sign-off terucap
