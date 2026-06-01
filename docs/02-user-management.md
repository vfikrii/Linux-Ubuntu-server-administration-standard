# 02-user-management.md

# User Management

## Overview

Dokumentasi ini menjelaskan implementasi manajemen pengguna pada server Linux untuk mendukung kebutuhan operasional perusahaan.

---

## Business Requirement

Perusahaan memiliki tiga jenis pengguna:

1. Administrator
2. Developer
3. Operator

Setiap pengguna harus memiliki akun terpisah agar aktivitas dapat diaudit dan hak akses dapat dikelola dengan baik.

---

## User Structure

| Username    | Role                 |
| ----------- | -------------------- |
| admin01     | Server Administrator |
| developer01 | Technical Developer  |
| operator01  | Network Operator     |

---

## Implementation

Membuat akun pengguna:

```bash
sudo adduser admin01
sudo adduser developer01
sudo adduser operator01
```

Menambahkan hak administrator:

```bash
sudo usermod -aG sudo admin01
```

---

## Verification

Verifikasi akun:

```bash
cat /etc/passwd
```

Verifikasi grup:

```bash
groups admin01
groups developer01
groups operator01
```

---

## Result

Seluruh akun berhasil dibuat dan memiliki home directory masing-masing.

Administrator memiliki hak sudo untuk melakukan administrasi server.

---

## Screenshots

* users-created.png
* groups-verification.png

---

## Outcome

Implementasi user management berhasil dilakukan sesuai kebutuhan organisasi.
