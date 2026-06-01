# 05-network-troubleshooting.md

# Network Troubleshooting

## Overview

Dokumentasi ini menjelaskan proses investigasi dan penyelesaian masalah jaringan yang terjadi saat implementasi SSH pada VirtualBox.

---

## Problem Description

Saat melakukan koneksi SSH dari Windows ke Ubuntu Server, koneksi gagal dilakukan.

Contoh:

```powershell
ssh developer01@127.0.0.1
```

Error:

```text
Connection refused
```

---

## Investigation Process

### Step 1 - Verify SSH Service

Memastikan layanan SSH berjalan.

```bash
systemctl status ssh
```

Hasil:

```text
active (running)
```

---

### Step 2 - Verify Listening Port

```bash
sudo ss -tlnp | grep :22
```

Hasil:

```text
LISTEN 0.0.0.0:22
```

SSH berjalan normal.

---

### Step 3 - Verify Network Configuration

```bash
ip a
```

Ditemukan bahwa server hanya memperoleh IPv6 dan tidak mendapatkan IPv4.

---

### Step 4 - DHCP Diagnostics

```bash
sudo dhclient -v enp0s3
```

Output:

```text
DHCPDISCOVER
DHCPDISCOVER
DHCPDISCOVER
```

Tidak terdapat DHCPOFFER dari DHCP Server.

---

## Root Cause

Mode jaringan VirtualBox menggunakan Bridged Adapter namun gagal memperoleh alamat IPv4 dari jaringan host.

---

## Solution

Mengubah konfigurasi jaringan VirtualBox menjadi:

```text
Network Mode: NAT
```

Setelah perubahan:

```bash
hostname -I
```

Output:

```text
10.0.2.15
```

---

## Result

Virtual Machine berhasil memperoleh alamat IPv4 dan dapat berkomunikasi melalui jaringan NAT VirtualBox.

---

## Screenshots

* bridged-adapter-problem.png
* dhcp-discover.png
* nat-ip-success.png

---

## Lessons Learned

Masalah konektivitas SSH tidak selalu disebabkan oleh layanan SSH. Investigasi harus dilakukan secara sistematis mulai dari service, port, interface jaringan, hingga konfigurasi hypervisor.

---

## Outcome

Network troubleshooting berhasil dilakukan dan root cause berhasil diidentifikasi.
