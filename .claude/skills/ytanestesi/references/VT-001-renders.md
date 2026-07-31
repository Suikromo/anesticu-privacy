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
| Master style still (OR interior) | `323c14a0-cb24-47b3-b523-2938959a7547` | `hf_20260731_162131_323c14a0-cb24-47b3-b523-2938959a7547.png` |

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

## Batch 2 · Wave 1 — 10 shot NEW/TPL (anchor: master style still `323c14a0`)
Gerbang verifikasi: uji apakah reference style-still mengontaminasi shot mikro. Prefix URL sama seperti di atas.
| Shot | Isi | Render job ID | Nama file PNG |
|---|---|---|---|
| S01 (TPL) | EKG-line plate | `7c07f78f-a936-423e-9f6f-314dace8d3d9` | `hf_20260731_234006_7c07f78f-a936-423e-9f6f-314dace8d3d9.png` |
| S02 | Orang tidur (glow cyan) | `84fde688-2827-481b-ac7e-7eb44d8a3564` | `hf_20260731_234016_84fde688-2827-481b-ac7e-7eb44d8a3564.png` |
| S06 | Establishing holding area | `5da3a719-d22c-40de-b3f3-7323a1f2a6fc` | `hf_20260731_234019_5da3a719-d22c-40de-b3f3-7323a1f2a6fc.png` |
| S08 | Kanula IV di punggung tangan | `e9a86da7-510c-492f-b6b5-a8a3d41e2164` | `hf_20260731_234022_e9a86da7-510c-492f-b6b5-a8a3d41e2164.png` |
| S13 | Etymology divider (garis EKG) | `9e1dd1e9-7169-4c93-99bd-abbbff8c9f67` | `hf_20260731_234025_9e1dd1e9-7169-4c93-99bd-abbbff8c9f67.png` |
| S14 | 3 ikon (feel/remember/aware) | `2125127c-6ca1-480b-940d-21f17033b8c6` | `hf_20260731_234027_2125127c-6ca1-480b-940d-21f17033b8c6.png` |
| S20 (hero) | Jaringan neuron | `d997441b-ab65-437d-835f-50dcc26b76a2` | `hf_20260731_234031_d997441b-ab65-437d-835f-50dcc26b76a2.png` |
| S23 (hero) | Sinaps (celah) | `86e4ca9a-af39-4b1b-acd1-cc3b00863fb8` | `hf_20260731_234033_86e4ca9a-af39-4b1b-acd1-cc3b00863fb8.png` |
| S24 | Reseptor + gate tertutup | `6f7c2eb2-8e9f-4e00-803f-1c6566b1501a` | `hf_20260731_234036_6f7c2eb2-8e9f-4e00-803f-1c6566b1501a.png` |
| S27 | Klorida masuk sel | `f59ced4c-6b14-40a5-8c6f-34e6e407e896` | `hf_20260731_234039_f59ced4c-6b14-40a5-8c6f-34e6e407e896.png` |

**Status Wave 1:** ⏳ menunggu verifikasi user (khusus: shot mikro S20/S23/S24/S27 — apakah gaya konsisten tanpa ketularan meja-OR dari style still).

