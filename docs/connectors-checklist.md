# Checklist Otorisasi Connector (Canva & Notion) + Aktivasi Skill

## Canva & Notion — cara authorize
Kedua connector ini butuh **otorisasi interaktif** (OAuth). Tidak bisa dilakukan dari sesi Claude Code remote — lakukan sendiri:

### Via claude.ai (connector bawaan)
- [ ] Buka **claude.ai** → **Settings → Connectors**.
- [ ] Cari **Canva** → klik **Connect** → login Canva → **Allow** akses.
- [ ] Cari **Notion** → klik **Connect** → login Notion → pilih workspace/halaman → **Allow**.
- [ ] Pastikan status keduanya **Connected**.

### Via Claude Code interaktif (jika pakai server MCP sendiri)
- [ ] Jalankan `/mcp` di Claude Code, atau
- [ ] `claude mcp` di terminal untuk menyelesaikan alur otorisasi.

> Catatan: Sesi non-interaktif (seperti sesi remote ini) **tidak bisa** menjalankan OAuth. Jangan pernah menempel token/kode otorisasi ke dalam chat.

### Untuk apa Canva & Notion di workflow ini?
- **Canva** — alternatif/penyempurnaan thumbnail & grafis (kalau ingin edit manual di luar Higgsfield).
- **Notion** — menyimpan kalender konten, daftar topik, status upload (mirip fungsi kontenIG tapi terpusat).

---

## Aktivasi Skill `ytfaceless` & `ytanestesi`

Kedua skill sudah ada di repo ini: `.claude/skills/ytfaceless/` dan `.claude/skills/ytanestesi/`.

- **Di sesi Claude Code pada repo ini:** otomatis aktif (skill di `.claude/skills/` repo terbaca).
- **Agar aktif di SEMUA sesi Anda** (di luar repo ini), salin ke skills global:

```bash
mkdir -p ~/.claude/skills
cp -r /path/ke/anesticu-privacy/.claude/skills/ytfaceless  ~/.claude/skills/
cp -r /path/ke/anesticu-privacy/.claude/skills/ytanestesi  ~/.claude/skills/
```

- [ ] Setelah disalin, buka sesi Claude Code baru.
- [ ] Ketik `/ytFaceless` atau `/ytAnestesi` untuk memicu skill.
- [ ] Atau minta natural: "buat channel YouTube AI edukasi kesehatan".

### Verifikasi
- [ ] Skill muncul saat mengetik `/` (daftar slash-command).
- [ ] Claude menyebut langkah-langkah dari SKILL.md saat dipanggil.
