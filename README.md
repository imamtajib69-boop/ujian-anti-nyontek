# ⚡ CBT TKA - Sistem Ujian Anti Nyontek Otomotif

Aplikasi portal ujian berbasis web (Computer-Based Test) berstandar **Tes Kemampuan Akademik (TKA / UTBK)** dengan sistem **Timer 30 Detik Per Soal** dan pengawasan **Anti-Nyontek Realtime**.

Dirancang khusus untuk asesmen kompetensi kejuruan Kelas XI Teknik Otomotif (XI TO 1 s/d XI TO 7).

---

## 🚀 Fitur Unggulan

### 1. Sistem Ujian Mode TKA
- **Timer Ketat 30 Detik Per Soal**: Dilengkapi progress bar visual (berubah warna: Hijau ➔ Kuning ➔ Merah berkedip di 5 detik terakhir).
- **Auto-Advance**: Berpindah otomatis ke soal berikutnya saat waktu 30 detik habis tanpa menunggu tindakan siswa.
- **Satu Arah (Lock Progression)**: Soal yang telah dilewati terkunci secara permanen demi integritas waktu.
- **Acak Soal (Fisher-Yates Shuffle)**: Urutan nomor soal antar-peserta berbeda meskipun duduk bersebelahan.
- **Navigasi Keyboard Cepat**: Tekan tombol `A`, `B`, `C`, `D` untuk memilih opsi, lalu `Enter` / `Spasi` untuk lanjut.
- **Ukuran Teks Dinamis**: Fitur pembesar/pengecil font soal (`A-` / `A+`).

### 2. Pengawasan Anti-Nyontek (Proctoring)
- **Deteksi Ganti Tab / Aplikasi**: Terdeteksi jika siswa membuka tab baru atau beralih ke aplikasi lain.
- **Deteksi Split Screen**: Mencegah siswa membagi layar di HP maupun laptop.
- **Proteksi Tombol**: Blokir klik kanan, F12 (Inspect Element), pintasan keyboard terlarang (Ctrl+C, Ctrl+V, Alt+Tab).
- **Sanksi Bertingkat**:
  - *Pelanggaran 1*: Peringatan keras dan auto-logout dari ruang ujian.
  - *Pelanggaran 2*: Akun diblokir permanen, ujian didiskualifikasi, nilai otomatis 0.

### 3. Panel Guru & Administrator
- **Dukungan 7 Kelas**: Guru kelas XI TO 1 sampai XI TO 7 memiliki hak akses terpisah.
- **Import Siswa Masal**: Cukup tempel daftar nama, akun langsung dibuatkan otomatis.
- **Bank Soal Masal**: Upload hingga 30 butir soal sekaligus menggunakan parser teks pintar.
- **Ekspor Excel Rapi**: Unduh rekapitulasi nilai lengkap dengan penanda warna hijau (Lulus) dan merah (Remedial).
- **Log Pelanggaran Realtime**: Riwayat kecurangan siswa tercatat lengkap dengan waktu dan jenis pelanggarannya.

---

## 📂 Struktur File

| File | Keterangan |
| :--- | :--- |
| `index.html` | Antarmuka pengguna (Frontend) dengan Tailwind CSS |
| `Code.gs` | Logika server (Backend) Google Apps Script & Google Sheets |
| `README.md` | Dokumentasi dan petunjuk penggunaan sistem |

---

## 🛠️ Cara Instalasi & Deploy

1. Buka [Google Sheets](https://sheets.new) baru.
2. Klik menu **Extensions (Ekstensi)** ➔ **Apps Script**.
3. Di editor Apps Script:
   - Salin isi file `Code.gs` ke file `Code.gs` di Apps Script.
   - Buat file HTML baru dengan nama `index` (klik tanda **+** ➔ **HTML**), lalu salin seluruh isi file `index.html` ke dalamnya.
4. Klik tombol **Save (Simpan)**.
5. Klik **Deploy** ➔ **New deployment**:
   - Pilih jenis: **Web app**.
   - Execute as: **Me**.
   - Who has access: **Anyone (Siapa saja)**.
6. Salin link Web App yang dihasilkan dan bagikan kepada siswa/guru.

---

## 👥 Akun Default

| Peran | Username | Password |
| :--- | :--- | :--- |
| **Admin** | `admin` | `admin123` |
| **Guru TO 1** | `guru_to1` | `guru123` |
| **Guru TO 2 - 7** | `guru_to2` s/d `guru_to7` | `guru123` |