## Batch 2 · Wave 2 — 14 shot NEW/TPL (anchor: style still `323c14a0`)
URL tiap job = pola `hf_YYYYMMDD_HHMMSS_<jobid>.png` di prefix yg sama; ambil via `job_display`/gallery (CDN egress-blocked di sesi ini).
| Shot | Isi | Render job ID |
|---|---|---|
| S03 | Orang di meja OR, glow padam, EKG hidup | `a5e251fa-5d70-403d-9e3c-f9ea69f1c6e9` |
| S05 (TPL) | Title-card bg (EKG sweep) | `fcbb2c0b-b4af-4e82-9ca7-0f919960be46` |
| S10 | Tangan menutup pergelangan | `be7063f8-5d87-4ac5-a180-973f963a2fcc` |
| S11 | Wajah pasien menghitung | `47eaf70a-0420-4f9d-a00b-7fb100557495` |
| S12 (TPL) | Etymology/sign-off plate | `e68b8bdb-6f9a-4b5d-a991-681abfd6770b` (regen; ganti `601503ee…`) |
| S15 | Cairan susu masuk kanula | `bab5d274-c22d-4425-9a1c-caed2d459f14` |
| S16 | Aliran cairan lengan→bahu | `b71d2288-57d5-40fe-bafe-ce8ffea868cf` |
| S18 | Cairan menyebar ke kepala | `aaf1e23b-0c6d-4a77-9c0f-90324c3a8b16` |
| S19 | Siluet tubuh + jalur menyala | `d8f1368e-1ec0-4acc-ae01-be15f51539d3` |
| S22 | Garis info antar-otak | `12abc3c6-1e5f-44b7-9814-50eccc01d5bd` |
| S25 | Propofol menempel reseptor | `803b8554-2f1c-4a53-9628-82b477f6caea` |
| S30 | Glow memudar jadi gelap | `5df7b6b8-b866-466c-bd2a-a746f15e1468` |
| S31 (hero) | Jari sentuh bulu mata | `9e05614a-1a19-4b9e-ab4f-70b7607aa848` |
| S32 | Syringe + ruang angka | `0d0b289f-9363-40ff-be9e-aadcd525a609` |

## Batch 2 · Wave 3 — 14 shot NEW (anchor: style still `323c14a0`)
| Shot | Isi | Render job ID |
|---|---|---|
| S35 (hero) | Syringe vs sendok makan | `7f5823c1-ba1c-40dc-a01d-3d8263a5d1fa` |
| S40 | Etimologi APNEA (divider) | `4841f76d-0779-4682-a67c-923a938a9a84` |
| S42 | Etimologi HYPOTENSION (divider) | `ce26afc0-be93-4fc4-8a7c-278bcec7f6d3` |
| S43 | Lidah jatuh tutup jalan napas | `fc65c955-75a6-4d79-9f72-023178ffbaf3` |
| S45 | Nada oksigen turun (visual) | `36e4165e-85e1-42a7-9fe6-fafe80460b47` |
| S48 (hero) | 4 ikon status merah | `adade1de-2b99-47ad-a115-5a80edb9ca6a` |
| S49 (hero) | Syringe mengancam (klimaks) | `48de1eb9-0e60-48bd-a53c-1cce9db8698c` |
| S50 | Siluet dokter kepala meja | `bcd17f99-f2d6-442b-90e0-08623a9c592b` |
| S51 | Paru diisi oksigen + sungkup | `cd4743c0-eca8-4c58-8e8a-6d08627467fa` |
| S52 (hero) | Laringoskop | `7075c157-f955-4a57-aea7-e7e764221fad` |
| S53 | Etimologi LARYNGOSCOPE (divider) | `4b8b0a29-e1ea-41a4-90ea-cd519a3e2206` |
| S54 | Tabung ET + ventilator | `c187c510-a6d2-4d36-ac7c-7952a957b004` |
| S58 | Wide pasien stabil + ventilator | `2fcf2c28-d0ac-411a-9472-ba3b9088b9eb` |
| S62 (hero) | Siluet gedung RS + EKG | `7421d4b7-247b-466d-bb03-0847ae1035e6` |

**Status Batch 2 (Wave 1–3):** semua **35 NEW + 3 TPL** ter-submit ke Higgsfield, anchor = master style still. ⏳ nunggu QC user di gallery.

## Rekap render VT-001
- ✅ **9 CHAR** (reference sheet terkunci) · ✅ **1 master style still** · ✅ **38 NEW/TPL** (35 NEW + 3 TPL, anchor style still).
- **16 REUSE** — tidak di-generate (layer assembly dari frame yang sudah ada di atas).
- **Total generate VT-001 = 48** (sesuai anggaran shotlist). Sisa pipeline: motion → narasi → rakit+subtitle → upload → Shorts.
