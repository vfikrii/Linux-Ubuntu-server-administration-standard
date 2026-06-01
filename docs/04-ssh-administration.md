# 04-ssh-administration.md

# SSH Administration

## Overview

Dokumentasi ini menjelaskan implementasi layanan Secure Shell (SSH) untuk kebutuhan remote administration server.

---

## Business Requirement

Administrator membutuhkan akses remote untuk mengelola server tanpa harus berada di depan mesin fisik.

---

## Installation

Instalasi OpenSSH Server:

```bash
sudo apt install openssh-server -y
```

---

## Service Verification

Memastikan service berjalan:

```bash
systemctl status ssh
```

Status:

```text
active (running)
```

---

## Port Verification

Memastikan SSH mendengarkan pada port 22:

```bash
sudo ss -tlnp | grep :22
```

Output:

```text
LISTEN 0.0.0.0:22
LISTEN [::]:22
```

---

## Remote Access Test

Pengguna dapat melakukan koneksi menggunakan:

```bash
ssh developer01@server-ip
```

atau melalui VirtualBox NAT Port Forwarding:

```bash
ssh developer01@localhost -p 2222
```

---

## Result

SSH Server berhasil diinstal dan dapat digunakan untuk administrasi jarak jauh.

---

## Screenshots

* ssh-status.png
* ssh-port22.png
* ssh-login-success.png

---

## Outcome

Remote administration berhasil diterapkan menggunakan OpenSSH Server.
