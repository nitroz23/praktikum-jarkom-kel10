# Tugas Pendahuluan
1. Jika kamu ingin mengakses web server lokal (IP: 192.168.1.10, port 80) dari jaringan luar, konfigurasi NAT apa yang perlu kamu buat?
2. Menurutmu, mana yang lebih penting diterapkan terlebih dahulu di jaringan: NAT atau Firewall? Jelaskan alasanmu.
3. Apa dampak negatif jika router tidak diberi filter firewall sama sekali?

# Modul Firewall & NAT
## 1.1 Apa itu Firewall?

### 1.1.1 Jenis-Jenis Firewall

### 1.1.2 Cara Kerja Firewall

### 1.1.3 Kebijakan Akses (Accept, Drop, Reject)

## 1.2 Apa itu Network Address Translation (NAT)?

### 1.2.1 Jenis-Jenis NAT

### 1.2.2 Cara Kerja NAT

## 1.3 Apa itu Connection Tracking?
**Connection Tracking** (pelacakan koneksi) adalah fitur **"pengamat lalu lintas jaringan"** yang cerdas. Ia mencatat siapa yang sedang ngobrol dengan siapa, kapan mulai ngobrol, lewat jalur mana (IP & port), dan apakah obrolan itu masih aktif atau sudah selesai.

Bayangkan kamu punya **resepsionis jaringan** yang mencatat semua "pengunjung" (paket data) yang masuk dan keluar. Kalau ada pengunjung yang balik lagi (paket balasan), resepsionis akan mengenalinya dan langsung mengizinkannya masuk, **tanpa perlu tanya-tanya lagi**.

Connection Tracking ini melakukan **manajemen trafik** dengan cara menyimpan informasi penting dari koneksi tersebut seperti:

- Source Address
- Destination Address
- Source Port
- Destination Port
- Protocol
- Connection State

Label ini sangat penting terutama untuk proses **firewall filtering** dan **NAT** karena memungkinkan router **mengenali status dari setiap paket data** yang lewat.

### 1.3.1 Cara Kerja Connection Tracking
Saat kamu **mengakses website**:
1. Komputer kamu mengirim permintaan ke server (misalnya IP 8.8.8.8).
2. Connection tracking mencatat: "Oke, koneksi baru dari 192.168.1.10 ke 8.8.8.8:80"
3. Server membalas → sistem tahu ini **balasan sah** dan langsung diizinkan.
4. Kalau ada koneksi aneh dari luar yang belum pernah dicatat → **langsung ditolak** (state: `invalid`)

### 1.3.2 Manfaat Connection Tracking
Connection Tracking memberikan banyak keuntungan dalam pengelolaan dan pengamanan jaringan. Berikut beberapa manfaat utamanya:
1. Keamanan yang Lebih Baik (Stateful Firewall)
2. Mendukung NAT Secara Efisien
3. Mengurangi Beban Router
4. Kontrol Lebih Detail terhadap Lalu Lintas Jaringan
5. Mendeteksi dan Menghentikan Koneksi Tidak Sah

## Tahapan Praktikum

## Tugas Modul
