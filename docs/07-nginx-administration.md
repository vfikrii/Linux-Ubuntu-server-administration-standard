# 07-nginx-administration.md

# Nginx Administration

## Overview

Dokumentasi ini menjelaskan implementasi Nginx sebagai web server pada Ubuntu Server.

---

## Business Requirement

Perusahaan membutuhkan web server untuk menyediakan layanan aplikasi internal.

---

## Installation

Instalasi Nginx:

```bash
sudo apt install nginx -y
```

---

## Service Verification

```bash
systemctl status nginx
```

Status:

```text
active (running)
```

---

## Landing Page Deployment

Edit file:

```bash
sudo nano /var/www/html/index.html
```

Isi:

```html
<!DOCTYPE html>
<html>
<head>
<title>Enterprise Linux Server Administration</title>
</head>
<body>
<h1>Enterprise Linux Server Administration</h1>
<p>Implemented by Muhammad Fikri</p>
</body>
</html>
```

---

## Verification

Verifikasi menggunakan:

```bash
curl http://localhost
```

atau browser.

---

## Result

Nginx berhasil dijalankan dan menampilkan landing page perusahaan.

---

## Screenshots

* nginx-status.png
* landing-page.png

---

## Outcome

Web Server berhasil diimplementasikan menggunakan Nginx.
