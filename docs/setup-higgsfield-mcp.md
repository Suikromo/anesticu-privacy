# Panduan Setup Higgsfield MCP di Claude

Panduan super-detail memasang **Higgsfield MCP** sebagai custom connector di Claude, supaya bisa dipakai bersama skill `ytfaceless` / `ytanestesi`.

> **Penting:** Pemasangan connector = proses **OAuth interaktif** yang harus dilakukan sendiri di aplikasi Claude Anda (Desktop/Web). Sesi Claude Code remote tidak bisa menjalankan login OAuth untuk Anda. Ikuti langkah di bawah secara manual.

---

## A. Buat akun & ambil URL MCP di Higgsfield
1. Buka browser → kunjungi situs **Higgsfield AI** (cari "Higgsfield AI").
2. **Sign up / Log in** (Google atau email). Selesaikan verifikasi bila diminta.
3. Di dashboard, cari menu **"MCP and CLI"** (biasanya di Settings / Developer / Integrations).
4. Pilih opsi **MCP**. Akan muncul:
   - sebuah **URL connector** (mis. `https://mcp.higgsfield.ai/...`), dan/atau
   - sebuah **perintah instalasi CLI**.
5. **Copy URL** tersebut (dan/atau API key bila ditampilkan). Simpan sementara di tempat aman — **jangan** bagikan ke siapa pun / jangan tempel di chat publik.

## B. Tambahkan sebagai Custom Connector di Claude
1. Buka **Claude** (Desktop app atau claude.ai).
2. Masuk **Settings → Connectors** (di beberapa versi: *Settings → Integrations*).
3. Klik **Add custom connector** (atau **Add MCP server**).
4. Isi:
   - **Name:** `Higgsfield`
   - **URL:** tempel URL dari langkah A.4
   - (bila diminta) tempel **API key / token**.
5. Klik **Connect / Add**. Jika muncul jendela **OAuth**, izinkan akses → selesaikan login Higgsfield.
6. Status connector harus berubah menjadi **Connected / Enabled**.

## C. Pakai di Claude Code
1. Buka **Claude Code** (CLI/IDE/web).
2. Cek MCP aktif: jalankan `/mcp` — pastikan **Higgsfield** terdaftar dan tools `mcp__higgsfield__*` (atau serupa) tersedia.
3. Mulai workflow dengan skill: ketik `/ytFaceless` atau `/ytAnestesi`, atau langsung minta: "buat channel YouTube AI edukasi kesehatan".

---

## Verifikasi cepat
- Di Claude, tanya: **"Tools MCP apa saja yang aktif?"** — harus menyebut Higgsfield.
- Coba prompt kecil: **"Higgsfield, generate 1 gambar tes 16:9."** Jika keluar hasil → koneksi OK.

## Troubleshooting
| Masalah | Penyebab umum | Solusi |
|---|---|---|
| Connector tidak muncul | Salah menu | Cari di Settings → Connectors **atau** Integrations, tergantung versi Claude |
| Status "Failed to connect" | URL/API key salah/expired | Ambil ulang dari Higgsfield → MCP and CLI, tempel baru |
| OAuth window tidak muncul | Popup diblokir | Izinkan popup untuk claude.ai, ulangi Add connector |
| `/mcp` tak menampilkan Higgsfield | Belum tersimpan / sesi lama | Restart Claude Code, buka sesi baru |
| Generate gagal / kuota | Paket Higgsfield habis | Cek billing/kuota di dashboard Higgsfield |
| Tools tak terpakai otomatis | Model tak diberi konteks | Sebut eksplisit "pakai Higgsfield MCP" di prompt |

## Keamanan
- Perlakukan URL MCP & API key seperti password. Jangan commit ke Git, jangan kirim ke chat publik.
- Bila bocor: **revoke/rotate** key di dashboard Higgsfield, lalu pasang ulang connector.
