
# 🌐 Praktikum Jaringan Komputer

Selamat datang di repositori **Praktikum Jaringan Komputer**!  
Repositori ini merupakan kumpulan materi, desain, dan simulasi jaringan yang disusun selama kegiatan praktikum, menggunakan **Cisco Packet Tracer** sebagai media utama simulasi.

Disusun oleh: **David Mario Yohanes Samosir**

---

## 📘 Daftar Isi
- [🔰 Pengenalan](#-pengenalan)
- [📌 Tujuan Praktikum](#-tujuan-praktikum)
- [🧱 Materi dan Tahapan Praktikum](#-materi-dan-tahapan-praktikum)
- [📚 Penjelasan Tambahan: Subnetting & IP Address](#-penjelasan-tambahan-subnetting--ip-address)
- [🛠 Tools yang Digunakan](#-tools-yang-digunakan)
- [📥 Cara Menggunakan](#-cara-menggunakan)
- [📧 Kontak](#-kontak)

---

## 🔰 Pengenalan

Praktikum Jaringan Komputer ini bertujuan memberikan pemahaman mendalam tentang bagaimana merancang, mengkonfigurasi, dan mengelola jaringan komputer, baik dalam skala kecil maupun menengah. Praktikum dilakukan secara simulatif menggunakan **Cisco Packet Tracer**, sehingga dapat mengembangkan keterampilan praktis dalam desain dan implementasi jaringan.

---

## 📌 Tujuan Praktikum

- Memahami konsep dasar jaringan komputer dan protokol jaringan.
- Melakukan **subnetting** untuk efisiensi alamat IP.
- Mengimplementasikan simulasi jaringan nyata menggunakan Cisco devices.
- Menguasai teknik konfigurasi dasar hingga lanjutan jaringan.

---

## 🧱 Materi dan Tahapan Praktikum

### 1. Pengenalan Jaringan dan Topologi
- Jenis-jenis topologi jaringan (Star, Ring, Bus, Mesh)
- Media transmisi dan perangkat jaringan (Router, Switch, PC, dll.)

### 2. Subnetting dan Pengalamatan IP
- Konversi biner–desimal
- Perhitungan subnet (VLSM dan FLSM)
- Penetapan IP statis dan dinamis

### 3. Konfigurasi Dasar Cisco Router dan Switch
- Pengaturan IP address
- Konfigurasi interface
- Penggunaan CLI Cisco

### 4. VLAN dan Inter-VLAN Routing
- Pembuatan dan manajemen VLAN
- Trunking dan konfigurasi 802.1q
- Routing antar VLAN menggunakan router-on-a-stick

### 5. Routing (Static & Dynamic)
- Routing statik dasar
- Routing dinamis (RIP, EIGRP, OSPF)
- Troubleshooting routing table

### 6. DHCP, DNS, dan Server Setup
- Konfigurasi DHCP server
- Penetapan DNS di jaringan
- Simulasi web server/email server

### 7. Akses Jarak Jauh (Telnet/SSH)
- Pengamanan akses remote
- Autentikasi dan enkripsi
- Manajemen router via command-line remote

### 8. Keamanan Jaringan Dasar
- ACL (Access Control List)
- Firewall dasar di Cisco
- Simulasi serangan dan pencegahan

---

## 📚 Penjelasan Tambahan: Subnetting & IP Address

### 🔤 Kelas IP Address

| Kelas | Rentang IP                    | Oktet Pertama | Jumlah Host per Network | Digunakan Untuk              |
|-------|-------------------------------|----------------|--------------------------|------------------------------|
| A     | 1.0.0.0 – 126.255.255.255     | 1 – 126         | ± 16 juta                | Jaringan sangat besar        |
| B     | 128.0.0.0 – 191.255.255.255   | 128 – 191       | ± 65 ribu                | Jaringan menengah            |
| C     | 192.0.0.0 – 223.255.255.255   | 192 – 223       | 254                      | Jaringan kecil               |
| D     | 224.0.0.0 – 239.255.255.255   | 224 – 239       | -                        | Multicast (bukan untuk host) |
| E     | 240.0.0.0 – 255.255.255.255   | 240 – 255       | -                        | Eksperimen                   |

> Catatan: Alamat 127.x.x.x adalah reserved untuk **loopback** (localhost).

---

### 🧠 Cara Menghitung Subnet (Manual)

1. **Tentukan jumlah host yang dibutuhkan**  
   Rumus: `2^n - 2 ≥ jumlah host`  
   - `n` = jumlah bit host  
   - `-2` = 1 untuk network address, 1 untuk broadcast address

2. **Hitung subnet mask**  
   Pinjam bit dari bagian host untuk menambah subnet.

3. **Contoh:**  
   - Dibutuhkan 50 host  
   - Maka `2^6 = 64`, cukup (karena `64 - 2 = 62`)  
   - Subnet mask-nya: `255.255.255.192` atau `/26`

---

### 🔄 Perbedaan FLSM dan VLSM

| Kriteria       | FLSM (Fixed Length Subnet Mask)     | VLSM (Variable Length Subnet Mask)     |
|----------------|--------------------------------------|----------------------------------------|
| Subnet mask    | Sama untuk semua subnet              | Bisa berbeda untuk tiap subnet         |
| Efisiensi IP   | Kurang efisien (banyak IP terbuang) | Lebih efisien, IP disesuaikan kebutuhan |
| Kemudahan      | Lebih mudah dihitung                 | Lebih rumit (perlu perencanaan detail) |
| Contoh Kasus   | Digunakan saat host tiap subnet sama | Digunakan saat host tiap subnet berbeda |

### 🔢 Referensi Cepat Prefix Subnet:

| Prefix | Host per Subnet |
|--------|------------------|
| /24    | 254              |
| /25    | 126              |
| /26    | 62               |
| /27    | 30               |
| /28    | 14               |
| /29    | 6                |
| /30    | 2                |

---

## 🛠 Tools yang Digunakan

- ✅ Cisco Packet Tracer  
- ✅ Text Editor (Notepad++ / VSCode)  
- ✅ [Optional] GNS3 untuk simulasi lebih kompleks  

---


---

## 📥 Cara Menggunakan

1. Clone repositori ini:
```bash
git clone https://github.com/DavidMarioYS/Praktikum-Jaringan-Komputer.git
````

2. Buka file `.pkt` menggunakan **Cisco Packet Tracer**.
3. Ikuti dokumentasi konfigurasi yang tersedia di setiap folder.
4. Jalankan simulasi dan analisis hasilnya.

---


