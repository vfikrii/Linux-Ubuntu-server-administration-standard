# 06-firewall-administration.md

# Firewall Administration

## Overview

Dokumentasi ini menjelaskan implementasi firewall menggunakan UFW (Uncomplicated Firewall) untuk meningkatkan keamanan server Linux.

---

## Business Requirement

Server hanya boleh mengizinkan akses terhadap layanan yang dibutuhkan.

---

## Installation

Install UFW:

```bash
sudo apt install ufw -y
```

---

## Firewall Rules

Mengizinkan SSH:

```bash
sudo ufw allow 22/tcp
```

Mengizinkan HTTP:

```bash
sudo ufw allow 80/tcp
```

---

## Enable Firewall

```bash
sudo ufw enable
```

---

## Verification

```bash
sudo ufw status verbose
```

Contoh hasil:

```text
22/tcp ALLOW
80/tcp ALLOW
```

---

## Security Benefits

* Membatasi akses yang tidak diperlukan
* Mengurangi permukaan serangan
* Melindungi layanan server

---

## Result

Firewall berhasil diterapkan dan hanya layanan yang dibutuhkan yang dapat diakses.

---

## Screenshots

* ufw-status.png

---

## Outcome

Server berhasil diamankan menggunakan UFW Firewall.
