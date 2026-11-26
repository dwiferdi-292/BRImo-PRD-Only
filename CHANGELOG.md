# CHANGELOG — BRImo-PRD-Only

Format mengikuti Keep a Changelog. Hanya mencatat perubahan yang benar-benar terjadi.

## [Belum dirilis]

### Ditambahkan
- 2026-11-26: PRD BRImo UX Redesign v1.0 (draft) pada README.md, disusun dari Worksheet 1–8 mengikuti struktur template PRD dosen.
- 2026-11-26: Struktur repository awal (README.md, CHANGELOG.md, folder src/).

### Ditambahkan (implementasi, 2026-11-26)
- Aplikasi statis `src/index.html` (HTML/CSS/JS satu berkas) dibangun dari PRD saja: beranda, tujuan transfer + nama penerima, nominal, konfirmasi (dengan Ubah Rekening/Ubah Nominal), verifikasi simulasi, status berhasil dan belum pasti, bukti transaksi, riwayat transaksi.
- `index.html` di root (pengarah ke `src/`) dan `.nojekyll` untuk GitHub Pages.
- `docs/screenshots/` berisi tangkapan layar tiap halaman.
- Prompt iterasi ke agent: 1 (pembuatan awal). Perbaikan setelah hasil pertama: 0.

### Asumsi yang diambil pada bagian yang belum pasti
- Biaya admin: Rp 0 ke Bank BRI, Rp 2.500 ke bank lain. Nominal minimum Rp 10.000. Saldo contoh Rp 12.450.000.
- Riwayat transaksi (FR-06) dibuat (masuk scope), berisi 2 transaksi contoh ditambah transaksi baru dari sesi berjalan.
- Hasil simulasi (berhasil/belum pasti) dipilih lewat pilihan di layar Verifikasi, karena PRD tidak menentukan pemicunya.
- Wawancara pengguna tetap berstatus simulasi (tidak diubah).

### Pengujian (Playwright + Chrome, lokal, 390x844)
- 15 pemeriksaan otomatis lulus terhadap Product Acceptance Criteria 1-9, tanpa error JavaScript. Satu pemeriksaan ("belum ada transaksi sebelum verifikasi selesai") lemah dan tidak dihitung sebagai bukti.
- Belum diuji: perangkat nyata, browser selain Chrome, deployment.

### Keterbatasan eksperimen
- Aplikasi ini dibuat oleh agen yang sama dengan penyusun dokumen UX pada percakapan yang sama, sehingga isolasi dari UX Skill tidak sempurna. Interpretasi hasil perbandingan harus mempertimbangkan hal ini.
- Waktu pengembangan: tidak dicatat dengan jam mulai/selesai; sesi pembuatan berlangsung pada 2026-11-26 hingga 2026-11-27.

### Diperbarui (dokumen v1.1, 2026-11-27)
- Seluruh tanda yang sebelumnya menandai informasi belum pasti telah diputuskan penulis dan diisi di PRD, README, dan (pada repo B) AGENTS.md serta UX-Skill. Keputusan mengikuti Worksheet 1–8: wawancara tetap berstatus simulasi, riwayat masuk scope (User Story 5), biaya dan batas nominal ditulis sebagai asumsi proyek akademik.
- Catatan: aplikasi pada src/ dibangun dari dokumen v1.0. Perubahan v1.1 menyelaraskan teks dengan keputusan yang sudah dipakai aplikasi dan tidak mengubah kodenya.
- Tanggal unggah ke GitHub: 2026-11-27. Demo GitHub Pages aktif pada hari yang sama.

### Belum dikerjakan
- Deployment.
- Pengujian pada pengguna nyata dan usability test.
