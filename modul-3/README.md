# Tugas Pendahuluan
SABAR YAA

## 1.1 Apa itu Jaringan Wireless?
"Wireless" secara harfiah berarti "tanpa kabel". Jadi, jaringan wireless adalah jaringan komunikasi yang tidak menggunakan kabel untuk menghubungkan antar perangkat. Sebagai gantinya, jaringan ini memanfaatkan gelombang elektromagnetik (EM waves) seperti gelombang radio atau inframerah sebagai media transmisinya.

"Kalau kabel itu seperti jalan aspal yang harus dibangun fisik, maka wireless itu seperti udara yang bisa dilewati sinyal — bebas hambatan dan lebih fleksibel!"

Kalau kabel itu seperti jalan aspal yang harus dibangun fisik, maka wireless itu seperti udara yang bisa dilewati sinyal — bebas 
hambatan dan lebih fleksibel!

### 1.1.1 Tipe-tipe Jaringan Wireless
#### 1.1.1.1 Wi-Fi
**Wi-Fi (Wireless Fidelity)** adalah teknologi standar untuk jaringan WLAN (Wireless Local Area Network) yang menghubungkan komputer dan perangkat lain tanpa kabel ke jaringan dan internet.

"Gampangnya, Wi-Fi itu seperti versi nirkabel dari kabel LAN. Kalau kabel LAN butuh ditancapkan, Wi-Fi cukup cari sinyal, klik SSID, masukin password, dan kamu sudah online!"

Wi-Fi menggunakan gelombang radio untuk mengirim dan menerima data dengan kecepatan tinggi.
Saat kamu tersambung ke Wi-Fi, sebenarnya kamu sedang terhubung ke router wireless, yang lalu menyambungkan perangkatmu ke internet.

Router Wi-Fi akan:
- Menciptakan jaringan lokal tanpa kabel
- Mengatur perangkat yang tersambung
- Mengirim data ke internet (dan sebaliknya)

#### 1.1.1.2 Bluetooth
Bluetooth adalah standar komunikasi jarak pendek (short-range wireless) yang memungkinkan perangkat seperti HP, laptop, speaker, printer, kamera, dan lainnya saling terhubung tanpa kabel.

"Kalau Wi-Fi itu jaringan untuk internet, Bluetooth itu untuk komunikasi antar perangkat jarak dekat — kayak kamu kirim lagu dari HP ke speaker bluetooth."

Bluetooth menggunakan gelombang radio 2.4 GHz (frekuensi yang sama dengan Wi-Fi) untuk mentransfer data antar perangkat.

**Kelebihan Bluetooth:**
- Tidak butuh router atau access point
- Bisa melewati benda atau tembok tipis
- Hemat daya dan biaya murah
- Umumnya plug-and-play

#### 1.1.1.3 Perbedaan Wi-Fi dan Bluetooth
| Aspek        | Wi-Fi                         | Bluetooth                      |
| ------------ | ----------------------------- | ------------------------------ |
| Tujuan utama | Akses internet                | Koneksi antar perangkat        |
| Jangkauan    | Lebih luas (hingga 100m)      | Jarak pendek (maks 10m)        |
| Kecepatan    | Lebih cepat                   | Cukup untuk file kecil/audio   |
| Daya         | Boros (lebih tinggi)          | Hemat daya                     |
| Koneksi      | Melalui router / access point | Langsung antar perangkat (P2P) |


## 1.2 Perbedaan Jaringan Wired vs Wireless
| Aspek                | Wired Network (Kabel)                 | Wireless Network (Wi-Fi)                    |
| -------------------- | ------------------------------------- | ------------------------------------------- |
| Media                | Kabel fisik (biasanya Ethernet)       | Gelombang radio / EM waves                  |
| Mobilitas            | Terbatas (harus tetap di dekat kabel) | Tinggi (bebas gerak selama dalam jangkauan) |
| Kemudahan pemasangan | Lebih ribet (perlu instalasi kabel)   | Lebih praktis (tinggal konek SSID)          |
| Kecepatan            | Sangat stabil dan tinggi              | Tergantung sinyal, bisa turun kalau jauh    |
| Keamanan             | Lebih aman secara fisik               | Perlu proteksi (WPA2/WPA3, password, dll)   |
| Cocok untuk          | Server, desktop tetap, studio editing | Laptop, HP, tablet, perangkat mobile        |
| Contoh penggunaan    | Lab komputer, kantor, data center     | Rumah, kampus, cafe, bandara, hotel         |

