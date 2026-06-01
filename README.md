# Enterprise Linux Server Administration Standard

## Overview

Enterprise Linux Server Administration merupakan proyek implementasi dan administrasi server Linux berbasis Ubuntu Server yang dirancang untuk mensimulasikan kebutuhan infrastruktur perusahaan.

Proyek ini mencakup manajemen pengguna, pengelolaan hak akses, administrasi SSH, firewall, web server, monitoring sistem, otomatisasi sederhana, serta proses troubleshooting jaringan yang umum ditemui oleh seorang Linux System Administrator.

---

## Business Scenario

Sebuah perusahaan membutuhkan server Linux untuk mendukung kebutuhan operasional tim IT yang terdiri dari:

* Administrator
* Developer
* Operator

Administrator bertanggung jawab mengelola server.

Developer membutuhkan akses untuk mengembangkan dan mengelola aplikasi.

Operator hanya diperbolehkan melakukan monitoring tanpa hak untuk mengubah data penting.

---

## Infrastructure Architecture

### Platform

| Component  | Specification           |
| ---------- | ----------------------- |
| Host OS    | Windows 11              |
| Hypervisor | Oracle VirtualBox       |
| Guest OS   | Ubuntu Server 26.04 LTS |
| Network    | NAT                     |
| SSH Server | OpenSSH                 |
| Firewall   | UFW                     |
| Web Server | Nginx                   |

---

## Project Topology

```text
Windows Host
      │
      │ SSH
      ▼
Ubuntu Server VM
      │
      ├── User Management
      ├── Permission Management
      ├── OpenSSH Server
      ├── UFW Firewall
      ├── Nginx Web Server
      ├── Monitoring Tools
      └── Bash Automation
```

---

## Features Implemented

### Environment Setup

* Ubuntu Server Deployment
* VirtualBox Configuration
* System Verification

### User Management

* Multi User Environment
* Role Based User Structure
* Sudo Privilege Management

### Permission Management

* Ownership Configuration
* File Permission Control
* Access Restriction Testing

### SSH Administration

* OpenSSH Installation
* Remote Access Configuration
* Port Verification

### Network Troubleshooting

* DHCP Diagnostics
* IPv4 Troubleshooting
* VirtualBox Network Configuration

### Firewall Administration

* UFW Installation
* SSH Rule Configuration
* HTTP Rule Configuration

### Nginx Administration

* Web Server Deployment
* Landing Page Configuration
* Service Verification

### Monitoring

* CPU Monitoring
* Memory Monitoring
* Disk Monitoring

### Automation

* Bash Script Development
* Server Information Reporting

---

## Project Documentation

| No | Documentation           |
| -- | ----------------------- |
| 01 | Environment Setup       |
| 02 | User Management         |
| 03 | Permission Management   |
| 04 | SSH Administration      |
| 05 | Network Troubleshooting |
| 06 | Firewall Administration |
| 07 | Nginx Administration    |
| 08 | Monitoring              |
| 09 | Automation              |

Documentation files are available in the `docs/` directory.

---

## Project Structure

```text
enterprise-linux-server-administration/
│
├── README.md
│
├── docs/
│   ├── 01-environment-setup.md
│   ├── 02-user-management.md
│   ├── 03-permission-management.md
│   ├── 04-ssh-administration.md
│   ├── 05-network-troubleshooting.md
│   ├── 06-firewall-administration.md
│   ├── 07-nginx-administration.md
│   ├── 08-monitoring.md
│   └── 09-automation.md
│
├── screenshots/
│
├── scripts/
│   └── server-info.sh
│
└── topology/
```

---

## Skills Demonstrated

### Linux Administration

* Ubuntu Server Administration
* System Configuration
* Service Management

### Access Management

* User Management
* Group Management
* Linux Permissions

### Remote Administration

* OpenSSH Server
* Secure Remote Access

### Security

* UFW Firewall
* Access Restriction
* Basic Hardening

### Web Services

* Nginx Deployment
* HTTP Service Verification

### Monitoring

* CPU Monitoring
* Memory Monitoring
* Disk Monitoring

### Automation

* Bash Scripting
* System Reporting

### Troubleshooting

* DHCP Diagnostics
* Network Troubleshooting
* VirtualBox Networking

---

## Key Learning Outcomes

Through this project, I learned how to:

* Deploy and administer Ubuntu Server.
* Manage users and permissions using Linux security principles.
* Configure SSH for remote administration.
* Implement firewall rules using UFW.
* Deploy and manage Nginx Web Server.
* Monitor system resources.
* Create automation scripts using Bash.
* Troubleshoot network connectivity and DHCP issues.
* Document infrastructure implementation professionally.

---

## Future Improvements

Planned enhancements:

* DNS Server (BIND9)
* Proxmox Virtualization
* Grafana Monitoring
* Prometheus Monitoring
* Backup & Disaster Recovery
* Linux Security Hardening
* Mail Server Administration

---

## Author

Muhammad Fikri

Project: Enterprise Linux Server Administration Standard

Role: Linux System Administrator (Lab Project)
