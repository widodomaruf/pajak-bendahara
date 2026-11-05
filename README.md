# Pahami Pajak Bendahara

Website edukasi pajak untuk **bendahara instansi pemerintah**: bendahara satker APBN, OPD APBD, Dana BOS, dan Dana Desa. Dengan website ini, bendahara bisa belajar sekaligus langsung mempraktikkan kewajibannya: memotong, memungut, menyetor, dan melaporkan pajak melalui Coretax DJP.

Disusun oleh **Muhammad Widodo Ma'ruf**, Edukator Pajak.
Instagram: [@widodomaruf](https://www.instagram.com/widodomaruf/) · YouTube: [@widodomaruf](https://www.youtube.com/@widodomaruf)

---

## Fitur

| Bagian | Isi |
|---|---|
| **Cek Transaksi** | Hitung pajak satu transaksi dari lawan transaksi (badan/orang pribadi), sumber dana, jenis belanja, nilai, dan status rekanan. Hasilnya menampilkan jenis pajak, jumlah, kode objek pajak, jenis bukti potong (BP21/BPPU), KAP-KJS, dan jumlah yang dibayarkan ke rekanan. |
| **Materi** | PPh 21, PPh 22, PPh 23, PPN, PPh 4(2) final, serta tabel kode setoran (KAP-KJS) bendahara. |
| **Jenis Bendahara** | Perbedaan alur pajak bendahara APBN, APBD, BOS, dan Desa. |
| **Alur Coretax** | Lima langkah, dari menyiapkan akun sampai melapor SPT Masa. |
| **Jatuh Tempo** | Kalender batas setor dan batas lapor yang dihitung otomatis dari tanggal hari ini. |
| **Kalkulator PPh 21** | Tarif efektif rata-rata (TER) bulanan untuk pegawai tetap dan TER harian untuk pegawai tidak tetap. |
| **Kuis** | Sembilan kasus bendahara, masing-masing dengan pembahasan. |
| **FAQ & Glosarium** | Pertanyaan yang sering muncul dan istilah yang bisa dicari. |
| **Tanya** | Formulir pertanyaan (Google Form) yang tersambung ke spreadsheet. |

## Ketentuan yang dipakai

- PMK 81/2024: Coretax, jatuh tempo setor dan lapor, pemungut PPh 22
- PMK 59/2022 s.t.d.t.d PMK 11/2025: PPN yang dipungut instansi pemerintah
- PMK 131/2024: PPN 12% dengan DPP nilai lain 11/12
- PP 58/2023 dan PMK 168/2023: PPh 21 tarif efektif rata-rata (TER)
- PMK 141/2015: jenis jasa lain objek PPh 23
- PP 55/2022 s.t.d.d PP 20/2026: PPh final UMKM
- PP 9/2022: PPh final jasa konstruksi

Materi disusun per **November 2026**.

## Struktur

```
.
├── index.html   # seluruh halaman: HTML, CSS, dan JavaScript dalam satu file
└── README.md
```

Website ini tidak memerlukan proses build, server, atau database. Font dimuat dari Google Fonts. Semua perhitungan berjalan di browser pengunjung.

## Menjalankan di komputer sendiri

Cukup buka `index.html` di browser. Bila ingin menjalankannya lewat server lokal:

```bash
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## Publikasi

### GitHub Pages
1. Unggah `index.html` dan `README.md` ke repository publik.
2. Buka **Settings → Pages**. Pada **Source** pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Website tersedia di `https://<username>.github.io/<nama-repo>/`.

### Vercel
1. Pilih **Add New → Project**, lalu impor repository ini.
2. Framework Preset: **Other**. Tidak ada build command, dan output directory dikosongkan.
3. Klik **Deploy**. Setiap commit ke branch `main` otomatis memperbarui website.

## Memperbarui isi

Bagian yang paling sering perlu diperbarui saat aturan berubah ada di `index.html`:

| Yang diubah | Cari di kode |
|---|---|
| Daftar jasa PPh 23 dan kode objek | `const JASA` |
| Tarif jasa konstruksi | `const KONS` |
| Objek PPh 21 bukan pegawai | `const HON` |
| Tabel TER PPh 21 | `const TER` |
| Kode KAP-KJS per sumber dana | `const KJSB` dan `function kapOf` |
| Soal kuis | `const Q` |
| FAQ dan glosarium | `const F` dan `const G` |
| Link Google Form | cari `docs.google.com/forms` |

## Catatan

Website ini adalah materi edukasi, bukan pengganti peraturan resmi. Untuk kasus khusus atau bila aturan berubah, konfirmasikan ke KPP/KP2KP tempat instansi terdaftar.

---

© 2026 Muhammad Widodo Ma'ruf
