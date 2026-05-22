# Test Case Documentation

Dokumentasi test case dan UAT checklist untuk pengujian aplikasi web toko online. Mencakup pengujian modul autentikasi (login, registrasi) dan modul transaksi (checkout).

---

## Daftar File

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

## Total Test Case

| Modul | Jumlah Test Case |
|-------|-----------------|
| Login | 10 |
| Registrasi | 8 |
| Checkout | 10 |
| **Total** | **28** |

---

## Format Dokumentasi

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

Proyek ini dibuat sebagai bagian dari proses belajar Quality Assurance, khususnya dalam merancang dan mendokumentasikan test case. Mencakup pengujian fungsional, validasi input, dan pengujian keamanan dasar (SQL injection, XSS) yang umum dilakukan dalam siklus QA.
