# 01-environment-setup.md

# Environment Setup

## Overview

Dokumentasi ini menjelaskan proses persiapan lingkungan server Linux menggunakan Ubuntu Server pada VirtualBox sebagai fondasi infrastruktur perusahaan.

---

## Business Requirement

Perusahaan membutuhkan sebuah server Linux yang stabil untuk mendukung kebutuhan Administrator, Developer, dan Operator dalam menjalankan layanan internal perusahaan.

---

## Infrastructure Specification

| Component               | Specification           |
| ----------------------- | ----------------------- |
| Host Operating System   | Windows 11              |
| Virtualization Platform | Oracle VirtualBox       |
| Guest Operating System  | Ubuntu Server 26.04 LTS |
| CPU                     | 2 vCPU                  |
| Memory                  | 4 GB RAM                |
| Storage                 | 30 GB                   |
| Network Mode            | NAT                     |

---

## System Verification

Verifikasi sistem dilakukan menggunakan perintah:

```bash
hostnamectl
```

dan

```bash
lsb_release -a
```

---

## Expected Result

Server berhasil berjalan menggunakan Ubuntu Server dan siap digunakan untuk proses administrasi sistem.

---

## Screenshots

* installation-hostnamectl.png
* installation-os-version.png

---

## Outcome

Lingkungan server berhasil dibangun dan siap digunakan untuk implementasi layanan administrasi Linux.
