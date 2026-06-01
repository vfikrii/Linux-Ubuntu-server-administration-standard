# 08-monitoring.md

# System Monitoring

## Overview

Dokumentasi ini menjelaskan implementasi monitoring dasar pada Ubuntu Server.

---

## Business Requirement

Administrator harus dapat memantau kondisi server untuk memastikan performa dan ketersediaan layanan.

---

## Monitoring Tools

### htop

Instalasi:

```bash
sudo apt install htop -y
```

Menjalankan:

```bash
htop
```

Fungsi:

* Monitoring CPU
* Monitoring RAM
* Monitoring Process

---

### Memory Monitoring

```bash
free -h
```

Fungsi:

* Melihat penggunaan RAM
* Melihat penggunaan swap

---

### Disk Monitoring

```bash
df -h
```

Fungsi:

* Melihat penggunaan storage
* Monitoring kapasitas disk

---

## Result

Administrator dapat memantau resource server secara real-time.

---

## Screenshots

* htop.png
* memory-usage.png
* disk-usage.png

---

## Outcome

Monitoring dasar berhasil diterapkan pada server Linux.
