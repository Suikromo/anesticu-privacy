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
| S52 (hero) | Laringoskop (orientasi diperbaiki: handle & blade ke arah tubuh/tenggorokan) | `f94831b1-7100-4924-8fef-c7a943de4a4b` (ganti `7075c157…`) |
| S53 | Etimologi LARYNGOSCOPE (divider) | `4b8b0a29-e1ea-41a4-90ea-cd519a3e2206` |
| S54 | Tabung ET + ventilator | `c187c510-a6d2-4d36-ac7c-7952a957b004` |
| S58 | Wide pasien stabil + ventilator | `2fcf2c28-d0ac-411a-9472-ba3b9088b9eb` |
| S62 (hero) | Siluet gedung RS + EKG | `7421d4b7-247b-466d-bb03-0847ae1035e6` |

**Status Batch 2 (Wave 1–3):** semua **35 NEW + 3 TPL** ter-submit ke Higgsfield, anchor = master style still. ⏳ nunggu QC user di gallery.

## Motion (image-to-video) — Batch M1: 6 hero
Kling 3.0 Turbo, 5 dtk, 1080p, 16:9, start_image = still shot; prompt gerak minimal (bible: denyut/partikel/cairan, kamera statis, jaga flat-2D). 10 kredit/klip.
| Shot | Gerak | Video job ID |
|---|---|---|
| S20 | Neuron flicker + sinyal jalan | `98389079-763a-4b98-b559-795a74b80c3f` |
| S23 | Sinyal arc di celah sinaps | `7ad9f7b2-7229-480c-a799-208487a4eb2b` |
| S31 | Glow "bernapas", jari nyaris diam | `ed7d8cca-e599-49a7-8bd5-9ce6da3c489f` |
| S49 | Glow merah berdenyut mengancam | `fe60cabb-0973-43c2-b4dc-3df040853c65` |
| S52 | Lampu cyan laringoskop berkedip | ~~`1ceca1e6…`~~ **basi** — still S52 diperbaiki orientasinya (`f94831b1`), re-motion pending |
| S62 | Garis EKG amber mengalir + gedung breathing | `6bcd4287-b1bf-4ee0-97b0-708f2c90bdef` |

**Status M1:** ✅ QC user "lolos" (flat-2D terjaga). Kecuali S52: still-nya salah orientasi laringoskop → regen (`f94831b1`), motion S52 diulang setelah still baru jadi.

## Motion — Batch M2: 9 CHAR (maskot)
Kling 3.0 Turbo, 5 dtk, 1080p, start_image = still CHAR, gerak sesuai state maskot.
| Shot | Gerak | Video job ID |
|---|---|---|
| S07 | MONI neutral — waveform cyan scroll | `e5768113-e40f-4fd9-a83c-53c4adf6a200` |
| S17 | CARDIO healthy — denyut + cairan | `88bc1b08-0bbf-4ac7-b924-17a9d79deb89` |
| S37 | ALVI healthy — napas mengembang | `db04440e-2ee3-4683-ae04-1eb5046ec4cb` |
| S39 | ALVI collapsed — glow flicker lemah | `1f014bef-fea2-4d6a-85c7-6aa9c0e35fc2` (retry; 503 pertama) |
| S41 | CARDIO straining — denyut cepat + sweat | `d55db26c-9c3d-4a17-bdf5-7ed4a5304318` |
| S44 | MONI alert — waveform amber jagged | `998d5beb-aed5-444a-a1a3-9ed4999e5931` |
| S46 | MONI alarm — waveform merah cepat | `2fe505d0-74c5-4f27-9388-a474504511d6` |
| S47 | CARDIO failing — glow redup lambat | `9aeb9e6a-f75c-4149-ac7c-d564be876608` |
| S55 | ALVI recruited — re-inflate mekanis | `8c51437c-5df6-4653-900c-fc991795c39a` |

**Status M2:** ⏳ render.

## Motion — Batch M3 & M4: sisa semua shot
**Keputusan skop (user: "CapCut jangan banyak edit"):** SEMUA still di-motion, **termasuk plate kartu/divider** — jadi garis EKG sudah bergerak sendiri di klip. Di CapCut tinggal **tempel teks + potong + subtitle**, tidak perlu animasi manual.

### M3 — plate & kartu (8)
| Shot | Video job ID | | Shot | Video job ID |
|---|---|---|---|---|
| S52 (still baru) | `5b7f2d3b-3bc8-4232-80fb-7f71e46df208` | | S13 divider | `c9d7614e-872d-49ec-965c-0723da34cf3e` |
| S01 EKG plate | `57cbc4e7-c6eb-47a1-8ceb-f42a5690754a` | | S40 APNEA | `7619428b-00db-49e5-8e6d-28300e6b5332` → S12 |
| S05 title-card | `ce8dab07-2ccc-4cc6-ba92-7db384d0b543` | | S40 | `7619428b…`(S12) / `4564febf…`(S42) |
| S30 fade-to-black | `04382061-5cad-4226-8afc-228cd815bb52` | | S42 HYPOTENSION | `4564febf-7d08-42b2-add8-ba4b53fb17d2` |

