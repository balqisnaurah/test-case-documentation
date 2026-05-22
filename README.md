# Test Case Documentation

Dokumentasi test case, test plan, dan UAT checklist untuk pengujian aplikasi web toko online. Mencakup strategi pengujian end-to-end mulai dari perencanaan hingga eksekusi.

---

## Daftar File

### `TEST_PLAN.md`

Dokumen perencanaan pengujian yang menjelaskan strategi dan pendekatan QA secara menyeluruh.

**Isi Test Plan:**
- Ruang lingkup pengujian (in scope dan out of scope)
- Jenis pengujian (functional, UI, API, security, compatibility)
- Test environment dan tools yang digunakan
- Entry criteria dan exit criteria
- Identifikasi risiko dan mitigasi
- Skedul pengujian per fase
- Tim dan tanggung jawab
- Deliverables yang dihasilkan

---

### `TC_Login.md`

Test case untuk modul login dengan 10 skenario pengujian.

**Skenario yang diuji:**
- Login dengan kredensial valid
- Login dengan password salah
- Login dengan email tidak terdaftar
- Validasi field kosong (email, password, atau keduanya)
- Validasi format email tidak valid
- Pengujian keamanan: SQL injection
- Fitur "Tampilkan Password"
- Pengujian session setelah login

---

### `TC_Register.md`

Test case untuk modul registrasi dengan 8 skenario pengujian.

**Skenario yang diuji:**
- Registrasi dengan data valid
- Registrasi dengan email yang sudah terdaftar
- Validasi panjang password minimum
- Validasi password dan konfirmasi tidak cocok
- Validasi field kosong (nama, email)
- Validasi format email tidak valid
- Pengujian keamanan: XSS pada field nama

---

### `TC_Checkout.md`

Test case untuk modul checkout dengan 10 skenario pengujian.

**Skenario yang diuji:**
- Checkout dengan 1 produk dan multiple produk
- Checkout dengan keranjang kosong
- Ubah quantity dan hapus produk dari keranjang
- Validasi alamat dan metode pembayaran wajib
- Penggunaan kupon diskon (valid dan tidak valid)
- Validasi stok produk

---

### `UAT_Checklist.md`

User Acceptance Testing checklist yang merangkum hasil pengujian seluruh modul.

**Isi UAT Checklist:**
- Ringkasan total test case per modul (Login, Registrasi, Checkout)
- Status pass/fail/blocked untuk setiap modul
- Kriteria penerimaan yang harus dipenuhi
- Keputusan akhir UAT

---

## Alur Dokumentasi QA

```
TEST_PLAN.md
    ↓
TC_Login.md + TC_Register.md + TC_Checkout.md
    ↓
UAT_Checklist.md
```

---

## Total Test Case

| Modul | Jumlah Test Case |
|-------|-----------------|
| Login | 10 |
| Registrasi | 8 |
| Checkout | 10 |
| **Total** | **28** |

---

## Format Dokumentasi Test Case

Setiap test case mencakup:

| Field | Deskripsi |
|-------|-----------|
| **TC ID** | Identifier unik test case (contoh: TC-LG-001) |
| **Skenario** | Deskripsi singkat skenario pengujian |
| **Langkah Pengujian** | Langkah-langkah detail untuk mereproduksi |
| **Test Data** | Data yang digunakan dalam pengujian |
| **Expected Result** | Hasil yang diharapkan |
| **Status** | Pass / Fail / Blocked |

---

## Tentang

Proyek ini dibuat sebagai bagian dari proses belajar Quality Assurance, khususnya dalam merancang strategi pengujian dan mendokumentasikan test case. Mencakup perencanaan QA (test plan), eksekusi pengujian fungsional, validasi input, pengujian keamanan dasar (SQL injection, XSS), dan UAT yang merupakan praktik standar dalam siklus QA.
