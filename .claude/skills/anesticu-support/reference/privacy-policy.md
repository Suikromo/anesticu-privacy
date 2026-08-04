# Peta struktur `privacy_policy.html`

Satu berkas HTML mandiri (tanpa dependensi eksternal), ~310 baris, dwibahasa dengan pengalih bahasa berbasis JavaScript.

## Tata letak

| Bagian | Perkiraan baris | Isi |
|---|---|---|
| `<style>` | 7–130 | Seluruh CSS inline. Variabel warna ada di `:root` (`--navy`, `--blue`, `--cyan`, dst.) |
| `<header>` | ~140–145 | Judul + baris **`Last updated: ... | Version ...`** (baris 143) |
| `.lang-toggle` | ~147–150 | Dua tombol pemanggil `showLang('id'|'en', this)` |
| `#content-id` | ~154–222 | Isi kebijakan bahasa Indonesia (tampil secara bawaan) |
| `#content-en` | ~224–290 | Isi kebijakan bahasa Inggris |
| `<footer>` + `<script>` | ~292–310 | Hak cipta + fungsi `showLang` |

## Sembilan bagian — harus sejajar di kedua bahasa

| # | Indonesia | English |
|---|---|---|
| 1 | Tentang Kebijakan Ini | About This Policy |
| 2 | Data yang Dikumpulkan | Data Collection |
| 3 | Penyimpanan Data Lokal | Local Data Storage |
| 4 | Pihak Ketiga | Third-Party Services |
| 5 | Perizinan Aplikasi | App Permissions |
| 6 | Disclaimer Medis | Medical Disclaimer |
| 7 | Keamanan Data | Data Security |
| 8 | Perubahan Kebijakan | Policy Changes |
| 9 | Hubungi Pengembang | Contact the Developer |

Penomoran dan urutan harus tetap cocok antar bahasa. Kalau menambah bagian baru, tambahkan di **kedua** blok dan nomori ulang keduanya.

## Kelas pembungkus yang dipakai

- `.section` — kartu putih pembungkus tiap bagian
- `.highlight` — kotak hijau penegasan (dipakai di bagian 2: klaim "tidak mengumpulkan data")
- `.warning` — kotak kuning peringatan (dipakai di bagian 6: disclaimer medis)
- `.contact-box section` — bagian 9

Pakai kelas yang sudah ada; jangan bikin gaya baru kecuali memang perlu.

## Jebakan

1. **Lupa menyunting salah satu bahasa.** Jebakan paling sering. Setelah menyunting, hitung ulang: jumlah `<h2>` di `#content-id` harus sama dengan di `#content-en`.
2. **Lupa menaikkan versi.** Baris 143 (`Last updated: June 2025 &nbsp;|&nbsp; Version 2.0`) harus ikut diperbarui setiap ada perubahan isi yang berarti.
3. **`googled12735427fff785c.html` tidak boleh disentuh.** Isinya harus tetap persis `google-site-verification: googled12735427fff785c.html` — kalau berubah, verifikasi Google Search Console lepas.
4. **Jangan tambahkan sumber daya eksternal** (font, skrip, gambar dari CDN). Halaman ini sengaja mandiri sepenuhnya.
5. **Klaim harus tetap jujur terhadap aplikasi.** Kalau suatu saat aplikasi mulai memakai analytics, crash reporting, atau meminta izin baru, bagian 2, 4, dan 5 wajib diperbaiki lebih dulu — jangan biarkan halaman ini menjanjikan sesuatu yang tidak lagi benar. Ini kewajiban hukum di Google Play, bukan sekadar kerapian.

## Cara memeriksa hasil suntingan

```bash
# jumlah bagian harus sama di kedua bahasa
grep -c '<h2>' privacy_policy.html          # totalnya harus genap (9 + 9 = 18)
# lihat baris versi
sed -n '143p' privacy_policy.html
```
