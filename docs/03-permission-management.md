# 03-permission-management.md

# Permission Management

## Overview

Dokumentasi ini menjelaskan implementasi hak akses file dan direktori menggunakan ownership dan permission Linux.

---

## Business Requirement

Developer membutuhkan akses penuh terhadap file proyek untuk melakukan pengembangan aplikasi.

Operator hanya diperbolehkan melihat data dan tidak diperbolehkan melakukan perubahan.

---

## Directory Structure

Direktori proyek dibuat sebagai berikut:

```text
/project
```

---

## Implementation

Membuat direktori proyek:

```bash
sudo mkdir /project
```

Mengubah ownership:

```bash
sudo chown developer01:developer01 /project
```

Verifikasi ownership:

```bash
ls -ld /project
```

---

## Testing

### Developer Access

Login sebagai developer:

```bash
su - developer01
```

Masuk ke direktori proyek:

```bash
cd /project
```

Membuat file:

```bash
touch source_code.txt
```

Hasil:

Berhasil membuat file tanpa error.

---

### Operator Access

Login sebagai operator:

```bash
su - operator01
```

Percobaan mengubah file:

```bash
echo "test" >> source_code.txt
```

Hasil:

```text
Permission denied
```

---

## Result

Developer memiliki akses penuh terhadap direktori proyek.

Operator tidak dapat melakukan perubahan terhadap file proyek.

---

## Screenshots

* ownership-project-folder.png
* developer-create-file.png
* operator-permission-denied.png

---

## Outcome

Role Based Access Control berhasil diterapkan menggunakan mekanisme ownership dan permission Linux.
