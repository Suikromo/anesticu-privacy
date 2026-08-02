# HANDOFF — Proyek Konten AI (Vital Threshold + Skills)

Dokumen serah-terima. **Tempel isi bagian "CARA LANJUT" ke chat/sesi baru mana pun** untuk melanjutkan tanpa kehilangan konteks. Semua kerja tersimpan di git.

- **Repo:** `Suikromo/anesticu-privacy`
- **Branch kerja:** `claude/youtube-video-learning-wgjcmq` ← SEMUA file ada di sini (BUKAN di `main`, BUKAN di repo `anesticu_pro`)
- **Terakhir diperbarui:** 2026-08-01

---

## 🚀 CARA LANJUT (tempel ini ke sesi baru)

> Repo `anesticu-privacy`, semua file ada di branch `claude/youtube-video-learning-wgjcmq`. Jalankan dulu:
> ```
> git fetch origin claude/youtube-video-learning-wgjcmq
> git checkout claude/youtube-video-learning-wgjcmq
> ```
> (Kalau clone-nya shallow / file kurang: `git fetch --unshallow origin` lalu checkout lagi.)
> Lalu baca `HANDOFF.md` dan `.claude/skills/ytanestesi/references/workplan.md` untuk status terkini, dan lanjutkan langkah berikutnya.

---

## 📋 APA YANG SUDAH DIBANGUN

Berawal dari mempelajari 1 video YouTube (workflow bikin channel faceless AI pakai Claude + Higgsfield MCP), berkembang jadi:

1. **2 skill produksi konten** (di `.claude/skills/`).
2. **Playbook DNA Bright Side** (analisis hook/copywriting).
3. **Channel "Vital Threshold"** — dokumenter edukasi anestesi/ICU. **VT-001 lengkap asetnya:** Production Bible, Retention DNA, naskah (angka klinis terverifikasi dokter), shot list 64 shot, 3 character sheet, 48 still, ~46 klip motion, narasi 10 scene (voice Cillian terkunci), panduan rakit, packaging YouTube. Sisa: rakit di CapCut + upload.
4. **Setup Higgsfield** (CLI + companion skills) + dokumentasi.

---

## 🗺️ PETA REPO (file penting)

```
HANDOFF.md                          ← dokumen ini
docs/
  brightside-playbook.md            ← analisis DNA/hook/copywriting Bright Side (2 format)
  setup-higgsfield-mcp.md           ← panduan pasang Higgsfield MCP connector
  connectors-checklist.md           ← checklist Canva/Notion + aktivasi skill
.claude/skills/
  ytfaceless/SKILL.md               ← skill generik: channel faceless AI (dari video)
  ytanestesi/
    SKILL.md                        ← skill operasional channel VITAL THRESHOLD
    references/
      production-bible.md           ← OTORITAS: brand, gaya visual, struktur, etika
      VT-001-script.md              ← naskah episode 1 (Anesthesia) — bible-compliant
      VT-001-shotlist.md            ← 64 shot, padat di PIVOT, tanda REUSE
      VT-001-renders.md             ← log SEMUA job ID (still, motion, narasi)
      character-sheet-prompts.md    ← 3 prompt sumber (MONI/CARDIO/ALVI)
      retention-dna.md              ← lapisan hook/retensi (Bright Side disaring lewat bible)
      VT-001-assembly.md            ← panduan rakit CapCut (VO→shot, teks, audio, checklist)
      VT-001-packaging.md           ← judul, deskripsi, tag, konsep+prompt thumbnail
      VT-001-rename-map.md          ← job ID → nama file final (104 aset)
      prompt-pack-google.md         ← prompt manual utk Gemini/Flow (pengganti Higgsfield)
      char-moni-master.png          ← ✅ character sheet MONI (2000×1116, 5 pose)
      char-cardio-master.png        ← ✅ character sheet CARDIO
      char-alvi-master.png          ← ✅ character sheet ALVI
      workplan.md                   ← STATUS HIDUP produksi (baca ini tiap mulai)
.agents/skills/ (di-gitignore)      ← 7 companion skill Higgsfield (install ulang bila perlu)
```

---

## 🧩 INVENTARIS SKILL

### Skill buatan kita (ada di repo, versioned)
| Skill | Trigger | Fungsi |
|---|---|---|
| `ytfaceless` | `/ytFaceless`, "channel YouTube AI" | Panduan generik bikin channel faceless AI bermonetisasi |
| `ytanestesi` | `/ytAnestesi`, "video Vital Threshold" | Operasional channel Vital Threshold (terkunci ke Production Bible) |

