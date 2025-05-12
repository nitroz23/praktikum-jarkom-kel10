# 📚 Daftar Isi
- [Tugas Pendahuluan](#tugas-pendahuluan)
- [Modul](#modul-routing-&-manajemen-ipv6)
- [Tugas Modul](#tugas-modul)
- [Referensi](#referensi)

# Tugas Pendahuluan

1. Jelaskan apa itu IPV6 dan apa bedanya dengan IPV4.
2. Sebuah organisasi mendapatkan blok alamat IPv6 2001:db8::/32.
    a. Bagilah alamat tersebut menjadi empat subnet berbeda menggunakan prefix /64.
    b. Tuliskan hasil alokasi alamat IPv6 subnet untuk:
        - Subnet A
        - Subnet B
        - Subnet C
        - Subnet D
3. Asumsikan terdapat sebuah router yang menghubungkan keempat subnet tersebut melalui empat antarmuka:
- ether1 (Subnet A)
- ether2 (Subnet B)
- ether3 (Subnet C)
- ether4 (Subnet D)
a. Tentukan alamat IPv6 yang akan digunakan pada masing-masing antarmuka router.
b. Buatkan konfigurasi IP address IPv6 pada masing-masing antarmuka router.
4. Buatlah daftar IP Table berupa daftar rute statis agar semua subnet dapat saling berkomunikasi.
5. Jelaskan apa fungsi dari routing statis pada jaringan IPv6, dan kapan sebaiknya digunakan dibandingkan routing dinamis.


# Modul Routing & Manajemen IPv6
## ❓ 1 Apa itu IPv6
![IPv6](images/1_IPv6.webp)

IPv6 atau Internet Protocol version 6 adalah generasi terbaru dari alamat IP. Nahh, IPv6 ini bisa ngasih jumlah alamat yang jauuuuh lebih banyak dibandingkan IPv4. Jumlah alamat IPv4 sekitar 4 miliar alamat, sedangkan IPv6 dia bisa nyediain 2 pangkat 128 alamat IP ngasih sampai 340 *undecilion* alamat! 340 + 36 nol dibelakangnya.

Format alamat IPv6 itu kayak gini:<br>
![IPv6 Representation](images/1_IPv6-Represantation.png)
<br>
Setiap "x" adalah angka heksadesimal (angka 0–9 dan huruf a–f), mewakili 4 bit. Nah, kalau ada nol di depan, bisa diskip biar lebih singkat. Misalnya 0042 bisa ditulis jadi 42. Terus, kalau ada banyak nol berurutan, bisa diganti ::, tapi cuma boleh sekali pakai dalam satu alamat.

Soal penerapannya, sekarang banyak perangkat udah mulai pakai Dual-IP Stack, artinya bisa jalanin IPv4 dan IPv6 sekaligus. Tapi kalau bisa, perangkat bakal lebih milih IPv6 duluan. Biasanya perusahaan-perusahaan gede mulai aktifin IPv6 dari router utama di jaringan luar (WAN), terus ke router di perbatasan, firewall, data center, sampai akhirnya ke router yang ngatur koneksi desktop.

## 📡 2 IPv4 v.s. IPv6
| Fitur                           | IPv6                                               | IPv4                                      |
| ------------------------------- | -------------------------------------------------- | ----------------------------------------- |
| *Panjang Alamat*              | 128-bit                                            | 32-bit                                    |
| *Konfigurasi Alamat*          | Mendukung konfigurasi otomatis & penomoran ulang   | Mendukung konfigurasi manual dan via DHCP |
| *Jumlah Alamat yang Tersedia* | Sangat besar: 3.4 × 10³⁸ alamat                    | Sekitar 4.29 × 10⁹ alamat                 |
| *Format Alamat*               | Ditulis dalam format heksadesimal                  | Ditulis dalam format desimal              |
| *Checksum*                    | Tidak tersedia di IPv6                             | Tersedia di IPv4                          |
| *Ukuran Header*               | Ukuran tetap 40 byte                               | Ukuran bervariasi antara 20-60 byte       |
| *Dukungan VLSM*               | Tidak mendukung VLSM (Variable Length Subnet Mask) | Mendukung VLSM                            |

## 3 Kemana IPv5?
Nah, lucunya… IPv5 itu sebenarnya nggak pernah benar-benar ada! 🤯
Meskipun angka “5” udah pernah dipakai sebagai versi protokol IP, versi IP yang resmi dikenal cuma ada IPv4 dan IPv6.

Yang disebut-sebut sebagai IPv5 itu sebenernya adalah Internet Stream Protocol (ST) — bukan pengganti IPv4, bukan juga pendahulu IPv6.

*Ceritanya gimana?*
1. Tahun 1979, seorang peneliti bernama James W. Forgie ngusulin protokol ini lewat dokumen eksperimen internet (IEN 119).

2. Tahun 1990, protokol ini dikembangkan jadi ST2 (Stream Protocol versi 2) lewat dokumen resmi RFC 1190.

3. Tujuan utamanya? Buat mengirim suara dan video lewat jaringan internet (kayak video call zaman sekarang).

4. Tapi… baik ST maupun ST2 nggak pernah dipakai secara luas. Semuanya masih tahap eksperimen aja.

*Jadi Kenapa Dikasih Nomor 5?*
Karena ST butuh cara buat ngebedain header-nya dari IPv4, akhirnya angka “5” dipakai sebagai tanda versinya di dalam paket data. Tapi ini bukan versi IP resmi. Gara-gara itu, biar nggak bingung, versi setelah IPv4 langsung loncat ke IPv6.

*Kok Nggak Jadi IPv5 Beneran?*
Masalah utama di IPv4 adalah jumlah alamat IP-nya cuma 4,29 miliar (karena 32-bit). Nah, ST/“IPv5” juga cuma bisa ngasih jumlah alamat segitu — artinya nggak nyelesain masalah kehabisan IP.

Padahal saat itu, kebutuhan akan alamat IP udah makin gila-gilaan. Bayangin aja, tahun 2025 diprediksi ada:
- 5+ miliar pengguna internet
- 27+ miliar perangkat IoT

Jadi, bikin “IPv5” yang kemampuannya sama kayak IPv4 itu ibarat tambal ban bocor pake permen karet — nggak tahan lama!!

Makanya, akhirnya diputuskan buat langsung loncat ke IPv6 yang bisa nyediain alamat IP hampir tak terbatas.

## 📦 4 Kunggulan dan Kekurangan IPv6
| ⚙ Aspek                             | ✅ Kelebihan IPv6                                                                       | ❌ Kekurangan IPv6                                                            |
| ------------------------------------ | -------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| 🔢 Alamat IP                         | Ruang alamat *sangat luas* (128-bit, bisa tampung 340 triliun triliun alamat)        | Belum semua perangkat dan sistem dukung IPv6 secara penuh                    |
| 🔗 NAT (Network Address Translation) | *Tidak butuh NAT*, langsung pakai global address                                     | Transisi dari NAT IPv4 ke non-NAT IPv6 butuh penyesuaian arsitektur jaringan |
| 🚀 Kecepatan                         | Umumnya *lebih cepat* dari IPv4 karena tidak pakai NAT dan struktur header sederhana | Beberapa jaringan IPv6 masih terbatas dan tergantung implementasi ISP        |
| 🔐 Keamanan                          | Sudah *mendukung IPsec secara bawaan*, lebih aman dan siap untuk enkripsi end-to-end | Masih rentan jika implementasi IPsec tidak diatur dengan benar               |
| 🔍 Pemindaian alamat                 | *Sangat sulit dipindai* oleh attacker karena jumlah alamat yang sangat banyak        | Jika attacker tahu pola, pemindaian masih bisa dilakukan (meski lebih sulit) |
| 🔒 Fitur keamanan ekstra             | Mendukung *SEND (Secure Neighbor Discovery)*, untuk validasi identitas perangkat     | Belum semua perangkat dukung atau implementasikan SEND                       |
| 🛠 Konfigurasi alamat               | Mendukung *SLAAC (Stateless Address Auto Configuration)* otomatis, tanpa DHCP        | Beberapa administrator lebih familiar dengan DHCP dari IPv4                  |
| 📦 Header paket                      | Header tetap 40 byte → *lebih ringan diproses*, tidak ada checksum yang memperlambat | Tidak ada checksum → keamanan data sepenuhnya bergantung pada layer lain     |
| 📡 Routing                           | Routing lebih efisien, *tidak terjadi fragmentasi paket di router*                   | Butuh update pada perangkat router lama agar dukung IPv6                     |
| 🌍 Adopsi global                     | Solusi jangka panjang untuk kebutuhan internet global dan IoT                          | Masih banyak ISP dan organisasi yang belum migrasi penuh ke IPv6             |

## Cara Menghitung Prefix IPv6

## Routing Statis IPv6

## Routing Dimanis IPv6

# Tugas Modul

# Referensi
## 1 [Apa itu IPv6](https://www.thousandeyes.com/learning/techtorials/ipv4-vs-ipv6)
## 1 [Apa itu IPv6](https://www.geeksforgeeks.org/what-is-ipv6/)
## 2 [IPv4 v.s. IPv6](https://www.geeksforgeeks.org/what-is-ipv6/)
## 3 [Kemana IPv5?](https://www.ipxo.com/blog/what-happened-to-ipv5/)
## 3 [Kemana IPv5?](https://www.cloudns.net/blog/ipv4-vs-ipv6-internet-protocol/)