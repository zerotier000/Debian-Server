# Debian-Server

# FINAL-PROJECT-OS-SERVER-SYSTEM-ADMIN---22.83.0886

Repository ini berisi dokumentasi yang menjelaskan cara instalasi dan konfigurasi berbagai layanan server, seperti SSH, DHCP, FTP/Samba, DNS, mail server, dan web server, serta Database Server. Dokumen ini ditujukan untuk memandu pengguna dalam mengatur dan mengelola server-server ini dengan langkah-langkah yang jelas.

## Daftar Isi
1. [Instalasi dan Konfigurasi SSH](#1-instalasi-dan-konfigurasi-ssh-server)
2. [Instalasi dan Konfigurasi DHCP Server](#2-instalasi-dan-konfigurasi-dhcp-server)
3. [Instalasi dan Konfigurasi FTP dan Samba Server](#3-instalasi-dan-konfigurasi-ftp-dan-samba-server)
4. [Instalasi dan Konfigurasi Web Server](#4-instalasi-dan-konfigurasi-web-server)
5. [Instalasi dan Konfigurasi DNS Server](#5-instalasi-dan-konfigurasi-dns-server)
6. [Instalasi dan Konfigurasi Database Server](#6-instalasi-dan-konfigurasi-database-server)
7. [Instalasi dan Konfigurasi Mail Server](#7-instalasi-dan-konfigurasi-mail-server)
8. [Instalasi dan Konfigurasi Monitoring Server](#8-instalasi-dan-konfigurasi-monitoring-server)
   

## 1. Instalasi dan Konfigurasi SSH Server

### 1.1 Instalasi SSH
**Langkah 1: Lakukan Instalasi Paket SSH Server**

```
apt-get install openssh-server
```
### 1.2 Konfigurasi SSH
**Langkah 1: Buka Direktori konfigurasi ssh dengan text editor(disini saya menggunakan nano)**
```
nano /etc/ssh/sshd_config
```
**Langkah 2: Edit Konfigurasi seperti dibawah ini**
```
Include /etc/ssh/sshd_config.d/*.conf

Port 9029
#AddressFamily any
#ListenAddress 0.0.0.0
#ListenAddress ::

#HostKey /etc/ssh/ssh_host_rsa_key
#HostKey /etc/ssh/ssh_host_ecdsa_key
#HostKey /etc/ssh/ssh_host_ed25519_key

# Ciphers and keying
#RekeyLimit default none

# Logging
#SyslogFacility AUTH
#LogLevel INFO