### Companion skill Higgsfield (di-gitignore; install ulang: `npx skills add higgsfield-ai/skills`)
`higgsfield-generate` (image/video/audio/3D) · `higgsfield-video-explainer` · `higgsfield-soul-id` · `higgsfield-product-photoshoot` · `higgsfield-marketplace-cards` · `higgsfield-game-generation` · `higgsfield-websites`

---

## ✅ STATUS & BLOCKER

**Selesai (VT-001 — SEMUA ASET PRODUKSI BERES):** Production Bible ✅ · Retention DNA ✅ · Naskah + **verifikasi angka klinis oleh dokter** ✅ · Shot list 64 shot ✅ · 3 character sheet ✅ (ter-commit) · **48 still** ✅ · **~46 klip motion** ✅ · **narasi 10 scene** ✅ (voice **Cillian** TERKUNCI selamanya) · panduan rakit `VT-001-assembly.md` ✅ · packaging judul/deskripsi/tag/thumbnail `VT-001-packaging.md` ✅ · peta rename aset `VT-001-rename-map.md` ✅

**Sedang jalan:** memindahkan 104 file aset dari akun Higgsfield → Google Drive (manual oleh user, lihat blocker jaringan di bawah).

**Belum:** rakit di CapCut → subtitle EN/ID → upload (disclosure sintetis) → Shorts → VT-002.

**Kredit Higgsfield: HABIS (1 Agu 2026).** Tidak menghambat VT-001 (semua aset sudah jadi). Jalur pengganti yang dipilih user: **generate manual di Google Gemini/Flow** dgn langganan Google AI Pro → `references/prompt-pack-google.md`. Catatan: `nano_banana_pro` **memang model Google** (= Gemini 3 Pro Image), jadi pindah ke Google tidak merusak konsistensi gaya.

---

### 🔒 BLOKIR JARINGAN — akar masalah & solusi (PENTING, jangan diulang)

**Gejala:** `curl` ke `d8j0ntlcm91z4.cloudfront.net` (CDN Higgsfield) selalu gagal — `000` / `connect_rejected` / HTTP 403 di CONNECT. Sudah dites berkali-kali sepanjang proyek.

**Akar masalah:** semua egress dari container lewat **proxy penegak kebijakan**. Host yang tidak ada di allowlist ditolak di level CONNECT. Ini **konfigurasi statis** yang dipilih saat environment dibuat — bukan gangguan sementara, bukan rate-limit, bukan soal kredit. **Retry berapa kali pun hasilnya sama.** Aturan proxy: jangan retry, jangan akali, laporkan.

**Kenapa sebagian jalan, sebagian tidak** (ini yang sering membingungkan):
| Jalur | Lewat | Hasil |
|---|---|---|
| `curl`/`git` dari shell | proxy egress environment | hanya host allowlist: `github.com`, pypi/npm, `generativelanguage.googleapis.com` |
| Tool MCP (Drive, Gmail, Higgsfield) | **server MCP di luar container** | ✅ selalu jalan, tidak kena policy |

→ Karena itu Claude **bisa** membuat folder & file di Google Drive, tapi **tidak bisa** mengunduh satu PNG pun dari CDN. Bisa menaruh di tujuan, tidak bisa mengambil dari sumber.

**Akibat nyata:** 104 file aset (48 still + 46 klip + 10 narasi) **hanya ada di akun Higgsfield**, tidak pernah bisa masuk repo. Yang ada di repo cuma **job ID + peta rename**. 3 character sheet bisa masuk repo hanya karena user paste gambarnya ke chat lalu di-decode dari attachment.

**Solusi (urutan yang disepakati user):**
1. **[2] Download manual** dari gallery Higgsfield → rename pakai `VT-001-rename-map.md` → upload ke Google Drive. ← sedang dikerjakan
2. **[1] Environment baru dgn network policy longgar** (izinkan egress luas / tambah `*.cloudfront.net`). Ini solusi permanen. ⚠️ Perubahan policy **tidak berlaku pada sesi berjalan** — wajib environment/sesi baru. Dok: `code.claude.com/docs/en/claude-code-on-the-web`
3. **[3] Claude Code lokal** di komputer user — tanpa proxy, akses penuh.

