# Catatan Keuangan — Peanut & Butter (Money Manager Pastel PWA)

Aplikasi pencatat keuangan pribadi ala **Money Manager (Realbyte)** dengan tema **Cream Pastel Peanut & Butter**, terintegrasi langsung dengan **Google Sheets** sebagai database.

## Fitur Utama
1. **Transaksi Ala Money Manager**: Tampilan **Harian**, **Kalender Heatmap**, dan **Ringkasan Bulanan**, lengkap dengan **kalkulator bawaan** langsung pada kolom nominal.
2. **Akun & Sub-Pocket**: Setiap akun utama (misal: `BCA`, `Tunai`, `GoPay`) dapat dibagi menjadi beberapa kantong dana (`Utama`, `Dana Darurat`, `Jajan`, dll.) beserta fitur transfer antar-pocket.
3. **Statistik & Anggaran**: Grafik rasio pengeluaran per kategori dan indikator batas anggaran bulanan.
4. **Tabungan & Goals**: Pelacakan target tabungan yang dapat dihubungkan langsung ke saldo Pocket tertentu.
5. **Hutang & Piutang**: Pencatatan pinjaman baru, jatuh tempo, dan cicilan/pelunasan otomatis.

## Cara Setup & Deploy

### Langkah 1: Pasang Backend di Google Sheets
1. Buka file Google Sheets **App Budgeting** Anda.
2. Klik menu **Ekstensi (Extensions) > Apps Script**.
3. Hapus kode default, lalu *paste* seluruh isi file **`Code.gs`**, kemudian tekan **Simpan (Ctrl+S)**.
4. Klik tombol biru **Terapkan (Deploy) > Deployment baru (New deployment)**.
5. Pilih jenis **Aplikasi web (Web app)**:
   - **Jalankan sebagai (Execute as):** Saya (*Me*)
   - **Yang memiliki akses (Who has access):** Siapa saja (*Anyone*)
6. Klik **Terapkan**, izinkan akses jika diminta, lalu **salin URL Web App** yang muncul. *(Saat pertama kali dijalankan, script otomatis membuatkan 6 tab database beserta header dan data awalnya).*

### Langkah 2: Upload ke GitHub Pages
1. Buat repositori baru di GitHub.
2. Upload file **`index.html`**, **`manifest.json`**, serta ikon PNG (**`icon-192.png`** & **`icon-512.png`** dari gambar koin Peanut & Butter yang sudah dibuat sebelumnya).
3. Aktifkan **GitHub Pages** melalui menu **Settings > Pages > Branch: `main` / `(root)`**.
4. Buka link GitHub Pages Anda di browser HP, ketuk ikon **⚙️ (Pengaturan)** di pojok kanan atas, tempelkan **URL Web App Google Apps Script**, lalu klik **Simpan & Sinkronkan**.
5. Pilih **Add to Home Screen / Install App** di browser HP untuk memasangnya sebagai aplikasi.
