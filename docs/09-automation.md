# 09-automation.md

# Basic Automation

## Overview

Dokumentasi ini menjelaskan implementasi otomatisasi sederhana menggunakan Bash Script untuk memperoleh informasi server secara cepat.

---

## Business Requirement

Administrator membutuhkan laporan kondisi server tanpa menjalankan banyak perintah secara manual.

---

## Script Creation

Membuat file:

```bash
nano server-info.sh
```

Isi script:

```bash
#!/bin/bash

echo "=== SERVER INFORMATION ==="

echo ""
echo "Hostname:"
hostname

echo ""
echo "IP Address:"
hostname -I

echo ""
echo "Disk Usage:"
df -h

echo ""
echo "Memory Usage:"
free -h
```

---

## Grant Execute Permission

```bash
chmod +x server-info.sh
```

---

## Execution

```bash
./server-info.sh
```

---

## Result

Administrator dapat memperoleh informasi server melalui satu perintah.

---

## Benefits

* Menghemat waktu administrasi
* Mengurangi kesalahan manual
* Mempermudah troubleshooting

---

## Screenshots

* automation-script.png

---

## Outcome

Implementasi otomatisasi dasar berhasil dilakukan menggunakan Bash Script.
