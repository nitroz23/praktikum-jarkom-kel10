# Crimping & Routing IPv4
## Daftar Isi
- 1 Dasar Jaringan Protokol
    - Kenapa Komputer Harus Terhubung ke Jaringan
    - Jenis-Jenis Jaringan
    - Jaringan Komputer Punya Aturan?
    - Semua Komputer Memiliki Alamat
- 2 Masuk ke IP Address
- 3 Masuk ke IPv4
- 4 Kenektivitas Kabel LAN
    - Crimpring
    - Routing Menggunakan Router
        - Statis
        - Dinamis
## 1 Dasar Jaringan Protokol
Apa Itu Jaringan Komputer?
"Bayangkan kamu tinggal di sebuah komplek perumahan. Tiap rumah punya keluarga yang ingin saling ngobrol, kirim surat, atau pinjam gula. Nah, kalau mereka saling terkoneksi, itu disebut jaringan."

Jaringan komputer adalah kumpulan perangkat (seperti laptop, PC, printer, dan router) yang terhubung satu sama lain untuk berbagi informasi atau sumber daya.

Pengandaian:
Rumah = Komputer

Jalan di antara rumah = Kabel jaringan

Surat yang dikirim antar rumah = Data

Tukang pos = Router

Tetangga ngobrol langsung = LAN (Local Area Network)

Tetangga beda kampung ngobrol = WAN (Wide Area Network)

### 1.1 Kenapa Komputer Harus Terhubung ke Jaringan
Bayangkan kamu ingin mengirim file dari satu komputer ke komputer lain **tanpa jaringan**, kamu harus meng-copy file tersebut ke flashdisk terlebih dahulu. Lalu mencabut dan mencolokkannya ke komputer tujuan. 

[Gambar meme nggak sih]

Bisa dibayangkan proses manual tersebut memakan waktu dan memiliki keterbatasan jarak. Bahkan risiko kerusakan atau kehilangan data. Namun, dengan pemanfaatan **jaringan** pengiriman file tidak perlu mengandalkan alat eksternal seperti flashdisk. Selain itu pemindahan file dapat dalam hitungan detik dan tanpa kamu berpindah tempat.

Jadi kids koneksi jaringan bukan sebagai kebutuhan tambahan aja, no no no. Karena tanpa jaringan kemampuan komputer menjadi terbatas.

### 1.2 Jenis-Jenis Jaringan

![Jenis-Jenis Jaringan Komputer](images/1.2_Network.png)

#### 1.2.1 Personal Area Network (PAN)
![PAN](images/1.2.1_PAN.png)

**PAN** atau *Personal Area Network* ibarat jaringan kecil yang hanya mengelilingi satu orang. PAN ini khusus buat menghubungkan perangkat pribadi kamu yang jaraknya deket-deket, sekitar 1-100 meter.

![MemePAN](images/1.2.1_MemePAN1.jpg)

Contohnya smartphone, laptop, smartwatch, bahkan printer yang kamu pakai sendiri bosa saling terhubung lewat jaringan ini.

**Fungsi PAN pada kehidupan sehari-hari:**
- Transfer file dari HP ke laptop lewat Bluethooh.
- Ngeprint dokumen dari laptop ke printer via USB

PAN ada 2 jenis:
- Wireless PAN: Nggak usah pakai kabel, dalam penerapannya memanfaatkan Bluetooth, WiFi, atau Zigbee. Contohnya kalau kamu lagi dengerin lagu pakai wireless headset dari HP kamu.
- Wired PAN: Pakai kabel, misalnya USB. Contohnya ketika kamu nyambungin HP ke laptop buat ngecas sekaligus sekaligus kirim file.

| ✅ **Kelebihan PAN**                                   | ❌ **Kekurangan PAN**                                                        |
|--------------------------------------------------------|-------------------------------------------------------------------------------|
| Praktis & fleksibel banget buat pemakaian pribadi      | Jangkauannya kecil, cuma buat sekitar 1 orang                                 |
| Biayanya murah dan gampang disetting                   | Kecepatan transfer data bisa terbatas, tergantung teknologinya                |
| Nggak perlu teknisi buat instalasi                     | Kadang perangkat nggak semua kompatibel satu sama lain                        |
| Mudah dibawa kemana-mana alias portable                | Beberapa teknologi PAN (kayak Zigbee) bisa agak mahal                         |
| Cocok buat orang yang pengen simple                    |                                                                       
#### 1.2.2 Local Area Network (LAN)
![LAN](images/1.2.2_LAN.png)

