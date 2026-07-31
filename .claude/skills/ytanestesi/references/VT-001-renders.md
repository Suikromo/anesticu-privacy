# VT-001 — Render Manifest

Catatan hasil generate still image VT-001 di Higgsfield. Sumber shot = `VT-001-shotlist.md`, gaya = `production-bible.md` bagian 3, karakter dikunci dari `char-*-master.png`.

_Terakhir diperbarui: 2026-07-31_

## Cara pakai
- Semua render lahir di akun Higgsfield (tersimpan permanen, job ID di bawah). URL PNG penuh ada di kolom URL — host `d8j0ntlcm91z4.cloudfront.net` **diblok egress di sesi ini**, jadi PNG belum bisa ditarik otomatis ke repo dari sini. Tarik dari environment tanpa restriksi egress, atau download manual dari akun.
- Model produksi: **Nano Banana Pro** (`model: nano_banana_pro`, internal `nano_banana_2`), 16:9, resolusi 2k (2752×1536). Sama dengan model character sheet → gaya konsisten.
- Setiap shot CHAR memakai character sheet sebagai **reference image** (image-to-image), dikunci lewat job ID sheet.
- Prefix URL: `https://d8j0ntlcm91z4.cloudfront.net/user_3HGLmxg8ehmKtoLNSzMjqzKQ0Ec/`

## Reference sheet (master, terkunci)
| Karakter | Sheet job ID | File repo |
|---|---|---|
| MONI | `f3357d4e-4216-4347-b0a7-43401bfce947` | `char-moni-master.png` |
| CARDIO | `420f332c-8f45-49bc-8e97-1b2f495a58e4` | `char-cardio-master.png` |
| ALVI | `0d99e267-b395-463c-825d-b2815af012c3` | `char-alvi-master.png` |

## Master style still (jangkar gaya untuk shot NEW)
Establishing ruang operasi bergaya bible, TANPA maskot — dipakai sbg reference image untuk 36 shot NEW biar seragam.
| Aset | Render job ID | URL |
|---|---|---|
| Master style still (OR interior) | `323c14a0-cb24-47b3-b523-2938959a7547` | _(rendering — URL menyusul)_ |

## Batch 1 — 9 shot CHAR (maskot, reference terkunci)
| Shot | Karakter / state | Ref sheet | Render job ID | URL PNG (prefix di atas + nama file) |
|---|---|---|---|---|
| S07 | MONI neutral (samping brankar) | MONI | `eee8d164-6afe-414d-a334-48feab601248` | `hf_20260731_155134_eee8d164-6afe-414d-a334-48feab601248.png` |
| S17 | CARDIO healthy (memompa) | CARDIO | `76faa8a3-597a-4890-ada2-e0dd8a87dade` | `hf_20260731_155139_76faa8a3-597a-4890-ada2-e0dd8a87dade.png` |
| S37 | ALVI healthy (mengembang) | ALVI | `f36de1dd-db87-43a6-a4d2-4c9a87186320` | `hf_20260731_155145_f36de1dd-db87-43a6-a4d2-4c9a87186320.png` |
| S39 | ALVI collapsed (kempis) | ALVI | `75f5b48e-5507-4665-8398-393eef7367c3` | `hf_20260731_155150_75f5b48e-5507-4665-8398-393eef7367c3.png` |
| S41 | CARDIO straining (condong, sweat) | CARDIO | `5ef13ffd-6f12-431a-8ee2-69dcff007b84` | `hf_20260731_155156_5ef13ffd-6f12-431a-8ee2-69dcff007b84.png` |
| S44 | MONI alert (amber jagged) | MONI | `5ce513e3-f7e1-4472-b8eb-cbbd73dc8254` | `hf_20260731_155203_5ce513e3-f7e1-4472-b8eb-cbbd73dc8254.png` |
| S46 | MONI alarm (merah kacau) | MONI | `64b5fbed-cc1c-44a0-8ee1-7bf8c3c7ab06` | `hf_20260731_155206_64b5fbed-cc1c-44a0-8ee1-7bf8c3c7ab06.png` |
| S47 | CARDIO failing (merosot, redup) | CARDIO | `f85825bf-1414-4cf4-adf2-0ee551cb2add` | `hf_20260731_155210_f85825bf-1414-4cf4-adf2-0ee551cb2add.png` |
| S55 | ALVI recruited (re-inflate mekanis) | ALVI | `637dfe3b-eb10-4435-af70-e1b548753b20` | `hf_20260731_155214_637dfe3b-eb10-4435-af70-e1b548753b20.png` |

**Status batch 1:** ⏳ menunggu review konsistensi user (belum di-approve). Model = Nano Banana Pro, reference sheet terkunci.

> Catatan: batch pertama sempat ter-generate di Nano Banana 2 (flash) karena salah alias model, lalu di-ulang di Nano Banana Pro (tabel di atas = versi Pro, ini yang dipakai). Job flash diabaikan.

## Belum di-generate (menunggu approval batch 1)
- **36 shot NEW** (S02, S03, S06, S08, S10, S11, S13, S14, S15, S16, S18, S19, S20, S22, S23, S24, S25, S27, S30, S31, S32, S35, S40, S42, S43, S45, S48, S49, S50, S51, S52, S53, S54, S58, S62 — cek shotlist untuk detail; sebagian butuh anchor gaya karena tanpa maskot).
- **3 TPL** (S01 EKG-line, S05 title-card, S12/S64 pola) — basis visual saja; teks/tipografi ditambah saat assembly (CapCut).
- **16 REUSE** — tidak di-generate (layer assembly dari frame yang sudah ada).
