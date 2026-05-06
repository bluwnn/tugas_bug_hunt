# 📌 Bugfix Pada Kode index.html

Dokumentasi ini berisi daftar bug yang ditemukan pada aplikasi serta perbaikan yang telah dilakukan untuk meningkatkan kualitas kode, tampilan, dan pengalaman pengguna.

## 🐞 Daftar Bug & Perbaikant

### 1. Bug Layout: Radio Button Tidak Tertata Dengan Benar

### Masalah

Semua elemen 'input' diberikan width: 100%, termasuk radio button. Hal ini menyebabkan radio button tampil tidak proporsional dan bergeser dari layout normal.

### Kode Bermasalah

<img src="radiobutton.png" alt="Alt Text" width="400" height="auto">

<img src="bug_1-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Pisahkan styling antara input teks dan radio button.

<img src="fixed_radiobutton.png" alt="Alt Text" width="400" height="auto">

<img src="bugfix_1-1.png" alt="Alt Text" width="400" height="auto">

### 2. Bug Logika: Data Tidak Tersimpan Saat Refresh

### Masalah

Data hanya disimpan di DOM (tabel), sehingga akan hilang saat halaman di-refresh.

### Kode Bermasalah

<img src="bug_2-1.png" alt="Alt Text" width="400" height="auto">

<img src="bug_2-2.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Gunakan _localStorage_ sebagai penyimpanan data.

<img src="bugfix_2-1.png" alt="Alt Text" width="400" height="auto">

Tambahkan fungsi render

<img src="bugfix_2-2.png" alt="Alt Text" width="400" height="auto">

### 3. Bug Logika: Fitur Edit Tidak Lengkap

### Masalah

Fungsi edit hanya mengisi sebagian data (tidak termasuk jenis kelamin dan tanggal lahir).

### Kode Bermasalah

<img src="bug_3-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

<img src="bugfix_3-1.png" alt="Alt Text" width="400" height="auto">

Tambahkan pengisian ulang untuk semua field.
