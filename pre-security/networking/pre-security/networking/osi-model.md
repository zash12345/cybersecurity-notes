# 🌐 OSI Model – Open Systems Interconnection

## 📘 Apa Itu OSI Model?
OSI (Open Systems Interconnection) adalah sebuah framework yang menjadi standar bagaimana perangkat dalam jaringan dapat saling berkomunikasi. 
Model ini membagi proses komunikasi menjadi tujuh lapisan yang masing-masing memiliki fungsi spesifik.

Manfaat utamanya: memungkinkan perangkat berbeda fungsi & desain tetap bisa saling memahami data.

---

## 🧱 Tujuh Lapisan OSI

### 🔹 Layer 1 – Physical
- Contoh perangkat: Kabel, konektor
- Fungsi: Menyampaikan sinyal listrik/fisik antar perangkat
- Protokol: Tidak ada, ini murni transmisi sinyal

---

### 🔹 Layer 2 – Data Link
- Contoh perangkat: Switch, Bridge
- Fungsi:
  - Komunikasi antar perangkat dalam satu jaringan
  - Pengalamatan fisik (MAC address)
  - Framing: Mengubah data jadi “frame” yang berisi data, MAC pengirim, penerima, dan kontrol kesalahan
  - Error detection (digunakan di LAN)

---

### 🔹 Layer 3 – Network
- Contoh perangkat: Router
- Fungsi:
  - Pengiriman data antar jaringan
  - Menggunakan IP Address sebagai identitas
  - Routing: menentukan jalur tercepat antar perangkat

#### ✴️ Routing Protocol
- **OSPF (Open Shortest Path First)** – berdasarkan jarak
- **RIP (Routing Information Protocol)** – berdasarkan jumlah hop

#### 📌 Faktor Penentu Jalur Routing
- Jumlah hop paling sedikit
- Jenis koneksi tercepat (fiber > tembaga)
- Riwayat jalur (packet loss)

#### 🔧 Proses Lain:
- IP Addressing: Penentuan alamat
- Reassembly: Penyusunan ulang data yang dipecah saat dikirim

---

### 🔹 Layer 4 – Transport
- Fungsi: Mengelola pengiriman data antara dua perangkat

#### ✴️ TCP (Transmission Control Protocol)
- Menyediakan koneksi konstan & handal
- Menjamin urutan data dan integritas
- Cocok untuk: web browsing, email, file sharing

#### ✴️ UDP (User Datagram Protocol)
- Tidak ada pengecekan error / koneksi konstan
- Lebih cepat tapi tidak handal
- Cocok untuk: streaming, game, VoIP

---

### 🔹 Layer 5 – Session
- Fungsi:
  - Membuka, mempertahankan, dan menutup koneksi antar perangkat
  - Menyimpan checkpoint data
  - Menghemat bandwidth

---

### 🔹 Layer 6 – Presentation
- Fungsi:
  - Menstandarkan format data agar dapat dipahami sistem lain
  - Translasi data, enkripsi, kompresi

---

### 🔹 Layer 7 – Application
- Fungsi:
  - Titik interaksi langsung dengan user
  - Protokol: HTTP, FTP, SMTP
  - Contoh aplikasi: browser, email client

---

## 🔄 Konsep Penting: Encapsulation
Saat data melewati setiap layer dari Layer 7 ke Layer 1, setiap layer menambahkan header informasinya masing-masing. 
Proses ini disebut **encapsulation** dan memastikan data bisa dipahami perangkat tujuan saat dikirim.

---

## 💡 Insight Pribadi
- Layer 3 dan 4 terasa sangat penting dan aplikatif, terutama saat nanti troubleshooting jaringan atau menganalisis log.
- Sekarang aku bisa mengerti kenapa traceroute bekerja di Network Layer, dan kenapa UDP digunakan untuk game online.

---

## 🔗 Referensi
- [TryHackMe Pre-Security Module](https://tryhackme.com/module/presecurity)
- [Wikipedia – OSI Model](https://en.wikipedia.org/wiki/OSI_model)
- [trustmebro]
- [my coffe]