## 1.3 Teknologi Wireless dan Standar IEEE 802.11
Apa itu standar IEEE 802.11? Dia lebih tepatnya adalah arsitektur dari jaringan wireless LAN (WLAN), atau seperti yang kita bahas tadi ia adalah Wi-Fi.

"Ibaratnya, kalau Wi-Fi itu kendaraan, maka IEEE 802.11 adalah buku aturan lalu lintasnya."

Standar Wi-Fi terdiri dari banyak versi (amandemen), contohnya:
| Versi Standar | Keterangan                          |
| ------------- | ----------------------------------- |
| 802.11a       | Kecepatan tinggi, frekuensi 5 GHz   |
| 802.11b       | Salah satu standar awal, 2.4 GHz    |
| 802.11g       | Lebih cepat dari 802.11b            |
| 802.11n       | Dual-band, sangat populer           |
| 802.11e       | Mendukung QoS (Quality of Service)  |
| 802.11ac/ax   | Generasi baru, lebih cepat & stabil |

### 1.3.1 Station (STA)
Merupakan setiap perangkat yang terhubung ke jaringan WLAN.
Dibagi menjadi dua jenis utama:

1. Wireless Access Point (WAP / AP)
Perangkat penghubung antara jaringan kabel dan nirkabel

Berfungsi sebagai jembatan antara client dan router

2. Client
Perangkat pengguna seperti laptop, HP, printer, tablet, dll

Terhubung ke jaringan melalui SSID dari Access Point.

### 1.3.2 Access Point (AP)
Salah satu elemen utama dalam arsitektur 802.11 adalah Access Point (AP).
- **AP mendukung koneksi kabel dan wireless** secara bersamaan.
- Dalam standar 802.11, jaringan kabel yang terhubung ke AP disebut:<br>
**👉 Distribution System (DS)**
- **Fungsi utama AP adalah sebagai jembatan (bridge)** antara:
  - Jaringan wireless (Wi-Fi)
  - Jaringan kabel (Ethernet)

Jadi, AP **meneruskan data** antara perangkat wireless dan jaringan LAN, dengan memproses **frame Ethernet level 2 (L2)** dari dan ke dua sisi tersebut.

### 1.3.3 SSID: Identitas Jaringan Wireless
Setiap jaringan wireless (Wi-Fi) pasti memiliki **SSID (Service Set Identifier)**, yaitu:
- **Nama unik** yang membedakan satu jaringan WLAN dengan yang lain
- Semua perangkat yang ingin bergabung ke jaringan harus menyambung ke SSID yang sama

"Misalnya kamu lihat SSID bernama Kampus_ITS_Wifi, itu adalah identitas WLAN tempatmu akan berga bung."

## 2.1 Perangkat Wireless Network

### 2.1.1 Access Point

### 2.1.2 Wireless Router
**Wireless Router** adalah perangkat jaringan yang berfungsi sebagai penghubung antara jaringan lokal (LAN) dengan jaringan luar seperti internet, sekaligus menyediakan koneksi nirkabel (Wi-Fi) untuk perangkat pengguna.

"Gampangnya, kalau router biasa itu seperti gerbang masuk ke internet lewat kabel, maka wireless router itu gerbang yang juga memancarkan Wi-Fi ke HP, laptop, dan perangkat lainnya."

### 2.1.3 Wireless Network Interface Controller (NIC)

### 2.1.4 Repeater / Range Extender

### 2.1.5 Point-to-Point (PtP) Wireless Bridge
#### 2.1.5.1 AirGrid M5 HP

## 3.1 Keamanan Jaringan Wireless

# TAHAPAN PRAKTIKUM

# TUGAS MODUL