**LAN** atau *Local Area Network* adalah jenis jaringan komputer yang paling sering dipakai, terutama di tempat-tempat yang areanya terbatas, kayak di rumah, kator, sekolah, atau lab. Jarak jangkauan LAN maksimal 2 km dengan kecepatan transfer yang tinggi.

Jaringan ini menghubungkan **dua atau lebih** komputer dalam satu area lokal, pengaplikasian lewat kabel Ethernet atau Wi-Fi. Jika melalui Ethernet berarti menggunakan kabel LAN dan pengaplikasiannya dicolok ke switch atau router. Kalau pakai Wi-Fi nggak perlu pakek kabel dan pengaplukasiannya tinggal menggunakan hotspot

[Masukin meme bang :)]

Contohnya komputer di lab MIOT yang bisa diakses bersama atau semua komputer kantor yang bisa mengirim file satu sama lain.

**✅ Kelebihan LAN**

| Keunggulan                | Penjelasan                                                                 |
|-------------------------  |----------------------------------------------------------------------------|
| Privasi Terjaga           | LAN bersifat privat, jadi tidak diatur oleh badan eksternal tertentu       |
| Kecepatan Tinggi          | Bisa mencapai 100 Mbps atau lebih, cocok buat transfer file besar          |
| Banyak Media Transmisi    | Bisa pakai kabel UTP, fiber optic, bahkan Wi-Fi                            |
| Murah & Gampang Dipasang  | Instalasi, perawatan, dan pengembangannya relatif murah & simpel           |
| Fleksibel & Scalable      | Bisa ditambah komputer atau perangkat lain dengan mudah                    |

**❌ Kekurangan LAN**

| Kekurangan                | Penjelasan                                                                 |
|-------------------------  |----------------------------------------------------------------------------|
| Biaya Awal Lumayan        | Butuh perangkat tambahan seperti switch, router, dan software server       |
| Privasi Bisa Terganggu    | Admin jaringan bisa akses file pribadi dan history internet kamu           |
| Jangkauan Terbatas        | Hanya berlaku untuk area lokal, tidak cocok untuk area yang terlalu luas   |
| Risiko Keamanan Data      | Kalau server utama diretas, semua data di jaringan bisa bocor              |

#### 1.2.3 Campus Area Network (CAN)
**CAN** atau *Campus Area Network* adalah jaringan komputer yang ukurannya lebih besar dari LAN, tetapi masih lebih kecil dari MAN. CAN biasanya digunakan di sekolah, kampus, ataupun beberapa gedung dalam satu kompleks. Jarak konektivitas CAN 1 - 5 km.

Jadi bisa kamu bayangkan di TW2 ada lab MIOT, lab Robotik, ruang kelas di lantai 6, dan sekretariat di lantai 2 yang dihubungkan dalam satu jaringan—itulah CAN! Paham Ente ? 👊🏻

Teknologi CAN sama dengan LAN yang menggunakan Ethernet dan jika Wi-Fi.

| ✅ Kelebihan                                                          | ❌ Kekurangan                                                                 |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------|
| **Kecepatan**: Transfer data antarsistem lebih cepat karena menggunakan LAN, bukan internet umum.      | **Jangkauan Terbatas**: Tidak cocok untuk koneksi antar kota atau wilayah yang sangat luas. |
| **Keamanan**: Admin jaringan bisa mengatur akses dan menjaga jaringan dengan firewall.                | **Butuh Admin Tetap**: Diperlukan admin khusus agar jaringan tetap stabil dan aman.         |
| **Efisien Biaya**: Setup dan perawatan sedang, bisa pakai WiFi untuk menghemat kabel.                | **Bisa Overload**: Jika terlalu banyak pengguna aktif dan tidak diatur dengan baik.           |

### 1.3 Jaringan Komputer Punya Aturan??
IYA, disebut protokol komunikasi
contoh :
- TCP/IP
- HTTP/HTTPS
- FTP
- DHCP

### 1.4 Semua Komputer memiliki Alamat
Alamat apa nih? Misalkan rumahmu punyua nomor dan temanmu mau ke rumahmu jadi kamu kasih tau nomor rumahnya. Konsep jaringan komputer juga sama.

Identitas Komputer itu disebut IP Address

## 2 MASUK KE IP ADDRESS

## 3 MASUK KE IPv4

## 4 KONEKTIVITAS KABEL LAN
### 4.1 CRIMPING

### 4.2 ROUTING PAKE ROUTER

#### 4.2.1 STATIS 

#### 4.2.2 DINAMIS