**Blokir lain yang sudah terbukti:**
- `clerk.higgsfield.ai` (OAuth CLI Higgsfield) → diblok. CLI tak terpakai, gunakan MCP.
- `aistudio.google.com`, `labs.google` (Flow) → diblok. Web UI tidak bisa diotomasi Claude; generate Google = kerja manual user.
- `generativelanguage.googleapis.com` → **TEMBUS** ✅. Kalau nanti user menyediakan API key Google AI Studio (billing terpisah dari langganan Pro), otomatisasi penuh **mungkin** dilakukan lewat skrip. Jangan tempel key di chat — pasang sebagai environment variable.
- **Canva & Notion:** perlu otorisasi interaktif user (opsional, belum dipakai).

### 📦 Di mana aset berada
| Aset | Lokasi | Aman? |
|---|---|---|
| Naskah, bible, panduan, prompt, peta | repo git | ✅ permanen |
| 3 character sheet PNG | repo git (`references/`) | ✅ permanen |
| 48 still · 46 klip · 10 narasi | **akun Higgsfield** → dipindah ke **Google Drive** | ⚠️ sedang diamankan |

Google Drive tujuan: folder **V1 1/8/26** (`1p4fgdR7aUiG5qM5UohWy4XjMh4IjYP74`) — sudah berisi subfolder `stills/`, `clips/`, `vo/` + dokumen peta rename.

> **Jangan commit video/still ke git.** GitHub batas 100MB/file & histori git membengkak permanen. Git = teks + character sheet. Drive/disk = media.

---

## ▶️ LANGKAH BERIKUTNYA (urut)

**SEDANG BERJALAN — amankan aset (user, manual):**
1. Download 104 file dari gallery Higgsfield.
2. Rename pakai **`references/VT-001-rename-map.md`** (job ID → nama final). ⚠️ Jangan rename manual tanpa peta ini — nama file Higgsfield acak dan mudah tertukar.
3. Upload ke Drive **V1 1/8/26** → `stills/` · `clips/` · `vo/`.
4. Ambil 3 character sheet dari repo (`.claude/skills/ytanestesi/references/char-*-master.png`) → taruh di `stills/`.
5. Kabari Claude → Claude **audit isi Drive** (punya akses baca) untuk memastikan 104 file lengkap & namanya benar.

**Setelah aset aman:**
6. **Rakit di CapCut** ikuti `references/VT-001-assembly.md` (narasi dulu, gambar belakangan; peta VO→shot; teks overlay; desain audio pulse-ox).
7. **Subtitle EN** (salin dari naskah) **+ ID** (terjemahan).
8. **Thumbnail:** generate di Gemini pakai prompt di `references/VT-001-packaging.md` bagian 4.
9. **Upload** pakai judul/deskripsi/tag di `VT-001-packaging.md` → ⚠️ **centang disclosure "altered or synthetic content"** (WAJIB).
10. Potong **2–3 Shorts** (kandidat ada di assembly guide bagian 8).

**Setelah VT-001 tayang:**
11. Pindah ke **environment dgn network policy longgar** (solusi #1 di blokir jaringan) supaya episode berikutnya tidak kena hambatan yang sama.
12. **VT-002 (Cardiac arrest)** — semua aset gaya & voice sudah terkunci, jadi jauh lebih cepat. Naskah bisa ditulis kapan saja tanpa kredit.

---

## 🔑 KEPUTUSAN & FAKTA KUNCI (jangan lupa)
- **Vital Threshold** = faceless, dokumenter fisiologi "tubuh di ambang bertahan hidup". Sign-off: *"Take the pulse. Know the threshold."*
- **Etika medis (wajib):** kasus dari literatur terpublikasi, inisial 2 huruf, disclaimer tiap video, disclosure konten sintetis, edukasi BUKAN nasihat personal. Angka klinis diverifikasi dokter (user), bukan dikarang.
- **Gaya visual terkunci:** flat vector 2D, palet 7 warna (maks 5/scene), cahaya dari DALAM objek (bioluminesensi), motif garis EKG Amber. Jangan improvisasi sampai 10 video terbit.
- **Hemat kredit:** target ~40–50 generate unik/episode; sisanya reuse + layer assembly (lihat tanda REUSE di shot list).
- **Git:** commit & push tiap progres ke branch `claude/youtube-video-learning-wgjcmq`. Jangan tumpuk di `main`.