_(S12 = `7619428b…`, S40 = `7b9fda95-b626-4493-a787-22414b010739`, S53 = `22ba9c6a-8b8a-4eb7-bea9-5a82958c4244`)_

### M4 — shot NEW dinamis (23)
| Shot | Job ID | Shot | Job ID |
|---|---|---|---|
| S02 | `03a27e84-73d2-469e-bf6b-218fd3bbf447` | S27 | `3e02cd65-1e3c-4592-ba4e-ef1403014d9c` |
| S03 | `62bb7c8f-966e-476f-baad-c197f40bd110` | S32 | `e22b172f-645c-4e02-bfdb-201f8d024d11` |
| S06 | `ccd7adb7-289a-4dc5-86ec-858ad3f43f07` | S35 | `820e3a89-6121-4c4e-a805-55e2cc9d385b` |
| S08 | `38cc875f-d589-4cf8-9e07-dd99a4e858fd` | S43 | `aa688897-be69-422e-b66c-4222b435379f` |
| S10 | `8f7b01da-4eaf-42bc-b460-1436a9fc5b9c` | S45 | `60651e34-6b3e-46bb-ab61-4192ce788859` |
| S11 | `684f8405-f275-461e-81e8-b376011937ff` | S48 | `b52cfab8-a089-4585-81cc-92d3b22230c0` |
| S15 | `178f2657-556f-4723-b86d-7d98f728966e` | S50 | `4302cea9-374e-4414-a3c2-10796a921ec5` |
| S16 | `ebfa02f2-cb99-4dc8-a04b-705d791a6242` | S51 | `b46adcc8-eafa-4f39-86f0-45b22d7ae745` |
| S18 | `24c4384c-5774-44f4-a175-fe9fca05c780` | S54 | `ce4dfeda-2e72-4c32-9b47-1feb42cff658` |
| S19 | `2cb9e821-d07a-46eb-9798-b5eb1e37e38b` | S58 | `7a9798a6-8519-4497-a4ca-9a6c3fc79f86` |
| S22 | `446c2ebc-064f-4f69-b2bd-5aeab8628854` | S24 | `a48db079-8280-4e92-9fa7-d0436f8af4ba` |
| S25 | `8de7b895-422c-4e6e-9e74-03e68990844f` | | |

> **Catatan preset:** Higgsfield berulang kali menyarankan preset sinematik "IN THE DARK". SEMUA ditolak (`declined_preset_id`) & di-generate literal — preset itu akan melanggar style-lock bible (flat 2D, kamera statis).

**Total motion VT-001 ≈ 46 klip** (M1 6 + M2 9 + M3 8 + M4 23), 5 dtk 1080p, ~10 kredit/klip.

---

## Narasi — tes voice (KEPUTUSAN TERKUNCI SELAMANYA)
Bible: **1 voice dipakai selamanya** untuk 10 episode. Tes memakai **teks cold open VT-001 asli** (bukan sample generik) supaya terdengar dalam konteks. Model: `seed_audio` (Seed Audio 1.0).

| Kandidat | Gender | voice_id | Job tes |
|---|---|---|---|
| **Callum** | pria | `858499d9-fef5-40e1-bc29-b4dc661dc283` | `0ff66081-2c10-428b-bc02-449ceaf00bd5` |
| **Sterling** | pria | `dc382508-c8bd-443c-8cb2-46e57b8d2e6f` | `aba4e6b9-df62-4ab1-8c26-46579041d1db` |
| **Naomi** | wanita | `caeba733-3c17-43db-863e-69c7025512cd` | `69842497-7dc9-4ae6-84b8-4826d29469b3` |
| **Simone** | wanita | `d3b201aa-086c-4d54-8568-a6bb9f4a0b63` | `e57b00f4-9008-4944-9392-f1ad050afd46` |
| **Cillian** | pria | `d8ba9f14-8a24-44db-932b-99e16c45bd32` | `6708c4f0-6cc1-48ab-a5ad-1d37c2f9cc89` (diminta user) |

**Kriteria pilih (dari bible + retention-dna):** tenang & terkendali (kontras dgn isi yang mencekam — pelajaran dari Zack D. Films), bukan hype/iklan · jelas untuk telinga non-native (audiens internasional) · sanggup bawa jeda hening sebelum PIVOT · terdengar kredibel untuk konten medis.

**Status:** ⏳ nunggu user memilih. Begitu terpilih → kunci voice_id di sini + `production-bible.md`, lalu generate narasi penuh VT-001 per-scene.

## Rekap render VT-001
- ✅ **9 CHAR** (reference sheet terkunci) · ✅ **1 master style still** · ✅ **38 NEW/TPL** (35 NEW + 3 TPL, anchor style still).
- **16 REUSE** — tidak di-generate (layer assembly dari frame yang sudah ada di atas).
- **Total generate VT-001 = 48** (sesuai anggaran shotlist). Sisa pipeline: motion → narasi → rakit+subtitle → upload → Shorts.
