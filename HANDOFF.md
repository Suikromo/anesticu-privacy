# HANDOFF — Proyek Konten AI (Vital Threshold + Skills)

Dokumen serah-terima. **Tempel isi bagian "CARA LANJUT" ke chat/sesi baru mana pun** untuk melanjutkan tanpa kehilangan konteks. Semua kerja tersimpan di git.

- **Repo:** `Suikromo/anesticu-privacy`
- **Branch kerja:** `claude/youtube-video-learning-wgjcmq` ← SEMUA file ada di sini (BUKAN di `main`, BUKAN di repo `anesticu_pro`)
- **Terakhir diperbarui:** 2026-07-31

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
3. **Channel "Vital Threshold"** — dokumenter edukasi anestesi/ICU: Production Bible, Retention DNA, naskah episode 1, shot list 64 shot, **3 character sheet (MONI/CARDIO/ALVI) sudah ter-generate**, dan batch 1 still (9 shot) berjalan.
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
      VT-001-renders.md             ← log render still (batch 1: 9 shot CHAR)
      character-sheet-prompts.md    ← 3 prompt sumber (MONI/CARDIO/ALVI)
      retention-dna.md              ← lapisan hook/retensi (Bright Side disaring lewat bible)
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

**Selesai:** Production Bible ✅ · Retention DNA ✅ · Naskah VT-001 ✅ · Shot list VT-001 (64 shot) ✅ · **3 character sheet (MONI/CARDIO/ALVI) ter-generate & ter-commit ✅** · Higgsfield CLI ter-install ✅

**Sedang jalan:** ilustrasi still VT-001 — **batch 1 = 9 shot CHAR** sudah ter-generate (Nano Banana Pro, reference sheet terkunci), nunggu review konsistensi. Sisa: **36 NEW + 3 TPL**. Detail: `references/VT-001-renders.md`.

**Belum:** sisa still → motion (image-to-video) → narasi → rakit + subtitle → upload → Shorts. (lihat `workplan.md`)

**Kredit Higgsfield:** sudah di-upgrade user (bukan 0). Character sheet berhasil dibuat, jadi jalur MCP terbukti bisa.

**Catatan koneksi (sesi remote):**
- MCP `mcp__Higgs__*` kadang naik-turun saat container restart; kalau hilang, cek ulang lewat ToolSearch atau buka sesi baru.
- CLI `higgsfield` tak terpakai: host `clerk.higgsfield.ai` (token OAuth) **diblok egress** → auth CLI gagal. Pakai MCP saja.
- Download master full-res dari CDN Higgsfield (`d8j0ntlcm91z4.cloudfront.net/...`) **diblok egress** di sesi ini. PNG yang di-commit adalah versi yang di-decode dari attachment chat (2000×1116, sudah cukup untuk referensi). Master 2752×1536 tersimpan di akun Higgsfield (Job ID di `workplan.md`).
- **Canva & Notion:** perlu otorisasi interaktif user (opsional, belum dipakai).

---

## ▶️ LANGKAH BERIKUTNYA (urut)
1. Pastikan `mcp__Higgs__*` aktif (cek `mcp__Higgs__balance`).
2. **Review 9 shot CHAR batch 1** (`VT-001-renders.md`) — cek konsistensi karakter/palet/glow. Regenerate yang meleset.
3. **Generate sisa still VT-001:** 36 NEW + 3 TPL, ikuti `VT-001-shotlist.md` (master prompt + reference sheet char-*-master.png yang sudah terkunci). Terapkan tanda REUSE untuk hemat kredit.
4. Update `workplan.md` tiap batch selesai.
5. **Motion:** image-to-video per still, gerak minimal (denyut/partikel/cairan), klip 5 dtk.
6. **Narasi:** verifikasi angka klinis dulu (lihat Catatan Produksi di naskah) → generate voice terkunci.
7. **Rakit + subtitle EN/ID + desain audio** (pulse-ox pitch = elemen kunci) → **upload** (centang disclosure "altered/synthetic content") → potong 2–3 **Shorts**.

---

## 🔑 KEPUTUSAN & FAKTA KUNCI (jangan lupa)
- **Vital Threshold** = faceless, dokumenter fisiologi "tubuh di ambang bertahan hidup". Sign-off: *"Take the pulse. Know the threshold."*
- **Etika medis (wajib):** kasus dari literatur terpublikasi, inisial 2 huruf, disclaimer tiap video, disclosure konten sintetis, edukasi BUKAN nasihat personal. Angka klinis diverifikasi dokter (user), bukan dikarang.
- **Gaya visual terkunci:** flat vector 2D, palet 7 warna (maks 5/scene), cahaya dari DALAM objek (bioluminesensi), motif garis EKG Amber. Jangan improvisasi sampai 10 video terbit.
- **Hemat kredit:** target ~40–50 generate unik/episode; sisanya reuse + layer assembly (lihat tanda REUSE di shot list).
- **Git:** commit & push tiap progres ke branch `claude/youtube-video-learning-wgjcmq`. Jangan tumpuk di `main`.
