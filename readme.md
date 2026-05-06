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

---

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

---

### 3. Bug Logika: Fitur Edit Tidak Lengkap

### Masalah

Fungsi edit hanya mengisi sebagian data (tidak termasuk jenis kelamin dan tanggal lahir).

### Kode Bermasalah

<img src="bug_3-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Tambahkan pengisian ulang untuk semua field.

<img src="bugfix_3-1.png" alt="Alt Text" width="400" height="auto">

---

### 4. Bug UX: Mekanisme Edit Menghapus Data Lama

### Masalah

Data lama dihapus saat edit, kemudian dibuat ulang. Ini berisiko kehilangan data jika pengguna tidak menyimpan ulang.

### Kode Bermasalah

<img src="bug_4-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Gunakan mode edit dengan indeks data.

<img src="bugfix_4-1.png" alt="Alt Text" width="400" height="auto">
<img src="bugfix_4-2.png" alt="Alt Text" width="400" height="auto">

---

### 5. Bug UI: Ikon Aksi Tidak Muncul

### Masalah

Menggunakan file gambar (edit.png, trash.png) tanpa memastikan keberadaan file.

### Kode Bermasalah

<img src="bug_5-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Gunakan ikon teks/emoji

<img src="bugfix_5-1.png" alt="Alt Text" width="400" height="auto">

---

### 6. Bug HTML: Penggunaan < a href="#" > untuk Aksi

### Masalah

Menggunakan anchor (< a >) untuk aksi menyebabkan perilaku tidak diinginkan seperti scroll ke atas.

### Kode bermasalah

<img src="bug_6-1.png" alt="Alt Text" width="400" height="auto">

### Perbaikan

Gunakan elemen _button_

<img src="bugfix_6-1.png" alt="Alt Text" width="400" height="auto">

---

### 7. Bug UX: Default Tanggal Tidak Valid

### Masalah

Dropdown tanggal, bulan, dan tahun memiliki nilai default sehingga pengguna dapat mengirim data tanpa memilih secara sadar.

### Kode bermasalah

<img src="bug_7-1.png" width="400" height="auto">

### Perbaikan

Tambahkan placeholder dan atribut _required_

<img src="bugfix_7-1.png" width="400" height="auto">

---

### 8. Bug Desain: Input Tanggal Tidak Efisien

### Masalah

Menggunakan tiga dropdown untuk tanggal lahir tidak efisien dan rawan kesalahan.

### Kode bermasalah

```
<select id="tanggal"></select>
<select id="bulan"></select>
<select id="tahun"></select>
```

### Perbaikan

Gunakan _input tanggal bawaan browser.

```
        <div class="field">
          <label>Tanggal Lahir</label>
          <input type="date" id="ttl" required />
        </div>
```
---

### 9. Bug Keamanan: Password Ditampilkan Secara Plain Text

### Masalah

Password ditampilkan secara langsung di tabel, yang merupakan praktik buruk.

### Kode bermasalah

```
<td>${password}</td>
```

### Perbaikan

Masking password.

```
const masked = "•".repeat(mhs.password.length);
```

---

### 10. Bug Maintainability: Tahun Hardcoded

### Masalah

Rentang tahun berhenti di 2025 dan tidak akan diperbarui otomatis.

### Kode bermasalah

```
    for (let i = 1990; i <= 2025; i++) {
        document.getElementById("tahun").innerHTML += `<option value="${i}">${i}</option>`;
    }
```

### Perbaikan

Gunakan tahun saat ini secara dinamis.

```
<input type="date" id="ttl" required /> 
```

---

### 11. Bug CSS: Tidak Menggunakan box-sizing

### Masalah

Padding dapat menyebabkan ukuran elemen melebihi container.

### Kode bermasalah

```
        input, textarea, select {
            width: 100%;
            padding: 8px;
            margin: 5px 0 15px;
        }
```

### Perbaikan

```
* {
    box-sizing: border-box;
  }
```

---
